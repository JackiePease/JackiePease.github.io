---
layout: post
title:  "Week Notes - All The Pens"
date:   2022-05-01 16:00:00 +0100
categories: weeknotes
---

Having done some maintenance on the pen plotter last month, I've mainly been experimenting with different pens and papers to see what effects they produce. I am aiming to use more refillable pens, but having been asked to produce a flower picture in the style of one of my earlier pen plots, it's been more Sharpies, fineliners and gel pens recently.

I forgot to take photos of that picture before handing it over, unfortunately - one issue was that the sky in the background was quite light and came out uncoloured in the plot, which was a strong contrast to areas which were heavily filled with Sharpie and Uniball Eye fineliner.

I also had problems knowing how long pens would last, particularly Sharpies, and trying to guess where to restart the gcode from once one had run out was leading to doubled lines and missed areas. As a test, I plotted this picture (approx. A5) repeatedly until the red pen ran out, so now I know it'll do about 2.5 of those (I like the version with less red ink best though). These also include a bit of experimenting with [Pentel Hybrid Dual Metallic Gel Pens](https://www.pentel.co.uk/product/pentel-hybrid-dual-metallic-gel-pen-k110/). My main conclusion is that although pretty, you need to go over the lines twice to get a good result and that uses nearly a whole pen for this size, so a bit expensive for this application.

