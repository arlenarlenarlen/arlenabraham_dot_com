---
layout:	page
title:	"title"
date:	2014-10-12 12:37:36 -0800
categories:	product
thumbnail:	images/somethumb.img
caption:	"Caption might be useful somehow"
type:	"Product Design"
intro:	"Introtext here"
---

<div class="wrapper" markdown="1">
Sarah Tappon, Andrew Kurtz, and I built the @DisruptHorn over the weekend of May 9-10, 2015 as an entrant in the “[Stupid Shit No One Needs & Terrible Ideas Hackathon](https://stupidhackathon.github.io/2015.html).”

The @DisruptHorn is a disruptive IoT wearable that triggers a 120dB airhorn whenever someone uses the hashtag #disrupt.

We wrote a Python microservice that runs on Herkou to listen to the Twitter Streaming API for tweets that contain the hastag #disrupt. This triggers the Spark API to fire the Spark Core (Coretex M3 + WiFi), which activates a heavy-duty hobby servo to trigger the airhorn. Typical delay between tweet and airhorn is <1000ms.

Originally, the @DisruptHorn also featured a bot that would tweet BYOOOORRRRRRRNK (where the number of R's is random, between 6 and 25) at anyone who used the hashtag #disrupt. This bot was found to be in violation of Twitter's Terms of Service and banned.

Materials: airhorn, plywood, wood glue, screws, cable ties, usb battery, velcro strap, cable tie mounts, 1/8" 316L TIG filler welding rod, Spark Core wifi-connected microprocessor, hobby servo, Heroku dyno

[github](github), [twitter](https://twitter.com/disrupthorn), [web](https://disruptor.herokuapp.com/)

May 2015
</div>
