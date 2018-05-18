---
layout: doc
title: Introduction to scripting module
subtitle: Cras at dolor eget urna varius faucibus tempus in elit. Cras a dui imperdiet, tempus metus quis, pharetra turpis.
author:
---

#### Sections in this article
{:.no_toc}
* TOC
{:toc}

TC Scripting Module allows you to access all of the data loaded in app. You can easily code
and analyze TC data, only basic basic JavaScript knowledge is required. Scripting Module comes with a few helper functions and libraries to ease your coding. 

Basics mechanics of the script: you write a data analysis, define name and interval (milliseconds). So if you set the interval e.g to 2000, it runs every 2 seconds.

<div class="caution">
Save copies of your scripts outside TC. Also data structures and API can change in the future.
</div>

### Data
Description of each data structure is not part of this manual. To study TC data, open browser console (F12) and output desired data to console, e.g. console.log(trades)

| data  |   description                      |
|:--------|:-------------                 | 
| ***trades***      | last 20min of trades feed           |
| ***largeTrades*** | last 24h of large trades |
| ***orderBook*** | current orderbook |
| ***chartData*** | trades heatmaps, orderbook heatmaps, candles, volume bars,... |
| ***currentRangeChartData*** | chart data of current range(domain) |
| ***counters*** | your current counters |
| ***market*** | market name |
| ***exchange*** | exchange name |

	

Each script has its own scope accessible by "self." prefix. You can store there script’s state variables for the next script run.

### Functions and libraries
TensorCharts provides you few functions and libraries which allow you to enhance capabilities of data analysis scripts and also to interact with TC itself, like charting price lines/annotations or creating your own voice assistant.

#### Functions

| function  |   description                      |
|:--------|:-------------                 | 
| ***speak***(textToSpeech string)       | your own voice assistant           |
| ***beep***(type int)       | sound alarm (type 1==positive, 2==negative), type can be omitted == default sound          |
| ***browserNotification***(title string, message string)      | sit creates browser’s push notification so you don’t have to watch TC all the time          |

 

#### Libraries
simple-statistics library as "**statistics**" object
<a href="https://simplestatistics.org/docs/" target="_blank">https://simplestatistics.org/docs/</a>


technical analysis library as "**TA**" object
candlesticks and price patterns detection or 25+ indicators
<a href="https://github.com/anandanand84/technicalindicators#user-content-available-indicators" target="_blank">https://github.com/anandanand84/technicalindicators#user-content-available-indicators</a>



