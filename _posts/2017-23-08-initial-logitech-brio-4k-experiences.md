---
layout: post
title: "Initial Logitech Brio 4k Experiences"
date: "2017-08-23 00:12:34 -0400"
categories: [tech]
tags: [video]
---
Recently I was playing around with the [Logitech BRIO](http://www.logitech.com/en-us/product/brio){:target="_blank"}, to see what potential it has for livestreaming 4k video content from Zoos or other locations in a city that might be useful for schools in the area.   My results with the camera itself were pretty good but getting live 4k video out can be demanding on both the local machine and network, but the potential seemed solid and the camera was dead easy to setup.  Getting software and services to play well with the camera can take a bit, my only real efforts were spent streaming to YouTube using [Open Broadcaster System](https://obsproject.com/){:target="_blank"}.

![logitech biro camera](/assets/images/20170731_logitechbrio.jpg){:class="img-responsive"} The camera itself just connects straight to your system via a USB cable. Although it's backwards compatible with various USB standards, to get 4k quality you really want to connect to a USB 3.1 port. System drivers run the camera just like any other webcam and it connects to software as any other normal camera sources on your system.  Heat on the camera didn't seem to be an issue and I left it up and streaming for a few hours without any significant heating issues.  The camera does some dynamic video adjustment but the lag coming out of the camera itself isn't too bad and in-line with the kind of lag you'd get from normal HD webcams.

The largest challenge was on connecting it to an appropriate piece of software and getting the quality out in some usable format.  For my own tests I used OBS (linked above) and getting that to go out at 4k quality wasn't straight forward.  I had to get into the Settings > Video menu and physically type in the resolution I wanted (it wasn't available in the dropdown), I had to set the bitrate to 25k manually as well.  One of the biggest system impacts for me was compression, I dialed down amount of compression in the settings as much as possible because that seems to have a significant impact on the actual video quality and particularly CPU if the software compression is even at a moderate level.  When I had CPU usage set to fastest (highest cpu) I was pegging out my quad core 3.1 Ghz chp at about 80% so utilization was pretty significant.

With the proper settings I was able to get video out to YouTube and it offered 4k streaming as an option, but my personal experienc varied a bit when viewing the actual livestream.  Also, at 4k I experienced a good bit of buffering on my home network under Verizon's Gigabit FIOS service.

I'll keep working with the camera to explore it's potential in other context.  At $200 it's a great cost for the quality of camera and I feel confident that as software for broadcasting, and networks improve, that it wont be hard to find useses for this in education, telemedicine and on other fronts.