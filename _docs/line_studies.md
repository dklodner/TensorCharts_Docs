---
layout: doc
title: VWAP, CVD, SMA, EMA
subtitle:
author:
tags: featured
---


You can’t customize colors of each line, however notice the width of the lines. The higher the period is, the wider the line gets.

#### Sections in this article
{:.no_toc}
* TOC
{:toc}

### VWAP - Volume Weighted Average Price
VWAP is calculated as a moving average derived from the price and adjusted by traded volume. This depicts a much more objective average price since it takes into account traded volume distribution. 

#### Standard deviations
VWAP is usually used alongside 1. and 2. standard deviation channels for mean reversion strategies.  You can define the interval of averaging as a number of candles in the bottom settings panel, as well as turn on/off the Standard Deviation (Std1, Std2).

For example, if the VWAP is set to a 20-period length, its deviations can produce the same signals as regular Bollinger bands. Thus, look for squeezes in volatility (compressed bands around price) prior to major trending moves in either direction.

<div class="summary-box">
<h4>HOTKEY:</h4>
<p>W = VWAP on/off</p>

<h4>TIPS:</h4>
<p>Set VWAP to 60, click on VWAP, Std1 and Std2 buttons and watch how price reverts back to the center line after crossing Std2 line.</p>
<h4>LINKS:</h4>
  <li> <a href="https://www.investopedia.com/terms/v/vwap.asp" target="_blank">Investopedia description</a></li>
<ul>
</ul>
</div>


### SMA, EMA
Multiple lines
Simple and exponential moving averages in TensorCharts can produce crossovers with price, or the famous golden and death crosses. However, when you insert multiple period lengths divided by a comma, you can overlay fishnets on the chart to best gauge for market compression and expansion as related to price.

You can’t customize colors of each line, however notice the width of the lines. The higher the period is, the wider the line gets.

### Cumulative Volume Delta - CVD
Line chart showing volume change of buy/sell volume delta. Interval of CVD defines moving window of cumulation. 0 interval means no moving window, it starts accumulating from the beginning. More about CVD in the following video.

<div class="videowrapper">
<iframe src="https://www.youtube.com/embed/gj-zxO-ZnSU?autoplay=0&amp;showinfo=0&amp;rel=0&amp;modestbranding=1&amp;playsinline=1" frameborder="0" allowfullscreen uk-responsive uk-video="automute: true"></iframe>
</div>


