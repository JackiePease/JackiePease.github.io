---
layout: post
title:  "Week Notes - My Bike's Got LED (Of Course)"
date:   2022-11-07 21:00:00 +0100
categories: weeknotes
---

If you know me, you might be aware that I'm quite keen on addressable LEDs, so, while I already had a light up backpack for cycling (a prototype for [Peloton Liverpool](https://peloton.coop)'s [Disco breastplates](https://twitter.com/PelotonLiv/status/1499019125011668996?s=20&t=nDrJC5sKxXCYXhn_cV9HPQ)), I couldn't resist buying a [MCQN Ltd](https://mcqn.com/) [My Bike's Got LED board](https://twitter.com/huffeec/status/1585560542080638979?s=20&t=gtIk50p2UsO_uZefMUf0Gg) after watching the flurry of activity here at DoES Liverpool as Adrian and Chris got the first batch ready - they were launching with Peloton Liverpool Joyride cyclists taking part in [Katumba Drumming](https://katumba.co.uk/)'s Halloween event.

It was a great night (more detail in Chris's post [here](https://mcqn.com/posts/2022-10-31-weeks-889-891-More-Bikes-got-LED/)). I didn't quite get my lights ready in time, but a few cable ties the next morning was all it took to finish the job:

<blockquote class="twitter-tweet"><p lang="en" dir="ltr">How my bike might have looked at yesterday&#39;s excellent <a href="https://twitter.com/KatumbaBloco?ref_src=twsrc%5Etfw">@KatumbaBloco</a> <a href="https://twitter.com/hashtag/halloweenparade?src=hash&amp;ref_src=twsrc%5Etfw">#halloweenparade</a> <a href="https://twitter.com/PelotonLiv?ref_src=twsrc%5Etfw">@PelotonLiv</a> <a href="https://twitter.com/hashtag/joyride?src=hash&amp;ref_src=twsrc%5Etfw">#joyride</a> if I&#39;d fitted my <a href="https://twitter.com/MCQN_Ltd?ref_src=twsrc%5Etfw">@MCQN_Ltd</a> <a href="https://twitter.com/hashtag/mybikesgotled?src=hash&amp;ref_src=twsrc%5Etfw">#mybikesgotled</a> board in time.<br>Everyone else&#39;s looked fantastic though and mine is now ready for future trips.<a href="https://twitter.com/hashtag/weeknotes?src=hash&amp;ref_src=twsrc%5Etfw">#weeknotes</a> <a href="https://t.co/6bPZrMqE2M">pic.twitter.com/6bPZrMqE2M</a></p>&mdash; Jackie Pease (@jackie_pease) <a href="https://twitter.com/jackie_pease/status/1586751768901419010?ref_src=twsrc%5Etfw">October 30, 2022</a></blockquote> <script async src="https://platform.twitter.com/widgets.js" charset="utf-8"></script> 

The boards use open source [WLED software](https://kno.wled.ge/), which makes it easy to control a variety of addressable LEDs (WS2812 in this case) via wifi using a phone app or your computer. At it's simplest you can just set the number of lights, choose an effect, apply colour and speed settings and you're ready to go. In this case, I had 2 rows of LEDs, divided into 3 parts each, so it made sense to put a little bit more work in and define segments.

This is just a case of telling WLED the starting and ending position of each segment - some of the LEDs on my bike are hidden under black heatshrink so I haven't included them in the segments. Depending on the layout you can reverse the order that a segment lights up in, or even set it as a mirror of the previous segment:

![segments.jpg](https://jackiepease.github.io/assets/weeknotes_20221107/segments.jpg)


I couldn't easily use the mirror option as my layout wasn't symmetrical:

![lights_diagram.jpg](https://jackiepease.github.io/assets/weeknotes_20221107/lights_diagram.jpg)

That might be something to consider next time, although the Reverse Direction option has worked well.

It's important to save all your settings, including segments, in presets, otherwise you'll lose them when you switch the board off, and it isn't difficult to [backup your settings to JSON files](https://github.com/Aircoookie/WLED/issues/146) either. From your browser, just type in the following 2 commands:


* [WLED-IP]/edit?download=cfg.json

* [WLED-IP]/edit?download=presets.json

where [WLED-IP] is the IP address of your board.

The good thing about WLED is that it's so easy to get started, although there's a lot more you can do if you want. I'm looking forward to some sound reactive stuff, as the group cycle rides organised by Peloton Liverpool nearly always have music; it would be good to be able to sync effects across the whole group too. I think Adrian and Chris have some of this planned for their v2 board.

Having the board makes things easy too - you could buy a dev board and source all the components yourself, but it's good to be able to move straight on to the fun bit and know it'll work.



