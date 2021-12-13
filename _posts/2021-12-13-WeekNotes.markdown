---
layout: post
title:  "WeekNotes - Plotting with Refillable Pens"
date:   2021-12-13 00:00:00 +0100
categories: weeknotes
---
Recently I've been spending a lot of my free time working on these [lights](https://twitter.com/amcewen/status/1467598114559299588?s=20), along with other members of the  [DoES Liverpool](https://doesliverpool.com/) and [Peloton Liverpool](https://peloton.coop/) communities; now they're in action I've had a chance to get back to a bit of pen plotting (I am going to do a blog post on the lights once I get a few more photos together though, and there's definitely more work to do in the future to take full advantage of the MCQN Ltd "[My Bikes Got LED](https://github.com/mcqn/my-bikes-got-led)" boards that control them).

I don't have any new code to plot at the moment, so thought I'd start off with [DrawingBotV3](https://github.com/SonarSonic/DrawingBotV3) again - I had some photos of this climbing plant that I'd taken back at the beginning of October but hadn't got far with plotting at the time:

![creeper_photo.jpg](https://jackiepease.github.io/assets/weeknotes_20211213/creeper_photo.jpg)


Annoyingly, I had to spend the first day resolving hardware issues: trying to work out why I was getting errors from one of the limit switches (this somehow spontaneously resolved), and replacing the servo. 

This was my first plot of the week, using Sharpies and an InkJoy fineliner:

![sharpies.jpg](https://jackiepease.github.io/assets/weeknotes_20211213/sharpies.jpg)

I was a bit disappointed with the outcome - there's a blue diagonal line across the picture, the thickness of the Sharpie lines against the white background make it difficult to see the image, and the registration is really bad. It felt like I'd forgotten everything I'd learned so far. I've now fixed the registration problem - I'd set up the bar that keeps the cables out of the way so one end was interfering with the pen holder moving back to the origin.

Next I wanted to experiment with refillable ink pens, as I've been shocked by the number of disposable pens I've been getting through. I'd used Rotring technical pens before with Rotring ink but seen on Instagram that some people were using fountain pen ink, which is cheaper and comes in more colours. I set the feedrate to 400 to try to avoid breaking the Rotring nibs (something that's happened before) and this was the output after around 7 hours, using Diamine fountain pen ink in "Ancient Copper" on smooth white card:

![damage_to_paper.jpg](https://jackiepease.github.io/assets/weeknotes_20211213/damage_to_paper.jpg)

Quite a pretty outcome, but this should have been the first colour out of 4, and the surface of the card was already badly shredded. 

Next I tried some Yupo - which is polyester sheet, not paper, and is strong with a very smooth surface. This is the result with Diamine fountain pen ink in "Claret". Hardly any ink is absorbed by the Yupo, leading to a very pale colour. At least there's less chance of the ink running out.

![fountain_pen_ink_yupo.jpg](https://jackiepease.github.io/assets/weeknotes_20211213/fountain_pen_ink_yupo.jpg)

I had a Rotring pen already filled with Rotring-alike ink so I tried that. It came out a lot darker than fountain pen ink, but still not as dark as it would have on paper. Because the picture didn't look finished, I plotted the Magenta layer with the Diamine Claret ink:

![drawing_ink_yupo.jpg](https://jackiepease.github.io/assets/weeknotes_20211213/drawing_ink_yupo.jpg)

Again quite a pretty effect, and this time I managed two layers (the second one took  11 hours), but the Yupo surface was still quite rough and damaged in places:

![completed_yupo.jpg](https://jackiepease.github.io/assets/weeknotes_20211213/completed_yupo.jpg)

![damage_to_yupo.jpg](https://jackiepease.github.io/assets/weeknotes_20211213/damage_to_yupo.jpg)

So what I've learned is that I'm not going to get the sort of super-saturated effects from Rotring pens that I can get from the faster-drying solvent-based ink in Sharpies, although they might be ok for more geometric patterns where there isn't much overlap betweeen lines. I think my next plot will be something like that, and I've also got a couple of fountain pens that I'm going to experiment with. I've been given some disposable pipettes so I can also try cutting off the end of a pen cartridge, putting some pauses in the gcode, and adding different coloured inks as the plot progresses.

On Sunday, I went to [Plastic Tactics](https://plastictactics.com/) Plastic Playgroup, and made some more milk carton petals for a bigger version of these [light up plastic flowers](https://www.instagram.com/p/CTK_ezwsrnH/), another project I'd like to make some progress on:

![petals.jpg](https://jackiepease.github.io/assets/weeknotes_20211213/petals.jpg)

Next to laser cut some more stems from scrap ply, and then add lights...
~                                                                                                                        


