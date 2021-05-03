---
layout: post
title:  "DrawingBotV3 - Plotting without Coding"
date:   2021-05-02 00:00:00 +0100
categories: blogpost
---
This is the pen plotter at DoES Liverpool. It's an A3 laser engraver base with a penholder and servo attached. I've been working on it`for a while now, and have mainly been learning about p5js and using it to produce [geometry-based patterns](https://github.com/JackiePease/p5js-sketches).

![plotter.jpg](https://jackiepease.github.io/assets/plotting_without_code/plotter.jpg)

Recently I've been experimenting with ways people could use the plotter if they didn't want to write code. One interesting piece of software I found is DrawingBotV3, which gives you a wide range of ways to produce interesting effects from bitmap files (inc. jpeg and png).

You can download the software here: [DrawingBotV3](https://github.com/SonarSonic/DrawingBotV3) - it's available for Linux, Windows and Mac, and the installation instructions are in the ReadMe section at the bottom of the page.

Then you just need to find a photo you want to make a picture from, or create your own bitmap file. Here I’ve used Inkscape with a quote (thanks to Ross Dalziel for the quote suggestion):

![ifyourenotangry.png](https://jackiepease.github.io/assets/plotting_without_code/ifyourenotangry.png)

I’ve used a bold font as detail is easily lost in this process, and added a background gradient so there’s something for the algorithm to pick up and so that it isn’t too uniform. I haven’t worried about the actual colours, as these will depend on the pens used when plotting.

Open DrawingBotV3, and from the File tab, choose “Export Settings”. For the plotter we have at DoES Liverpool you need to set the following so that the GCode (instructions sent to the machine) will lift and lower the pen and write in the right direction.

![exportsettings_speedpenuppendown.png](https://jackiepease.github.io/assets/plotting_without_code/exportsettings_speedpenuppendown.png)

I changed the feedrate to F2000 (the default is F8000, which is likely to damage some pens, but it's definitely worth experimenting here)
The pen up and pen down setting will depend on the plotter you're using. Currently I'm using M3 S40 for pen up and M3 S60 for pen down, but again this is subject to experimentation...

![exportsettings_direction.png](https://jackiepease.github.io/assets/plotting_without_code/exportsettings_direction.png)

The x-direction has been changed to Negative to stop the plotter sending a mirror image - this will depend on the plotter, and whatever has been set up in firmware

Then import your picture and set the paper size and orientation.

![ifyourenotangryimport.png](https://jackiepease.github.io/assets/plotting_without_code/ifyourenotangryimport.png)

There’s a whole load of options you can play with. Under “Path Finding Controls” select “Path Finding Module”. In this case I picked "Sketch Lines PFM"

You can also choose the pen settings – they’re not going to mean much unless you’ve got the pens that the program was written for, but might be good to choose a set where it’s easy to work out which pens you’re substituting (if you choose “Special” it gives you an option of CMYK separation, which I’m intending to explore next – could mean buying some more pens...).

Once you’ve chosen the options you want, click “Start Plotting”, you should see a representation of the plot on your screen:

![ifyourenotangryplotted.png](https://jackiepease.github.io/assets/plotting_without_code/ifyourenotangryplotted.png)

When you’re happy with it, choose File → Export Per/Pen → Export GCode File

(if you do it this way, you’ll get one file per colour. I like this as it means you don’t need to plot them all at once).

There are also options for saving to Inkscape, which is useful if you’ve got an Axidraw (Inkscape has its own extension for exporting to GCode).

I use [Universal GCode Sender](https://winder.github.io/ugs_website/download/) to send the GCode files to the plotter (Note: only the "Classic" version works on Linux). There are many other options though, especially if you’ve got a Windows machine…

Load the files in one at a time – DrawingBotV3 default is to start with the darkest – choosing appropriate pen colours and trying to start at the same point each time (I haven’t found the ideal way to do this as yet – some pen plotters have carousels or magnetic attachments that make it easy to load and unload pens).

This photo shows the output of just the first 2 GCode files (which are both black ink):

![ifyourenotangry_blackphoto.jpg](https://jackiepease.github.io/assets/plotting_without_code/ifyourenotangry_blackphoto.jpg)

and this is the final result:

![ifyourenotangry_colourphoto.jpg](https://jackiepease.github.io/assets/plotting_without_code/ifyourenotangry_colourphoto.jpg)

I think I prefer the black and white version though!

I've tried a few other options.

This is "Voronoi Triangulation":

![voronoi_triangulation.jpg](https://jackiepease.github.io/assets/plotting_without_code/voronoi_triangulation.jpg)

It does involve a lot of lifting and lowering of the pen, which is a bit noisy if you’re sharing a room, and is also likely to wear out the servo motor that does the lifting.
   
I used “Sketch Squares PFM” for this house picture from a photo: 

![egerton_st_beige.jpg](https://jackiepease.github.io/assets/plotting_without_code/egerton_st_beige.jpg)

and in blue....     

![egerton_st_blue.jpg](https://jackiepease.github.io/assets/plotting_without_code/egerton_st_blue.jpg)

The detail is really interesting: 

![close_up_squares.jpg](https://jackiepease.github.io/assets/plotting_without_code/close_up_squares.jpg)

I think DrawingBotV3 is a good starting point for pen plotting - thanks to the developers. There's lots to experiment with in terms of input files, options within the program, and pen and paper choices, then you can go on to think about coding if that's what you want to do.
