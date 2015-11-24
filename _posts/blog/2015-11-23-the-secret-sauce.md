---
layout: post
title:  "PCR Cycles"
date:   2015-11-23 08:00:00
author: Maxwell Ng
categories: 
- blog

img: Week-12-header.png
thumb: Week-12-thumb.png
---


#Week 12: PCR Mix - The Secret Sauce

######Note: Do Not Injest!

Surprise! While usually Fei Fei takes the even weeks, I'm going to be here to take you through the rest of [PCR](https://www.youtube.com/watch?v=x5yPkxCLads) (this week and next week)! 

[Last week](http://mcmastergem.com/blog/2015/11/09/pcr-cycles/) we talked about programming and calculating your PCR cycles. We went through initialization, denaturing, extension, annealing, and storage. Now we're going to put it into practice!

##1. Choose the ingredients

As with any good recipe, ingredients must be thought of well ahead of time. PCR is no different, although we recommend not actually eating of these materials (although there [ARE sciency foods that you and your friends can enjoy](http://www.thekitchn.com/phd-in-delicious-the-science-c-108963) - yum!).

For mGEM, we used a Platinum PCR SuperMix High Fidelity (Thermo Fischer). Aside from the template DNA and your primers, these PCR mixes contain everything necessary for the chemical reaction of PCR, including *Taq* polymerase, buffer, and dNTPs (dNTP = deoxy-nucleoside triphosphate, which constitute the building blocks for the DNA nucleotides). Although you can make [your own PCR mix from a recipe](https://www.neb.com/protocols/1/01/01/protocol-for-a-routine-taq-pcr-reaction) for ~$200 cheaper, it is recommended to use a PCR mix. Manufactured mixes have been tested, may have high-fidelity polymerases (more accurate DNA cloning), and are less likely to cause you problems and delays for troubleshooting. 

![supermix](https://scontent-ord1-1.xx.fbcdn.net/hphotos-xpf1/t31.0-8/12239218_10208091002616642_4045265327528594678_o.jpg){: .center-image .responsive-image }

##2. Blending the solution


**Before we start, a reminder: Keep the solutions on ice! Enzymes should be thawed minimally, as too many freeze-thaw cycles can reduce their efficiency.**

Now, to start, we need to attain the correct ingredient concentrations. The goal is to have primer concentrations between 100nM-500nM concentrations, and between 1ng-200ng of template DNA. To do this we diluted some of our samples, as follows:

	Dilute primers 10x (1µL primer + 9µL nuclease-free water)
	Dilute DNA 20x (1µL DNA + 19µL nuclease-free water)

We diluted our samples because too high a concentration will interfere with the PCR reaction, making it less efficient and a lower yield. Now, using the PCR SuperMix, we used:

	2.0µL		Template DNA
	2.5µL		Forward primer
	2.5µL		Reverse primer
	43µL		PCR SuperMix
	All into a PCR tube
	
This reaction is for a 50µL PCR reaction, and for our specific producer (many actually add nuclease-free water to the mix as well, since their PCR Mix is more concentrated). There are PCR protocols attached to your PCR mix as well as online (in case you lose your papers, though you should keep a copy safe in your lab notebook).

![tube](https://scontent-ord1-1.xx.fbcdn.net/hphotos-xpf1/t31.0-8/12247905_10208091002656643_1373393575106923614_o.jpg){: .center-image .responsive-image }

##3. Place it in the oven

Now you can put your samples back in the 4°C freezer for storage, and place your PCR tube into the thermal cycler. Following [last week's protocols](http://mcmastergem.com/blog/2015/11/09/pcr-cycles/), for either standard or overhang PCR, we can input our necessary temperatures, durations, and cycles.

![machine](https://scontent-ord1-1.xx.fbcdn.net/hphotos-xfp1/t31.0-8/12303928_10208091002576641_8340500722028334979_o.jpg){: .center-image .responsive-image }


######Example: RFP Backbone

######Linearized backbones are essential for the plasmids we create. They contain the antibacterial resistance required to select those bacteria that actually have our desired plasmid. For example, we want a linear backbone that contains Chloramphenicol resistance. The red-fluorescent protein (RFP) in the backbone gives us a visual clue as well for when bacteria are successfully proliferating with this plasmid. Using a RFP plasmid that also has this resistance, we can amplify this gene directly through PCR. Therefore, we follow the previous protocols to form our solution and our cycles. A note that might not have come out clearly form last week: If the template DNA is 2.5kb long, we will use 2.5 minutes for extension time. This has two purposes: (i) it provides enough time for the polymerase to add nucleotides for the entire length of the gene of interest (from template DNA), but (ii) it also keeps the extension period short enough so that we don't create extremely long strands of DNA past the gene of interest for no purposeful reason, and this wastes time, resources, and can make the PCR reaction less efficient.

![diagram](https://mnggraphics.files.wordpress.com/2015/11/screen-shot-2015-11-09-at-11-14-37-pm.png){: .center-image .responsive-image }

####That’s all for this week!
Come back next week when we finalize the PCR procedure! If you have a question or comment, leave us a message below! We'll see you next week!