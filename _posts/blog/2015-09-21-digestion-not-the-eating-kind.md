---
layout: post
title:  "5. Digestion (not the eating kind!)"
date:   2015-09-21 08:00:00
author: Yu Fei Xia
categories: 
- blog

img: post06.png
thumb: thumbs05.jpg
---

#Week 5: Digestion (not the eating kind!)

Surprise!! I’m back again, two weeks in a row! Usually this would be Max's post, but he’s a bit busy this week so just this once I’m posting in his stead. Who knows, maybe Max will be taking over one of my posts sometime :). This week’s topic requires quite a bit of background, but I think it is very interesting and will give you a new perspective on the ‘classic’ method that you have probably learned about in high school. If you missed last week's post on Miniprep, read it [here](http://mcmastergem.com/blog/2015/09/14/e-coli-go-to-a-happier-place/)!

The restriction digest, commonly known as digestion, is the process in which a DNA strand or plasmid is cut at specific DNA sequences, called restriction sites. This happens through hydrolysis, which is probably why the name of the process is digestion - the backbone is ‘digested’ at the restriction site into smaller pieces. We use restriction enzymes, which recognize the specific restriction sites on DNA and cut at that location. Restriction enzymes originated from bacteria, as a defense mechanism for destroying viral DNA.

![](https://scontent-lga1-1.xx.fbcdn.net/hphotos-xap1/v/t1.0-9/10368188_1101992526492542_2817754395985373711_n.jpg?oh=b807c88fe6d9e66f1adc3da4709bd68d&oe=569F04B6){: .center-image .responsive-image }
[Source](http://www.scq.ubc.ca/restriction-endonucleases-molecular-scissors-for-specifically-cutting-dna/)

In synthetic biology, digestion is used in cloning to isolate genes of interest from plasmids, so that we can work with them to create recombinant DNA - plasmids with gene sequences and functions that we design. This can then be introduced to our bacteria, which will display the desired traits.

The process of digestion itself is quite simple. You find a restriction site that is present on both sides of your gene of interest, and use the restriction enzyme as well as some buffers to cut at those locations. The important part is to study your plasmid diagram and gene sequence carefully before choosing a restriction enzyme to work with. You don’t want to cut through your gene of interest, nor do you want too many places cut due to having the same restriction site. A sample with too many different gene segments which all have a common restriction site will later reduce the efficiency of ligation , since there is less chance that what is ligated includes the piece with the gene of interest.


However, like I mentioned in the introduction, there is a twist to the digestion protocol we are learning about today. iGEM plasmids containing specific gene sequences, known as BioBricks, come with *four* standard restriction sites (surprising right?), cut using four corresponding restriction enzymes. The sites are called **EcoRI** **(E)**, **Spel (S)**, **Xbal (X)**, and** Pstl (P)**. **E** and **S** are located on the left of the sample, or before the gene, and **X** and **P** are located on the right side, after the gene. This plasmid ‘format’ is part of the iGEM *Standard 3A assembly protocol*, which allows for two-part assemblies (adding two genes or parts to a plasmid backbone to create a new BioBrick). The logistics of this assembly method will be further explained in the post on ligation, which will be next week, but for now it is important to know that using four different restriction sites allow us to assemble the BioBricks in a certain order, which is important if we want to create gene circuits that involve downstream activation. Don't panic at all these sites! Ultimately, the underlying framework isn’t much different than normal digestion, where we would only use one restriction enzyme for a common restriction site located on each side of our target gene.

![](https://scontent-lga1-1.xx.fbcdn.net/hphotos-xfl1/v/t1.0-9/12032272_1101992543159207_708862994265303906_n.jpg?oh=a82094eb045398f3ce4520fd6d36dc37&oe=56934FA2){: .center-image .responsive-image }
[Source](http://parts.igem.org/Help:Assembly/3A_Assembly)

<br><br>

##The procedure (finally!):


Let’s create a scenario where we have two samples of Miniprepped plasmid DNA - the promoter sequence pBAD/AraC and the gene sequence ho1 - and we plan to insert them both into a new plasmid with Kanamycin resistance to create an intermediate of our final (plasmid) design. We must first digest both genes out of their original plasmids, using restriction enzymes for two of the four sites on each plasmid. pBAD is the promoter, so we want it to be located upstream of the ho1 sequence; therefore we will cut using the **E** restriction enzyme and the **S** restriction enzyme. ho1 will be cut at the **X** and **P** sites, allowing it to be attached after the promoter. Again, the reason for this will be explained in further detail in next week’s post on ligation.

![](https://scontent-lga1-1.xx.fbcdn.net/hphotos-xtf1/v/t1.0-9/12036707_1101992556492539_8500390147664457540_n.jpg?oh=56bebcf72d7df9117e3455cd4eecbbe3&oe=565DCC11){: .center-image .responsive-image }
*The promoter pBAD*

![](https://scontent-lga1-1.xx.fbcdn.net/hphotos-xfp1/v/t1.0-9/12011356_1101992589825869_8658171084529371137_n.jpg?oh=083fcb0be3db7940ee805eda8b6c7c13&oe=56971B7E){: .center-image .responsive-image }
*The BioBrick ho1*


A DNA digestion is usually done in a 1.5mL sample tube. The mixture requires the plasmid DNA, NEB buffer for the enzymes, BSA (Bovine Serum Albumin) which prevents the enzymes from sticking to the sides of the sample tube, water to dilute the solution, and of course the restriction enzymes. It really doesn’t matter what order you use when adding in these components (which is why this post isn’t as stepwise in format), as long as you ***add in the enzymes LAST, AFTER the NEB buffer and BSA***. Otherwise, the enzymes will be destroyed due to the environment of the solution. If a mastermix is available (a premade mixture of NEB, BSA and the enzymes), just use the mastermix, water, and the plasmid DNA. The iGEM digestion protocol calls for 250ug of plasmid DNA in your sample, which means you will be adding different volumes depending on the concentration of DNA you have. This is why the required volume of water will vary - it is only added to make sure that the final volume in the sample tube is 20uL. If you have 20uL of solution without the water, then adding it is not necessary. 

![](https://scontent-lga1-1.xx.fbcdn.net/hphotos-xaf1/v/t1.0-9/12032244_1101992536492541_4092753026394400841_n.jpg?oh=af0375e10f8e5c5943e0dc7335c2af3e&oe=56628B00){: .center-image .responsive-image }

Depending on what protocol you use and where you buy your buffers, the ratios of the components will be different. For our pBAD digestion, we used 5uL plasmid DNA, 11uL water, 2.5uL NEB, 0.5uL BSA, 0.5uL enzyme **E**, and 0.5mL enzyme **S**. They were added in that order purely by preference, EXCEPT for the enzymes which were added LAST! Since there were so many things to add and sometimes I worked on two digestions at once, I found it helpful to keep track of what I had added by shifting the sample tube one spot forward on the tray every time I added something new. Sometimes, I even checked off a list of the components I had added on the side. This way I wouldn’t forget a component, or add something twice. Remember to use the appropriate micropipettes when adding each component, switch pipette tips after every use, and keep the sample tubes closed between additions to prevent contamination of your sample (at this point labelling your samples properly should be a given, right?)!

![](https://scontent-lga1-1.xx.fbcdn.net/hphotos-xpa1/v/t1.0-9/12049710_1101992579825870_3738039465448653011_n.jpg?oh=394e4c281926472097b9c30af3a177cf&oe=56948FA6){: .center-image .responsive-image }

After you have added everything to the sample tubes, centrifuge to collect everything at the bottom, and incubate the samples at 37°C for 30 mins. Then, *heat kill* the enzymes in your sample at 80°C for 20 mins (for a review of heat kill vs heat shock, revisit [Transformations](http://mcmastergem.com/blog/2015/08/31/the-magical-world-of-transformations/)). This denatures the digestion enzymes so that they are no longer active and will not interfere in future procedures involving this sample. Don’t worry about the DNA, as it is fairly stable and only begins to denature at a higher temperature.

![](https://scontent-lga1-1.xx.fbcdn.net/hphotos-xfa1/v/t1.0-9/12042719_1101992569825871_966801383235269487_n.jpg?oh=a031dba2fca855ff15224e85df057a87&oe=56935A62){: .center-image .responsive-image }

(Image only for demonstrative purposes. Always use gloves as PPE when working in the lab!)

And there you have it, your sample should now be properly digested, and ready to be recombined using ligation. Store them at -20°C until the next use. Tune in next week for ligation, or what is in my opinion one of the most troublesome procedures in my experience with synbio!

---

*Source: Everything I’ve learned about the iGEM digestion protocol was taught by my kind upper year teammates, Hamza Q., Sam S., Michael R. and Vivian L. Find them on our [team page](http://mcmastergem.com/tp.html)!*

*I also forgot to mention the source of last week’s post on Miniprep; the workings of the spin column collection tube as well as the procedure itself were patiently explained to me by Michael X. :).*