![sharpie_testing.jpg](https://jackiepease.github.io/assets/weeknotes_20220501/sharpie_testing.jpg)

I plotted the original picture on Pergamino paper, and I think the texture of the paper and the fact that Sharpie ink doesn't soak into it as much makes this more successful.

![roses_on_pergamino.jpg](https://jackiepease.github.io/assets/weeknotes_20220501/roses_on_pergamino.jpg)


It's all been [DrawingBotV3](https://github.com/SonarSonic/DrawingBotV3) and photos this month - the next thing I did was to produce a card for a friends new baby, Laelia. As I discovered from Wiki, a Laelia is a type of orchid, so I downloaded this [photo](https://commons.wikimedia.org/wiki/Laelia_rubescens#/media/File:Laelia_rubescens_Orchi_038.jpg) of a Laelia Rubescens from Wiki commons and processed it with DrawingBotV3 Sobel Edges option. Some of my preprocessing decisions I regretted a bit afterwards, like dialling up the saturation to get rid of the lovely white in the flower because I was worried about having uncoloured areas in the final plot - maybe it would have worked ok like that.

Original photo by [https://commons.wikimedia.org/wiki/user:Orchi](https://commons.wikimedia.org/wiki/user:Orchi): 

![Laelia_rubescens_Orchi_038.jpg](https://jackiepease.github.io/assets/weeknotes_20220501/Laelia_rubescens_Orchi_038.jpg)


This was the result, plotted on Fabriano Disegno 4 paper, using Sharpies and a [0.1mm Unipin fineliner](https://www.cultpens.com/i/q/UN02216/uni-pin-drawing-pen-black):

![orchid_card.jpg](https://jackiepease.github.io/assets/weeknotes_20220501/orchid_card.jpg)


I then tried the same gcode with a Unipin plus some Marabou Creabox watercolour pens from Lidl. I was expecting a nice line and wash effect - the Unipin has "Water and Fade Proof" printed on the barrel, and the website claims "Solid, pigment ink line can easily be used with watercolour as the ink will not smudge when wet". However it didn't stand up to a couple of hours of pen plotting (the paper did though, which is progress!). I do like the result - it reminds me of Batik:

<blockquote class="twitter-tweet"><p lang="en" dir="ltr">Pen plot created using <a href="https://twitter.com/hashtag/drawingbotv3?src=hash&amp;ref_src=twsrc%5Etfw">#drawingbotv3</a> Sobel Edges option. The black pen was supposed to be waterproof but didn&#39;t stand up to this - all good though<a href="https://twitter.com/hashtag/weeknotes?src=hash&amp;ref_src=twsrc%5Etfw">#weeknotes</a> <a href="https://twitter.com/hashtag/happyaccident?src=hash&amp;ref_src=twsrc%5Etfw">#happyaccident</a> <a href="https://t.co/V5wgrgOzIg">pic.twitter.com/V5wgrgOzIg</a></p>&mdash; Jackie Pease (@jackie_pease) <a href="https://twitter.com/jackie_pease/status/1508213445367377921?ref_src=twsrc%5Etfw">March 27, 2022</a></blockquote> <script async src="https://platform.twitter.com/widgets.js" charset="utf-8"></script>

One more experimient with the orchid gcode - I plotted on the reverse of some photo paper with Marabou Creabox Sketch Pens, also from Lidl. I don't like the result as a whole but there are some interesting parts. In general the first layer comes out fainter than on normal paper e.g. the pink areas, but where there is more than one colour in a region the new ink tends to push the previous one around. Not good for reproducing what's in the photo, but could work for something more abstract:

![alcohol_on_photo_paper.jpg](https://jackiepease.github.io/assets/weeknotes_20220501/alcohol_on_photo_paper.jpg)

Here's a detail:

![photo_paper_detail.jpg](https://jackiepease.github.io/assets/weeknotes_20220501/photo_paper_detail.jpg)


Then it was on to another photo-based plotting project. I took a bike ride along to Westminster Road to take photos of this [historic former police/fire station](https://historicengland.org.uk/listing/the-list/list-entry/1392283): 

![westminster_road.jpg](https://jackiepease.github.io/assets/weeknotes_20220501/westminster_road.jpg)

![westminster_road_bird.jpg](https://jackiepease.github.io/assets/weeknotes_20220501/westminster_road_bird.jpg)

And then I started plotting from them (DrawingBotV3 SobelLines and Sketch Squares options).

This plot was with [Uniball Eye pens](https://www.cultpens.com/i/q/UN00907/uni-ball-eye-rollerball-pen-ub-157) (blue and pink), 0.1mm Unipin fineliner (dark grey) and 0.3mm Rotring pen with yellow Diamine ink(as the only other yellow pens I had were Sharpies). I love the way the sky has turned out, but the building shouldn't look as grey. The Uniball Eye pens are very fine so often last for a couple of prints. 

![fire_station_portrait.jpg](https://jackiepease.github.io/assets/weeknotes_20220501/fire_station_portrait.jpg)


I increased the amount of red using the DrawingBotV3 preprocessor and tried again, using these [Uni-ball On Point One Dream Gel Pens](https://www.cultpens.com/i/q/UN86996/uni-ball-on-point-one-dream-gel-pen-3-pack) - expensive, but they do claim to be fade proof and this 3 pack actually has a useful colour range:

![uniball_one.jpg](https://jackiepease.github.io/assets/weeknotes_20220501/uniball_one.jpg)

I used a 0.1mm dark grey Unipin as key, but it ran out so I went over it with 0.5mm. It doesn't look as pretty but the result is easier to read ( 0.5mm was specified in DrawingBotV3):
![fire_station_square.jpg](https://jackiepease.github.io/assets/weeknotes_20220501/fire_station_square.jpg)

Here's a couple of plots I did of the Liver Bird on the corner of the building, firstly in the Uni-ball Ones plus a UniPin 0.5mm in dark grey, then in black and light grey 0.5mm Unipins:

![Bird_triangles.jpg](https://jackiepease.github.io/assets/weeknotes_20220501/Bird_triangles.jpg)

![Bird_greyscale.jpg](https://jackiepease.github.io/assets/weeknotes_20220501/Bird_greyscale.jpg)

The light grey Unipin didn't seem to have the same quality of ink as the black one, and the tip seemed to deteriorate during the plot (also the grey pen must have been knocked during plotting ...).

I do have a few non-pen plotter related things to mention (it has been about 6 weeks since my last blog post after all).

[Snoof](https://www.instagram.com/robotorium/) showed us how to make these paper flowers at DoESLiverpool [makerday](https://doesliverpool.com/maker-events/):

<blockquote class="twitter-tweet"><p lang="en" dir="ltr">Some of the flowers that I (and others) made at <a href="https://twitter.com/Robotorium?ref_src=twsrc%5Etfw">@Robotorium</a> impromptu paper flower tutorial yesterday <a href="https://twitter.com/DoESLiverpool?ref_src=twsrc%5Etfw">@DoESLiverpool</a> makerday - thanks Snoof!<a href="https://twitter.com/hashtag/weeknotes?src=hash&amp;ref_src=twsrc%5Etfw">#weeknotes</a> <a href="https://t.co/LVA8ZoyJeV">pic.twitter.com/LVA8ZoyJeV</a></p>&mdash; Jackie Pease (@jackie_pease) <a href="https://twitter.com/jackie_pease/status/1513047444786974720?ref_src=twsrc%5Etfw">April 10, 2022</a></blockquote> <script async src="https://platform.twitter.com/widgets.js" charset="utf-8"></script>

I started looking into making something sparkly for summer using waste plastics at [Plastic Tactics](https://plastictactics.com/) Plastic Playgroup:

<blockquote class="twitter-tweet"><p lang="en" dir="ltr">Prototype &quot;sashiko&quot; in crisp packet &quot;plarn&quot; on ironed-together plastic bags with laser-cut holes. <a href="https://twitter.com/PixiesInSpace?ref_src=twsrc%5Etfw">@PixiesInSpace</a>, who did the sewing, said it made her hands hurt though, so I need to think of some improvements before Sunday afternoon&#39;s <a href="https://twitter.com/plastacs?ref_src=twsrc%5Etfw">@plastacs</a> <a href="https://twitter.com/hashtag/plasticplaygroup?src=hash&amp;ref_src=twsrc%5Etfw">#plasticplaygroup</a>. <br>Ideas welcome! <a href="https://t.co/0ieCpkrbFE">pic.twitter.com/0ieCpkrbFE</a></p>&mdash; Jackie Pease (@jackie_pease) <a href="https://twitter.com/jackie_pease/status/1517123059924324353?ref_src=twsrc%5Etfw">April 21, 2022</a></blockquote> <script async src="https://platform.twitter.com/widgets.js" charset="utf-8"></script>

Also for Plastic Playgroup, I talked a bit about making the Plastic Flowers in this radio clip (worth listening to for [Arthur's](https://twitter.com/arthrowl) explanation of why he set up Plastic Tactics and what he hopes people will get from it:

<blockquote class="twitter-tweet"><p lang="en" dir="ltr">Here&#39;s the clip, and a pic of the award we made, for those who couldn&#39;t listen live to the <a href="https://twitter.com/bbcmerseyside?ref_src=twsrc%5Etfw">@bbcmerseyside</a> piece by <a href="https://twitter.com/chamiltonbbc?ref_src=twsrc%5Etfw">@chamiltonbbc</a> about their experience at the <a href="https://twitter.com/hashtag/PlasticPlaygroup?src=hash&amp;ref_src=twsrc%5Etfw">#PlasticPlaygroup</a><a href="https://t.co/nBRo2QbRoz">https://t.co/nBRo2QbRoz</a> <a href="https://t.co/J0VTNnvaM9">pic.twitter.com/J0VTNnvaM9</a></p>&mdash; Plastic Tactics (@plastacs) <a href="https://twitter.com/plastacs/status/1519282787731263489?ref_src=twsrc%5Etfw">April 27, 2022</a></blockquote> <script async src="https://platform.twitter.com/widgets.js" charset="utf-8"></script>

Speaking of the Plastic Flowers, [Michael Dales](https://www.mynameismwd.org/) took a really good photo on a recent visit to DoES Liverpool:

![md_plastic_flowers.jpg](https://jackiepease.github.io/assets/weeknotes_20220501/md_plastic_flowers.jpg)


And finally, on this Friday's [Peloton Liverpool](https://twitter.com/pelotonliv) ride, we got the chance to find out more about the work of [Wheels for All Merseyside](https://wheelsforall.org.uk/) and try out some of their bikes:

<blockquote class="twitter-tweet"><p lang="en" dir="ltr">A pleasure joining up with <a href="https://twitter.com/PelotonLiv?ref_src=twsrc%5Etfw">@PelotonLiv</a> last night. Lovely to have a ride together with some of our inclusive cyclists, and to show the group what we do every day of the week across Merseyside <a href="https://t.co/7yrPDvWb64">https://t.co/7yrPDvWb64</a></p>&mdash; Wheels for All Merseyside (@WFAMerseyside) <a href="https://twitter.com/WFAMerseyside/status/1520431809263280128?ref_src=twsrc%5Etfw">April 30, 2022</a></blockquote> <script async src="https://platform.twitter.com/widgets.js" charset="utf-8"></script> 
