---
template: post
title: 'Optimizing network bandwidth for my gaming PC  '
slug: optimize-network-bandwidth-verizon-gaming-pc
draft: false
date: 2025-07-20T06:15:44.639Z
description: >-
  In this article i detail a lot of little lessons i learned on the way to
  becoming a 400lb neckbeard. I also improved the network speed on my gaming PC
  by a factor of 10x. You win some you lose some, i guess. 
category: random
tags:
  - network
  - bandwidth
  - gaming
---
When I first started playing on pc, i couldn't get higher than ~30mbps throughput no matter what, even though i have FIOS and am technically paying for gigabit internet. I can't run an ethernet cable up to my gaming PC because it's too far and I would have to drill through walls, which I'm not gonna do as a renter. And I never had any deadzones in my house, which made me doubt the low speed as being a range issue that requires a wifi extender or mesh network. I wanted to see if i could improve my bandwidth, and i was able to with a few network config changes and a hardware upgrade. 

A quick lesson on networks and radio signals. There are 3 bands which devices can connect to the network: 2.4Ghz, 5Ghz, and now, 6Ghz. 2.4Ghz has longer range and generally handles interference better (aka walls), but its max bandwidth is limited to around 35mbps. 5Ghz allows for upwards of 100mbps download speeds over radio (best case), but has less penetration / range. 6Ghz is just faster than 5ghz -- around 700mbps w/ no interference. 

Verizon has a feature called SON (Self Organizing Network) which automatically selects the optimal Wi-Fi band for connected devices. So, because my gaming rig's network signal was weaker than other connections, it exclusively put me on the 2.4Ghz radio band.  You can fix this two ways: you can either login to the router and create a new network SSID for the 5Ghz connection specifically, or you can change your network card driver settings to [configure a preferred WiFi-band](https://superuser.com/questions/1774002/i-want-to-force-windows-11-to-only-use-2-4ghz-wifi-but-the-driver-options-doesn#:~:text=To%20force%20use%202.4GHZ,either%205GHZ%20or%202.4GHZ.). i opted to do the latter because I think having multiple SSIDs in the same house is a clunky UX. By just flipping these network configs, i was able to boost my network speeds from 35mbps to around 90. Not bad!  Downloading game updates / patches takes seconds, not minutes. 

Note: The downside of setting your wifi to prefer a specific band (i.e. 5Ghz) is that managing the optimal radio band becomes your responsibility. It still makes sense to force 2.4Ghz when you need to minimize packet loss. For applications that use TCP instead of UDP,  (like watching youtube) the higher interference made streaming video harder since the packets need to come in a specific order. So, tradeoffs. 

# Hardware Upgrade

I noticed that after fiddling around with my network router settings (CR1000A), it had the option of enabling 6Ghz! However, my network card didn't support it. So, I bought and installed the AX210NGW Wifi Card that supports 6Ghz. The entire process very easy, and the new network speed is 400mbps!! 



![A large game being downloaded at ~400mbps, a 10x improvement over the original 32mbps.](/media/new-network-card.png "new-network-card-download-screenshot")