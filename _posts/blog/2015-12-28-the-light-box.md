---
layout: post
title:  "The Light Box"
date:   2015-12-28 08:00:00
author: Maxwell Ng
categories: 
- blog

img: Week-15-header.png
thumb: Week-15-thumb.png
---


#Week 15: The Light Box

######mGEM Special

Here we are at the end of our mGEM 2015 blog series! It's been an interesting journey, and so we're going to leave it off with something a bit different. 

###A box.

Oh yes, it's been said many times to "think *OUTSIDE* the box", but let's take a moment now to think *ABOUT* the box.

What are we doing? We are doing science, a field which modifying the genetic code of microorganisms as a method of creating new and desirable functions. However, science is much broader than just synthetic biology. To name just some of the basics, science involves the larger context of biology, as well as chemistry and physics. What is even more interesting is that none of these fields necessarily stand apart. They are all interconnected and even rely on each other, with the introduction of fields such as astrobiology, biochemistry, and chemical engineering, to name a few.

So in this post, we're going to look at an example of how to combine various fields - notably, engineering and biology - to create something new (aside from synbio).

##1. The Plan

As a quick summary, for 2015, the McMaster iGEM team designed plasmids that could allow *E. coli* bacteria to respond to multichromatic light. More specifically, red light would cause the cells to produce a protein of interest, after which a green light could be used to biologically lyse the cells. If you want to learn more, you can go to our [wiki page](http://2015.igem.org/Team:Hamilton_McMaster).

Now for the nitty-gritty. The specific light sensors used are responsive to only certain wavelengths of light. Specifically, red 650nm and green 535nm. These were therefore the wavelengths of light that needed to be lit over the cells.

So the plan from here was straightforward. We needed a box that would shut out all exterior light to avoid accidental activation of the cell's sensors. All this would need to be integrated with a shaker inside an incubator. Solution? Place the incubator inside the sealed box, and the box inside the incubator.

Inside the box, there needs to be two sets of lights: red and green. Each can be achieved through LED strips with narrow bandpass filters (only allows a specific region of wavelengths to pass through). These would then be connected to a circuit, using switches and an optical density (OD) sensor or timer. This OD sensor or timer would allow the system to be completely automated.

This all culminated into the circuit below by Sachin Doshi:

![circuit diagram](https://scontent-ord1-1.xx.fbcdn.net/hphotos-xpl1/v/t1.0-9/10615548_10208323017216862_4479876350363645670_n.jpg?oh=f182e989654efa0359812d1715e82bc7&oe=57004C01){: .center-image .responsive-image }

#####Circuit

This circuit allows the system to be turned on or off, and to have only either red light or green light.

##2. The Prototyping

An excellent rule when building new things: **prototype fast!** It doesn't matter if it's clean or perfect - as long as the general concept and functionality is there, the prototype is a success. It's best to try things out when the price of failure is still low, e.g. before building an entire light box only to find a simple yet overlooked flaw. Hence, using some spare and salvaged parts, we quickly created this simple demonstration:

#####OFF

![desk image](https://scontent-ord1-1.xx.fbcdn.net/hphotos-xft1/t31.0-8/10658719_10208323076578346_8072286203587692057_o.jpg){: .center-image .responsive-image }

#####RED

![desk image](https://scontent-ord1-1.xx.fbcdn.net/hphotos-xlf1/t31.0-8/462335_10208323076818352_7701302357235738904_o.jpg){: .center-image .responsive-image }

#####GREEN

![desk image](https://scontent-ord1-1.xx.fbcdn.net/hphotos-xtl1/t31.0-8/12418826_10208323076738350_6554713358346953052_o.jpg){: .center-image .responsive-image }

The alumnium would be used to increase reflectivity inside the box, if there was not enough LEDs available to cover the walls entirely.

##3. The Renders

As it turned out we didn't need the box, so its outer shell was never constructed. However, it's always good to create some visuals to gain a better understanding of how something might truly be. A simulation of sorts. So using the animation software [Blender 3D] (https://www.blender.org) - *which I highly recommend for anyone interested in the world of 3D animation!* - I created the sequence of images below:

#####OFF

![3 render sequence](https://scontent-ord1-1.xx.fbcdn.net/hphotos-xft1/t31.0-8/702001_10208323029697174_5120603171725355292_o.jpg){: .center-image .responsive-image }

First the tubes containing the transformed cells are added to the light box, with the light box inactive. Then, with the light in the room turned off, the cells can be activated using a chemical activator.

#####RED

![3 render sequence](https://scontent-ord1-1.xx.fbcdn.net/hphotos-xta1/t31.0-8/10631152_10208323026977106_7844939409339675419_o.jpg){: .center-image .responsive-image }

First the red light is turned on to enhance the production of the protein of interest by the transformed bacteria.

#####GREEN

![3 render sequence](https://scontent-ord1-1.xx.fbcdn.net/hphotos-xaf1/t31.0-8/1534690_10208323024777051_255188811446628948_o.jpg){: .center-image .responsive-image }

Once enough of the protein has been produced, the lights switch to green (either by an OD sensor or by calculated time delay from initial experiments). After sufficient time for a the cells to be lysed, the solution can be retrieved, purified, and the protein extracted!

---------------

#The End?

Thank you for following our series! We've had a great time making these, and we hope you've had a great time reading them! If you want to see more, there is a summary list at the bottom of this post!

So, is this it? Is this the end of the mGEM blog, [A Fledgling’s Guide to Cell Bio](http://mcmastergem.com/blog/)?

No, of course not! We are still learning, and always will be! This is only the end of the first blog series, and you can be sure that there will be another! We'll post [here on our website](http://mcmastergem.com), on our [Facebook page](https://www.facebook.com/igemmcmaster), and on our [Twitter feed](https://twitter.com/igem_mcmaster), when that time comes.

But for now, I suppose it's time to bid a farewell! From Fei Fei and I, and the whole mGEM team, we hope you have a great and happy New Year!

*We hope to see you then!*

------------

##Review of Phase 1

**Week 1 - Lab Preparation:**
[Preparing the lab (for science!)](http://mcmastergem.com/blog/2015/08/24/week-1-preparing-the-lab/) with Max

**Week 2 - Transformations:** [Transform! - The Magical World of Transformations](http://mcmastergem.com/blog/2015/08/31/the-magical-world-of-transformations/) with Fei Fei

**Week 3 - Making Cultures:** [Controls, Streaking, Overnight Cultures, and Glycerol Stocks](http://mcmastergem.com/blog/2015/09/07/streaking-overnight-cultures-and-glycerol-stocks/) with Max

**Week 4 - Miniprep:** [Miniprep! The E. coli Go to a Happier Place...](http://mcmastergem.com/blog/2015/09/14/e-coli-go-to-a-happier-place/) with Fei Fei

**Week 5 - Digestion:** [Digestion (not the eating kind!](http://mcmastergem.com/blog/2015/09/21/digestion-not-the-eating-kind/) with Fei Fei

**Week 6 - Gel Extraction:** [Gels - Proper Experimental Design, or Just Confusing?](http://mcmastergem.com/blog/2015/09/28/gelception/) with Fei Fei

**Week 7 - Ligation:** [Ligations (gels not included)](http://mcmastergem.com/blog/2015/10/05/Ligations-gels-not-included/) with Max

**Week 8 - Sequencing:** [The Sequence Matters!](http://mcmastergem.com/blog/2015/10/12/The-Sequence-Matters/) with Fei Fei

**Week 9 - Review of Phase 1:** [Phase 1, Complete!](http://mcmastergem.com/blog/2015/10/19/phase-one-complete/) with Max

##Review of Phase 2

**Week 10 - PCR Primer Designs:** [A Primer for Primer Design](http://mcmastergem.com/blog/2015/11/02/a-primer-for-primer-design/) with Fei Fei

**Week 11 - PCR Cycles:** [PCR Cycles](http://mcmastergem.com/blog/2015/11/09/pcr-cycles/) with Max

**Week 12 - PCR Mix:** [PCR Mix - The Secret Sauce](http://mcmastergem.com/blog/2015/11/23/the-secret-sauce/) with Max

**Week 13 - PCR Cleanup:** [PCR Cleanup](http://mcmastergem.com/blog/2015/11/30/pcr-cleanup/) with Max

**Week 14 - Troubleshooting:** [Troubleshooting: Did You Try Turning it Off and then On again?](http://mcmastergem.com/blog/2015/12/07/troubleshooting-did-you-try-turning-it-off-and-on/) with Fei Fei

**Week 15 - Interdisciplinary Science:** [The Light Box](http://mcmastergem.com/blog/2015/12/28/the-light-box) with Max
