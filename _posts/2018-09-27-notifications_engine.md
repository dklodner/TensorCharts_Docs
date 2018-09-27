---
layout: post
title: Notification engine and TC alerts
categories: []
tags: notifications
author: David
---



It’s been a rough week, but we made it through. The roll-out of paid subscriptions and bug fixing took a few days, update of websocket servers, couple of sleepless nights but your support exceeded my expectations and I would like to thank you for that.

TensorCharts has been stable as never before for the last 4 days so I took some time to review the survey from August and ended up with a to-do list containing 100 features/items. 

I will reshift my focus a little bit more on the front-end side in the upcoming weeks/months, improving the current features and start working on some new ones. One of which is the notification engine and alerts...

This was one of the most prevalent requests in the survey  
<blockquote>“...make trader’s life and sleep easier with alerts and notifications. Watching market going sideways is boring and switching between markets isn’t fun either...”.</blockquote>

#### Win 1 month of Premium plan

Designing a notification engine can be tricky. I will outline some ideas but your input is crucial here. Let’s design it together, this will take some time and multiple iterations to get it right but it can’t be done by one or two people.

This engine should be based on order flow data, starting in the first version as a stream of events from all markets. Events like 
- large trades
- liquidations
- high trades counters ratio
- high relative trading volume
- vwap
- standard deviation cross
- price close to Volume Profile POC (VAH, VAL)
- *and more...*

As we progress the design, these events should be accessible via  “alerts builder”, where anyone can define certain conditions and build their own notifications. 

example:  <small>(<i>taken from the survey, not my idea</i>)</small> 
```
IF 5min_counters_ratio < -2 
AND 5min_rel_volume > 3 
AND 2min_large_trades > 400 
= sendAlert(email)
```



Three best answers of the following survey will **win 1 month of PREMIUM plan** (ends 30.9.2018)

<a class="link" href="https://goo.gl/forms/7UBVmTJhf84PXzQj1" target="_blank">https://goo.gl/forms/7UBVmTJhf84PXzQj1</a>
<br>
<br>

Looking forward to reading your ideas.

Have a good one,
<br>
David.



