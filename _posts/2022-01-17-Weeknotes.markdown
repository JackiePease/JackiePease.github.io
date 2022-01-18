---
layout: post
title:  "MonthNotes - Progress with the Plastic Flowers"
date:   2022-01-17 19:00:00 +0100
categories: weeknotes
---
I thought I'd slightly sabotaged my pen plotting project recently by getting qualms about the number of disposable pens I was getting through, but trying out various reusable alternatives instead is proving just as interesting. I've done more with the Rotring technical pens and Lamy fountain pens which I had already, and I've bought [Pilot Parallel Pens](https://www.cultpens.com/i/q/PL01289/pilot-parallel-pen).

One problem I've had is that finer pens (and water based ones) tend to dig up the paper. It looks as if you just can't use more than 2 - 3 layers, but I've also ordered some tougher paper. This might be followed by some new ink, as only some are properly permanent - Rev Dan Catt mentions Noodler's Bulletproof in this Instagram [post](https://www.instagram.com/p/CYj10z4tQ1a/).

Here's some of the output. The first 2 are based on this Andy Wallace [tweet](https://twitter.com/Andy_Makes/status/1470549299020943360?s=20) and this Keith Peters [blog post](https://www.bit-101.com/blog/2017/10/flow-fields-part-i/) and plotted in technical pen on card and calligraphy paper respectively. The card has been badly dug up. The calligraphy paper did better, although the blue ink stopped flowing half way through the second part for some reason, and the lines are a bit wobbly:

![circles_plot.jpg](https://jackiepease.github.io/assets/monthnotes_20220117/circles_plot.jpg)
![bit101-flowfields.jpg](https://jackiepease.github.io/assets/monthnotes_20220117/bit101-flowfields.jpg)

When the Pilot pen arrived I didn't have anything ready to plot, except a dxf grid for the plastic flowers. I wrote a bash script to convert it to gcode using vPype, Juicy GCode and the vpype-dxf extension:

```bash
for x in $@
do
   f=$(echo "$x" | cut -f 1 -d '.')
   echo $f
   vpype dread $f.dxf scaleto -f 250mm 250mm linesort write \
           --page-size a3 --landscape --center $f-out.svg
   vpype read $f-out.svg ldelete 2 write $f-out2.svg
   juicy-gcode $f-out2.svg -f flavor.txt -o $f.gcode
done
```

The pen worked really well on cartridge paper with a lovely smooth red (there's some Sharpie on there too - I need to use them up!):

![pilot_pen_on_cartridge_paper.jpg](https://jackiepease.github.io/assets/monthnotes_20220117/pilot_pen_on_cartridge_paper.jpg)

On calligraphy paper it was less smooth, but still a nice effect:

![pilot_pen_on_calligraphy_paper.jpg](https://jackiepease.github.io/assets/monthnotes_20220117/pilot_pen_on_calligraphy_paper.jpg)
~                                                                                                                        
I've had to take a break from pen plotting to make progress on the Plastic Flowers, which were cluttering up Room 29 at DoES Liverpool. In order to fill the light fitting / vase, I need 40ish flowers so laser cutting stems and hand cutting and heat pressing milk carton petals has taken a while. This week I've been lucky to have help from Sanna King and Mike Gorman, with assembly and soldering, so progress has been a lot quicker than it would have been otherwise: 

<blockquote class="twitter-tweet"><p lang="en" dir="ltr">Lots of thanks to <a href="https://twitter.com/sanna_king?ref_src=twsrc%5Etfw">@sanna_king</a> (shown)and Mike G for helping me with my light up up plastic flowers this week. <br>&#39;Only&#39; the wiring to go now. Hopefully it will be finished soon!<a href="https://twitter.com/hashtag/weeknotes?src=hash&amp;ref_src=twsrc%5Etfw">#weeknotes</a> <a href="https://t.co/bU70S1Pr8M">pic.twitter.com/bU70S1Pr8M</a></p>&mdash; Jackie Pease (@jackie_pease) <a href="https://twitter.com/jackie_pease/status/1482844377131241479?ref_src=twsrc%5Etfw">January 16, 2022</a></blockquote> <script async src="https://platform.twitter.com/widgets.js" charset="utf-8"></script> 

The Peloton disk lights I've been working on recently have been deployed successfully on 3 occasions now, including this Peloton Liverpool trip to Kirby:

<blockquote class="twitter-tweet"><p lang="en" dir="ltr">Lovely <a href="https://twitter.com/PelotonLiv?ref_src=twsrc%5Etfw">@PelotonLiv</a> Friday night <a href="https://twitter.com/hashtag/joyride?src=hash&amp;ref_src=twsrc%5Etfw">#joyride</a> to Kirby to visit <a href="https://twitter.com/cultureKnowsley?ref_src=twsrc%5Etfw">@cultureKnowsley</a> light installation <a href="https://twitter.com/hashtag/aqualux?src=hash&amp;ref_src=twsrc%5Etfw">#aqualux</a> <a href="https://t.co/DRcTuXQvaG">pic.twitter.com/DRcTuXQvaG</a></p>&mdash; Jackie Pease (@jackie_pease) <a href="https://twitter.com/jackie_pease/status/1482262962219978754?ref_src=twsrc%5Etfw">January 15, 2022</a></blockquote> <script async src="https://platform.twitter.com/widgets.js" charset="utf-8"></script> 

Unfortunately there's been a slight issue, obvious in this photo of Arthur at that ride. The light disks were attached to wooden spacers and those were attached to the backs with carpet tape... This issue didn't show up in the earlier sets until they'd been in use for a couple of weeks. So I think I'm going to be gradually going through all the sets if and when they fail, using a scalpel to prise apart the VHB tape round the edges, and replacing the wood and carpet tape with acrylic and VHB ...

![arthur.jpg](https://jackiepease.github.io/assets/monthnotes_20220117/arthur.jpg)

