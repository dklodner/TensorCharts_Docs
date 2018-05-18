---
layout: doc
title: F.A.Q. and Errors
subtitle: 
author:
---

#### Sections in this article
{:.no_toc}
* TOC
{:toc}

#### *Can’t see the main chart*
Try open up TC in incognito mode. If it helps then the problem is in browser’s localStorage. You can follow this guide on how to clear your localStorage. Be aware it deletes your TC settings and custom scripts. 


<a href="https://superuser.com/a/655198" target="_blank">https://superuser.com/a/655198</a>

#### *Counters ratio chart is empty*
You have to turn on counter ratio chart for each of your trades counters. See the chart pictogram next to trades counters settings.
Site is not loading or 502 bad gateway error page.
Check TC twitter account if there’s no server maintenance. Otherwise report it please on Discord channel “bug reports”.

#### *The site is blank*
See the issue above. If it’s neither server crash or maintenance and TC is not working in incognito mode, then you have probably old version of browser. TC is built on top of the latest web technology. Upgrade your browser. in order to get the best experience
An alert about  timing popped up. What shall I do about if?
Check your clock time (system time). Toggle on and off the automatic system time just to make sure the in-app timing processing is correct.

#### *Bitfinex order book is empty above 10k.*
Bitfinex handles orderbook precision differently than other exchanges therefore the orderbook can look empty or buggy during a order transition - 1s->10s->100s->1000s.... Orderbook will readjust its precision once the price is near the limit price.
Site is not loading or 502 bad gateway error page.
Check TC twitter account if there’s no server maintenance. Otherwise report it please on Discord channel “bug reports”.

#### *Hotkeys are not working.*
Hotkey are disabled when your chat box or scripting module is active/open.

#### *Site layout is different than in your videos. How do I get orderbook next to chart?*
Your screen resolution or window size is probably too small. You can also try to decrease site zoom.  For chrome users: 


<a href="https://support.google.com/chrome/answer/96810?hl=en" target="_blank">https://support.google.com/chrome/answer/96810?hl=en</a>

#### *I don’t see counters ratio chart on mobile phone*
Counters ratio chart is hidden for mobile devices as a part of the performance optimization.

#### *Why I can’t filter out some trades counters by volume?*
Volume filter of trades counters is limited for intervals less than 60 minutes.

#### *The last candle is few hours old*
Report it in chat box or on Discord. Some pairs/markets data feeds are not stable yet. 

#### *Can’t scroll more than a few weeks/months back*
TensorCharts is currently showing only data since each market was connected to server. More data will downloaded in the future for exchanges which allow to download tick history 

#### *Can I copy settings from one pair to another?*
Not at this moment. I should be possible soon with user accounts. 
