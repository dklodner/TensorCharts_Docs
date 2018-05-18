---
layout: doc
title: Example of a TC script
subtitle: 
author:
---

#### Sections in this article
{:.no_toc}
* TOC
{:toc}

```js
// Detection of large limit order cancelation or insertion 
// Set percentage range of orderbook to be analyzed

//console.log(orderBook)

// Orderbook data structure:
// orderBook = {price:[amount, count], price:[amount, count], ...}
var PERCENTAGE_RANGE = 5;

// Get the latest price from which the range will be calculated
// if trades data is empty, set prite to -1, otherwise get the most recent one
var lastTradePrice =  trades.length>0 ? trades[0].Price : -1

// Large limit order will be defined as a multiple of limit orders' median
var MEDIAN_MULTIPLICATOR = 1

// We don't have to calculate median every cycle/run, so we keep cycles'
// counter and analyze distribution only every nth cycle
var CYCLES_LIMIT = 5
if(self.cyclesCount == undefined){
  self.cyclesCount = 0
}

// Prerun check if all required data are loaded
// We need to store orderbook state from previous cycle so we can
// compare it with the current one
if(lastTradePrice > 0 && self.previousOrderBook!=undefined){
    // setting up price range defined by upper and lower limit
    // orderbook data is an object with price levels as keys and 
    // [amount, count] as its value

    // get all orderBook object keys
    var priceLevels = Object.keys(orderBook)
    
    var upperLimit = lastTradePrice * (1+PERCENTAGE_RANGE/100)
    var lowerLimit = lastTradePrice * (1-PERCENTAGE_RANGE/100)
    
    // Calculate volume median of orderbook price levels
    if(self.largeLimitOrderAmount==undefined ||   self.cyclesCount >= CYCLES_LIMIT){
        // reset cycles count
        self.cyclesCount = 0
        var medianData = []
        
        // loop through price levels and populate medianData 
        for(var i = 0; i < priceLevels.length; i++){
            var price = priceLevels[i]
            if (price <= upperLimit && price >= lowerLimit){
                var volume = Math.abs(orderBook[price][0])
                    medianData.push(volume)
            }
        }
        
        var median = statistics.median(medianData)
        
        // define large limit order amount
        self.largeLimitOrderAmount = MEDIAN_MULTIPLICATOR * median

    }

    // Compare previous orderbook with the current one
    for(var i = 0; i < priceLevels.length; i++){
        var price = priceLevels[i]
        if (price <= upperLimit && price >= lowerLimit){
            var currentAmount = orderBook[price][0]
            var previousAmount = self.previousOrderBook[price][0]
            
            // if the price level was bid in previous cycle and now it's ask or vice versa, return back to the loop start
            if((currentAmount < 0 && previousAmount > 0) || (currentAmount > 0 && previousAmount < 0)){
                continue   	 
            }
            
            currentAmount = Math.abs(currentAmount)
            previousAmount = Math.abs(previousAmount)
                            
            var diff = Math.abs(currentAmount - previousAmount)
            
            // return back to the loop start if size differece is less than calculated largeLimitOrderAmount
            if(diff < self.largeLimitOrderAmount){
                continue
            }
            
        
            if (price < trades[0].Price){
                if(currentAmount > previousAmount){
                    speak(" buy wall canceled at  " + price) 
                } else {
                    speak(" new buy wall of " + currentAmount.toFixed(1) + " detected at " + price) 
                }
            } else {
                if(previousAmount > currentAmount){
                    speak(" sell wall canceled at " + price) 
                } else {
                    speak(" new sell wall of " + currentAmount.toFixed(1) + " detected at " + price) 
                }
            }

        }
    }
}
        
          
// save current orderbook as previous
self.previousOrderBook = Object.assign({}, orderBook);

self.cyclesCount++;
```