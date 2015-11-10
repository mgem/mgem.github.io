---
layout: post
title:  "PCR Cycles"
date:   2015-11-09 08:00:00
author: Maxwell Ng
categories: 
- blog

img: Week-11-header.png
thumb: Week-11-thumb.png
---


#Week 11: PCR Cycles

######The process that never ends...

Welcome back to a [A Fledgling’s Guide to Syn Bio](http://mcmastergem.com/blog/)! We’re all about PCR right now, so let’s jump right into it! Last week we learned about primers, so if you’re unfamiliar with those, check out last week’s post [here](http://mcmastergem.com/blog/2015/11/02/a-primer-for-primer-design/)! If you want an even more general overview of what PCR is, we have that too - [here](http://mcmastergem.com/blog/2015/10/19/phase-one-complete/)! Now we will discuss how to go about calculating the settings on your PCR cycle.

So how does PCR make copies? Well, it’s actually analogous to DNA replication. A DNA Polymerase comes in and, starting from the primers, adds nucleotides to complement the gene of interest. Specifically, we use *Taq* polymerase, because it can withstand extremely high temperatures. Why is this important? Well, to achieve the required separations and re-hydrogen-bond-connections of the DNA strands in PCR, we can simply vary the thermal energy in the system - a.k.a. changing its temperature! This is why it’s so interesting that a PCR machine can often be reduced to a thermal cycler (a machine that cycles different temperatures).

Why does it have to be a cycler? Well, every cycle of the PCR process will double the amount of gene DNA (simplified and ideally). Therefore, to get a large enough sample and at a high enough purity (to outweigh the initial DNA added), we need to repeat the PCR cycle several times.

######*A Side of Physics! #1*

######*Energy can take many forms - chemical, kinetic, thermal, etc. Here, as we will soon learn, we are interested in raising the kinetic energy of the molecules in our system (everything inside the PCR tube). To do this, we can increase the thermal energy of the system. This is because, in this situation, the thermal energy is directly connected to the kinetic energy of the system. Essentially, the hotter the system, the faster things move. Furthermore, we can represent the amount of thermal (or thus, kinetic) energy in the system by a measure of its temperature, a measurement which indicates the average thermal or kinetic energy of the molecules within it.*

A crucial concept in PCR is the that its process happens in steps, and in practice we can break it down into three broad sections: 1. Initialization, 2. the Cycle, and 3. Finalization. Let’s take a look at each of these.

##1. Initialization
This section includes two simple steps: A. system preparation, and B. denaturation of the DNA.

####A. System Preparation
Here we add all the reagents necessary for PCR, including our DNA or gene of interest along with our specific primers and nucleotides, to a PCR tube. This has already been covered in [Week 9](http://mcmastergem.com/blog/2015/10/19/phase-one-complete/)!

####B. Denaturation of DNA
The DNA you added to the PCR machine is most likely double stranded (dsDNA). This is a bit of a problem, because we need our primers to attach to the inside of our DNA helix, and we don’t have all the enzymes and biological tools a living system has. So how do we separate the two DNA strands? Well, by using kinetic energy in the form of thermal energy! See, the DNA is connected via hydrogen bonds, and while these are relatively quite strong, if we can introduce enough thermal energy into the system, the molecules will have enough kinetic energy to break loose from these hydrogen bonds, and therefore will separate (if you want a bit information on this, see the *A Side of Physics! #1* section above!). Now that the DNA strands are separated, the primers will be able to move between them and begin the PCR process.

So how much energy is enough energy? We like to use 95°C for 2min or 3min, as can be seen for Step 1 in the image below. The temperature denotes the temperature the machine achieves, and because the PCR tube is so small, it too will achieve this temperature fairly quickly.

![diagram](https://mnggraphics.files.wordpress.com/2015/11/screen-shot-2015-11-09-at-11-14-37-pm.png){: .center-image .responsive-image }


##2. The Cycle
This section includes three steps: C. denaturing, D. annealing, and E. extension, as presented in the diagram below (temperatures, durations, and cycle counts will vary):

![diagram](http://missinglink.ucsf.edu/lm/molecularmethods/images/clip_image002_0000.jpg){: .center-image .responsive-image }	
[Source](http://missinglink.ucsf.edu/lm/molecularmethods/images/clip_image002_0000.jpg)



####C. Denaturing
This process is the same as the denaturing step in Step B. This is important though because it is the first part of the cycle that will be repeated several times in PCR. However, because the DNA will already be heated and the gene isolated out of the larger plasmid or cassette, the duration of this step is much shorter. For example, we like to use 95°C for 30sec.

####D. Annealing
During this step, the primers attach or ‘anneal’ to the separated DNA strands. For annealing time, primers are generally short and of similar lengths. Therefore, we will consistently use 30sec. However, unlike the previous duration quantities that were essentially ‘standard’ for any piece of DNA, here we need to start doing some calculations.

Why? Well, the temperature value depends on the gene’s nucleotide sequence. Specifically, as we learned last week, the C-G bonds are stronger than A-T bonds, and this will change the amount of kinetic energy we need to add to the system as a results of needing to break these bonds.

######*A Side of Physics! #2*

######*The annealing temperature is a careful balance between too cold and too hot. Too low a temperature, and the primers will be stable enough to bind to DNA sequences on the gene strands that may not be exactly those it was intended for, thereby producing impure yields. Too high a temperature, and the primers won’t be able to bind easily to the DNA sequences on the gene strands, thereby significantly reducing the PCR yield.*

So how do we actually go about calculating this? Well, we could do a lot of math.

Luckily, there are wonderful people who have already automated these calculations for you! There are many out there, and the one we use is [Oligo Calc](http://www.basic.northwestern.edu/biotools/oligocalc.html). It has a lot of more detailed information on how to do the raw calculations if you want, just scroll down on its page!

To do the calculation, add one of your primer sequences (either your forward or reverse, but only one at a time!) to the calculator. This will generate a melting temperature. By rule-of-thumb, we use the melting temperature minus 5°C as the annealing temperature. For example, one of our primers had a melting temperature of 50°C. Therefore, its annealing temperature was 45°C!

Now, what if the two primer temperatures differ? Unfortunately, if it’s more than 4°C, it’s best to change the primer design. However, if it’s less than that, you can simply take the average.

####E. Extension
This step involves *Taq* polymerase adding nucleotides from the primers complementary to the DNA strand. The temperature used is 72°C. Now, while the temperature is the same for different genes (because of the common *Taq* polymerase), the duration will depend on the length of the gene. This makes a lot of sense, since the longer the gene, the longer the time it will take to add nucleotides all along the DNA strand. The calculation here is fairly simple, and there are several possible choices. We generally use 1min for 1kb (kilobase) of DNA. For example, for a gene of about 2kb in length, we would use 2min of extension time.

Now, the DNA synthesis process is complete! To make more DNA, simply repeat steps C through E as many times as necessary. In general, 30 cycles is good enough to achieve high quantities of DNA.

##3. Finalization
This section includes one step: Z. storage.

####Z. Storage
With the PCR process finally complete, after the many cycles, it can now be purified and used. However, it is very likely that you left to do something else since PCR processes can last around 3h long. Therefore, it is very important that the PCR machine finishes by cooling the entire system down as a way to protect and store your new DNA product. This final steps is therefore a standard 4°C for infinity (i.e. until you return to the lab to move it to the next stage or the freezer).

And that finalizes everything for the basic PCR approach!

##But wait, that’s not all!

######Oh yes: overhangs.
Things can get complex as we saw last week with overhangs! So what does this mean? Well, during the first few cycles, only part of the primer will anneal, as the overhangs have no complementary bases on the original DNA base strands. However, after several cycles, there will be more and more DNA strands that were essentially ‘grown’ from these primers with overhangs (prefixes or suffixes), and will therefore contain the overhangs. This allows new DNA strands to be synthesized with the prefixes or suffixes attached!

A simplified summary:

![diagram](http://bitesizebio.s3.amazonaws.com/wp-content/uploads/2014/08/OverhangPCR_Fig1.jpg){: .center-image .responsive-image }	
[Source](http://bitesizebio.s3.amazonaws.com/wp-content/uploads/2014/08/OverhangPCR_Fig1.jpg)


So what will this mean practically? For us, we first do 15 cycles assuming only the complementary part of the primers anneal, and not the overhangs. Then, for the future cycles (another 15), we assume the whole primer anneals. What will this variation in procedure change? Practically, only the annealing temperature. To do this calculation, go back to your calculator of choice, and first use ONLY the part of the primers that are complementary to the DNA, thereby excluding the overhangs you’ve designed (again, do each primer separately). Use the calculated annealing temperature for the first 15 cycles. Remember! Annealing temperature is (rule-of-thumb) 5°C less than melting temperature, so make sure of which temperature you write down after using the calculator. Then, calculate the annealing temperature using the entire primer (i.e. including the overhang) because it is now assumed that there is enough DNA strands with the desired prefixes or suffixes. This will be of a higher temperature, perhaps of about 10°C higher - as was in our case when adding the BioBrick sticky ends.  Use this new annealing temperature for the next 15 cycles.

####That’s all folks (for this week)!
Hopefully you enjoyed this discussion on how to calculate your PCR cycles settings! If you have a question or comment, leave us a message below! We'll see you next week!