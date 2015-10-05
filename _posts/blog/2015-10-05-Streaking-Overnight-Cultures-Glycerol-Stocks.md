---
layout: post
title:  "Week 7. Streaking, Overnight Cultures, and Glycerol Stocks"
date:   2015-10-05 08:00:00
author: Maxwell Ng
categories: 
- blog

img: Week-7-header.png
thumb: Week-7-thumb.png
---

#Week 7: Ligations (gels not included)

Welcome back to the [A Fledgling’s Guide to Cell Bio](http://mcmastergem.com/blog/)! And yes, it’s an odd week and [I'm](mailto:ngmc2@mcmaster.ca) back from the [Jamboree](https://www.flickr.com/photos/igemhq/albums)! There will be a complete blog post on the Jamboree in the coming weeks, but for now here’s a few sneak peek images:

![oh, so you've found the hidden text?](https://scontent-ord1-1.xx.fbcdn.net/hphotos-xta1/t31.0-8/12132642_10207808975926151_6011806608972103809_o.jpg){: .center-image .responsive-image }

![well well well then](https://scontent-ord1-1.xx.fbcdn.net/hphotos-xpa1/t31.0-8/12028854_10207808975806148_1045004629709928728_o.jpg){: .center-image .responsive-image }

![what shall we do then?](https://scontent-ord1-1.xx.fbcdn.net/hphotos-xat1/t31.0-8/12045774_10207808975686145_4145425591676623118_o.jpg){: .center-image .responsive-image }


But now then, let us go forth unto the science!

To start, what are ligations? Well, ligation is an old-old [word](http://www.etymonline.com/index.php?term=ligation) that essentially means to join two things together. In the context of synthetic biology, we will be focusing here on joining two pieces of DNA together. This will allow to create longer genetic sequence, and (eventually) create our desired plasmid. For the mGEM 2015 project, we proposed 3 different plasmids that would work in conjunction, as shown below.

![hmmmmm](https://scontent-ord1-1.xx.fbcdn.net/hphotos-xtp1/t31.0-8/s2048x2048/12132449_10207808978046204_8419097713026192243_o.jpg){: .center-image .responsive-image }


Each plasmid involves the ligation of several genetic sequences. It is clear that a solid grasp of ligation is therefore key to synthetic biology.

To start, we will have a short re-cap of digestion. During digestion, the ends of the DNA sequences were cut into ‘sticky ends’. This allows the DNA strands to re-combine with different DNA strands, if the sticky ends of each strand is compatible. We will be using the 3A Assembly method, which allows the ligation of three different pieces of DNA together, in a specific order. 

As shown in the diagram below, we have digested three pieces of DNA. The first one (blue gene) has been digested at its E (EcoRI) and S (SpeI) sites. The second one (green gene) has been digested at its X (XbaI) and P(PstI) sites. The third one (antibiotic resistance backbone) has bee digested at its E (EcoRI) and P (PstI) sites.

![well I guess we should start with introductions](https://scontent-ord1-1.xx.fbcdn.net/hphotos-xap1/v/t1.0-9/12143140_10207808975646144_516326962580001567_n.jpg?oh=cd7b83dad2138d4c655753847296dd76&oe=56D248AC){: .center-image .responsive-image }
Diagram from [iGEM](http://parts.igem.org/Help:Assembly/3A_Assembly)

As the diagram says, we then mix the DNA parts together (don’t worry, more detail on this later on in this post!). The DNA parts then ligate together. Naturally, the two E sites (one from blue and from backbone) will preferably bind with each other, as they have the same sticky ends (as shown below). Similarly, the two P sites (green and backbone) will join with each other.


![Hi, I'm the image guy](https://www.addgene.org/static/data/easy-thumbnails/filer_public/cms/filer_public/83/bc/83bc9c5f-077e-4bdf-8a39-0bcc57e83e9e/restrictiondigest_2.png__400x300_q85_crop_subsampling-2_upscale.png){: .center-image .responsive-image }
Diagram from [AddGene](https://www.addgene.org/plasmid-protocols/restriction-digest/)
 
However (and this is where the magic happens) a special ligation occurs between the blue gene’s S site and the green gene’s X site. Even though they are not the exact same sticky ends, the S site can join with the X site, forming a scar site (M). This M site cannot be digested with the E, S, X, or P enzymes that we use, thereby making this ligation ‘permanent’. This is great because we can now repeat the 3A Assembly ligation method under the assumption that the blue-green genes act as a single entity (cannot be split apart, are flanked by common cut sites).

Now then, the 3A Assembly molecular process we just went over might be a bit of a doozy, so we’re going to explore our ligation protocol by starting with something simple: Red Fluorescent Proteins (RFPs).

#Ligation


Here all we are ligating together is a gene for RFPs and 2 backbones. Taking 2 tubes, we add 2µL of digested backbone in each. Add 3µL of RFP gene to each. Then, add 1µL of T4 DNA ligase reaction buffer, and 0.5µL of T4 DNA ligase. Incubate at room temperature for 1 hour, and then heat kill the enzymes at 80°C for 20 minutes. Then your ligations are complete, and you now have a complete plasmid! It is important that you verify your ligated products on a [gel](http://mcmastergem.com/blog/2015/09/28/gelception/) If the ligated products is messy, it’s extremely advised that you do a gel extraction to get your plasmids and not anything else that could interfere with future steps. You can store the DNA in the -20°C freezer, or (if you have time in your lab day) start moving onto the next steps (sequencing and transformation).

Since we used RFPs, once transformed, under specific light the bacteria with our plasmid will grow red. However, these RFPs are special in that they appear red even under normal light. This way have get two things: 1) a quick method of verifying that our plasmid was completed properly (and taken up by the bacteria), and 2) a really nifty set of tubes and pictures!

![How are you? Not many people come 'round here.](https://scontent-ord1-1.xx.fbcdn.net/hphotos-xat1/t31.0-8/12079985_10207808975606143_1012495833270279487_o.jpg){: .center-image .responsive-image }


![Well I have to go now, but I'll see you later!](https://scontent-ord1-1.xx.fbcdn.net/hphotos-xpa1/t31.0-8/12087835_10207808977806198_5064582737236344731_o.jpg){: .center-image .responsive-image }


#Further Protocols

Now that you’ve seen the simple ligation, you’re ready for the 3A Assembly method! The full protocol can be found on the [iGEM website here](http://parts.igem.org/Help:Protocol/3A_Assembly)
 
That’s all for now, fledglings!I want to finish by saying that the ligation methods presented here are only a few of the many ways that ligations can be accomplished! If you’re interested, I highly recommend that you explore other methods such as Gibson Assembly [] and  Golden Gate Assembly [].

####Have an excellent week and come back again soon for Fei Fei’s post on Sequencing (oooooooh!)!####