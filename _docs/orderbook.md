---
layout: doc
title: Orderbook
subtitle: 
author:
tags: featured
---

#### Sections in this article
{:.no_toc}
* TOC
{:toc}

The Order book is a basic part of every standard market structure. When you place a limit order, you are part of the order book even if you do not realize it. When you buy or sell via market order you are taking liquidity directly from order book (you are counterparty to some already pending limit orders in order book). Examination of the order book can bring you another dimension of information that is not visible on a price chart. TensorCharts order book allows you to see the most important information from it and several order book related tools and settings to maximize your output info.

### Volume highlighter and charting
Type desired volume level to highlight only order book zones with a larger volume than your number. Use the chart pictogram button to plot these areas to the price chart.

### Count
Count function enables to display exact number of limit order on every order book level. You can evaluate importance of price zone not only by the limit orders volume but also intensity. Sometimes you can also spot single large orders that are being send to market to fake short term traders decision making process.

Only available for Bitfinex.

### Precision
Precision allows you to see the order book in several ways. You can zoom(+) waiting limit orders to see every single price level detail or unzoom(-) to let TensorCharts count them together on an aggregated scale basis - which is more practical for most traders.

### Ask/bid side
Ask limit orders are pending limit order to buy (red colour) and bid limit orders are pending limit orders to sell (green colour). The Order book aggregates them to a vertical row and divides them by the current price level and different colours.

### Buy/Sell counter
Measure volume of buyers and sellers for every price level in real time. Have a look at the most attractive zones for both buyers and sellers and quickly spot zones where whales tend to be active.

### Book Counter
Measure Order Book pressures by identifying how the volume of limit orders is affecting price change. Focus on the zones where you expect a price reversal to occur and confirm your trade ideas with the Book Counter in real time.

- **Interval**: Select number of rows to display. Number represents the sequence of rows on each side of the market.

- **Fixed/relative settings**: Tweak the Book Counter settings by adjusting the number of rows to consider - fixing them relative to the actual price level, or whichever price you wish to observe.

- **start/stop**: On/off button for the book counter function.

<div class="videowrapper">
<iframe src="https://www.youtube.com/embed/Q7D7AIKjudM?autoplay=0&amp;showinfo=0&amp;rel=0&amp;modestbranding=1&amp;playsinline=1" frameborder="0" allowfullscreen uk-responsive uk-video="automute: true"></iframe>
</div>


<div class="summary-box">
<h4>HOTKEY:</h4>
<p>Spacebar = start/stop book counter</p>

<h4>TIPS:</h4>
<p>Levels with the largest intensity are important for future market development.</p>
<p>Zones without large volume are often areas where the price tends to pass by faster than those with larger volume.</p>
<ul>
</ul>
</div>