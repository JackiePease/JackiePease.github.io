---
layout: post
title:  "Week Notes - You Win or You Learn"
date:   2022-10-26`16:00:00 +0100
categories: weeknotes
---

A quote from Nelson Mandela apparently. It’s been in my head recently as I spent several days working on an LED project I shouldn’t have agreed to do with too little time, too little experience with the tools I eventually had to use, and without ever getting to see the physical installation. It feels like I’ve learnt a lot though and I'm inspired to learn more. So here's a few rough notes, so I don’t forget, and in case there's anything useful to other people.

## Sensors

Originally there was a plan to use a sensor to control the speed that the lights moved and their brightness.  I experimented with several different inputs:

#### Potentiometer

![esp32_with_potentiometer.jpg](https://jackiepease.github.io/assets/weeknotes_20221026/esp32_with_potentiometer.jpg)

I used [this code from Sensing the City](https://www.sensingthecity.com/controlling-an-addressable-led-strip-with-any-sensor/) to make a light move along a strip of LEDs (it looks even better if it's moving around a disk!). Sensing the City is a great site, with loads of other good ideas.

#### Capacitive Touch Sensor

![capacitive_touch.jpg](https://jackiepease.github.io/assets/weeknotes_20221026/capacitive_touch.jpg)

I already had an Adafruit CAP1188 breakout, recommended to me by Chris E at the Friday night cycling group I go to. It was easy to set up following [the instructions on the Adafruit site](https://learn.adafruit.com/adafruit-cap1188-breakout) and worked well, although I didn't go further than blinking the onboard lights on this occasion. It seems worth putting in a bit more time and investigating some of its other features.

Although I didn't get to use the Azoteq pressure sensor originally suggested for the project, I did see an Arduino sketch that used it. It looks as though there's more to set up, but apparently it is very reliable, so might be worth further investigation too.

#### Pressure Sensors

We've used home made pressure sensors a lot at DoES Liverpool, mainly because we've found them a bit more predictable than capacitive touch. 

I refamiliarised myself with these foam/wire/Velostat sensors that we made for [Laura Pullig / Lanacaster Univerity's What Does Health Look Like? project](https://getamoveon.ac.uk/events/what-does-health-look-like):

<blockquote class="twitter-tweet"><p lang="en" dir="ltr">Here’s <a href="https://twitter.com/SoleRebelTapUK?ref_src=twsrc%5Etfw">@SoleRebelTapUK</a> testing out pressure sensors <a href="https://twitter.com/DoESLiverpool?ref_src=twsrc%5Etfw">@DoESLiverpool</a> for ‘What Does Health look like’ with <a href="https://twitter.com/davidaellis?ref_src=twsrc%5Etfw">@davidaellis</a> &amp; <a href="https://twitter.com/GAMONetwork?ref_src=twsrc%5Etfw">@GAMONetwork</a> <a href="https://t.co/8pqFMPdOW1">pic.twitter.com/8pqFMPdOW1</a></p>&mdash; laura pullig (@Laura_pullig) <a href="https://twitter.com/Laura_pullig/status/1094233839629680640?ref_src=twsrc%5Etfw">February 9, 2019</a></blockquote> <script async src="https://platform.twitter.com/widgets.js" charset="utf-8"></script> 

They work well and can use similar code to the potentiometer.

Along with Chris T, I also refurbished one of these much larger, but functionally similar, pressure sensors from [MCQN Ltd's Play the Tree/Geometric Lights](https://mcqn.com/ibal191/). There are another 3 of these at DoES Liverpool and we're now thinking of new uses for them:

![large_pressure_sensor.jpg](https://jackiepease.github.io/assets/weeknotes_20221026/large_pressure_sensor.jpg)
 
## Mapping Irregular LED Layouts
The project involved a fairly large number of pixels, arranged irregularly. In the end some of the pixels weren’t added until the day before the project shipped, so they had to be laid out physically in the order they would light up. I did try out several tools that might help me do pixel mapping in future though:

#### [xLights Generate Custom Model](https://manual.xlights.org/xlights/chapters/chapter-five-menus/tools/generate-custom-model)
I’ve tried this before, and I didn’t have any more luck this time. The consensus seems to be that you need a decent camera, so I think it’s going to be worth borrowing one, watching a bunch of YouTubes, and trying again. On the other hand, I did find out that you can now control WLED via wifi from xLights on your laptop, so all good.

This [semi-automatic pixel mapper](https://github.com/aaknitt/pixel_mapper) might also be worth investigating.

#### [LED-Mapper](https://jasoncoon.github.io/led-mapper/) by Jason Coon

This is great - you do have to use Google Sheets to create a layout first, but it then allows you "to generate and visualize maps for irregular and/or gapped LED layouts, for use with FastLED, Pixelblaze and other libraries" and "also generates coordinate maps for radius and angle."

I used both a disk of regularly spaced rings (wired as a spiral) and an irregular spiral made from WS2811 Xmas tree style pixels, taped onto Correx. Both were good although obviously the more closely-packed disk shows the pattern much better. This Tweet shows the regular disk running Jason Coon's example sketch:

<blockquote class="twitter-tweet"><p lang="en" dir="ltr">Disappointingly I haven&#39;t got <a href="https://twitter.com/hashtag/xlights?src=hash&amp;ref_src=twsrc%5Etfw">#xlights</a> Generate Custom Model to work yet, so have been using laser cut PP grids, then switching on LEDs sequentially, in order to get them into the spreadsheet to start off with...<a href="https://twitter.com/hashtag/weeknotes?src=hash&amp;ref_src=twsrc%5Etfw">#weeknotes</a> <a href="https://t.co/sp6eTwJbZE">pic.twitter.com/sp6eTwJbZE</a></p>&mdash; Jackie Pease (@jackie_pease) <a href="https://twitter.com/jackie_pease/status/1576696560481509376?ref_src=twsrc%5Etfw">October 2, 2022</a></blockquote> <script async src="https://platform.twitter.com/widgets.js" charset="utf-8"></script> 

I used laser-cut polypropylene grids to work out the coordinates of the pixels, but Jason replied to the Tweet recommending [this](http://app.bhencke.com/pixelmap.html), which should be easier and more accurate.

I put together a quick push button circuit on the Arduino to help me identify the next pixel in line in the irregular spiral, and I can see that being useful again. The sketch is [here](https://github.com/JackiePease/LEDTests/tree/main/Button_LED).

## Raspberry Pi as localhost with several ESP32s running WLED (or PicoWs?)

Another thing I didn't get very far with before it became apparent that we weren't going to use it, but I found some easy to follow instructions [here](https://pimylifeup.com/raspberry-pi-mosquitto-mqtt-server/) and [here](https://learn.sparkfun.com/tutorials/setting-up-a-raspberry-pi-3-as-an-access-point/introduction). I'd like to take this further.

There are some alternatives to mqtt that might be worth looking at too - e.g. [this YouTube](https://www.youtube.com/watch?v=LkGCo9Gi8mk) shows how to make a lightshow with WLED, FPP, xLights and DDP data.

## Arduino Mega 2560

This was what I finally wrote the sketch on, as there was one on site and I had one here. Memory was a bit of an issue,  and because I didn't get to see the final output, I wasn't able to easily make amendments when things didn't work as the users wanted (another lesson learned is that it might have helped to demonstrate the kind of effects that can be created at the start, and with what density of pixels).

Thanks to Adrian and Chris T for advice on C++ ([the current spaghetti](https://github.com/JackiePease/LEDTests/tree/main/October_LED_Project) is my responsibility). 

So I still want to do more LED projects...
