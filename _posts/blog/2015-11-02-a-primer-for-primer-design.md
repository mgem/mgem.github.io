---
layout: post
title:  "10. A Primer for Primer Design"
date:   2015-11-02 08:00:00
author: Yu Fei Xia
categories: 
- blog

img: post10.png
thumb: thumbs10.jpg
---

#A Primer for Primer Design

Welcome back everyone! I hope you all had a great Halloween :). This week’s post is the first protocol entry for phase 2 of our Fledgling’s Guide series. We apologize for the brief break in our schedule last week, but from this week onwards the blog is back on track again! Today we will be talking about the very interesting concept of primer design. As Max has already explained in our [most recent entry](http://mcmastergem.com/blog/2015/10/19/phase-one-complete/), it is very common to obtain your plasmid, or cassette, with your gene of interest (GOI), but realize that it does not have the restriction sites needed for your project. Especially in the case of iGEM, where all BioBricks come with the standard 4 restriction sites to be used with the 3A assembly method ([remember E, X, S, P](http://mcmastergem.com/blog/2015/09/21/digestion-not-the-eating-kind/)?), it is unlikely that a cassette can be ordered with these same restriction sites already included. PCR is a tool that can be used to isolate and amplify our specific GOI while adding the restriction sites of our choosing. This allows them to be compatible with our other iGEM BioBricks, and also match the correct format for BioBrick submissions. However, everything comes down to designing the perfect primer.

![](https://scontent-yyz1-1.xx.fbcdn.net/hphotos-xpf1/v/t1.0-9/12190923_1125652094126585_1944749088803828038_n.jpg?oh=88b403cbed59cfe34b3dac9a244653b5&oe=56BC9464){: .center-image .responsive-image }	

[Source](https://actu.epfl.ch/news/optimal-qpcr-primer-design-2/) 

Recall that a primer is a piece of single-stranded DNA that attaches to its complementary sequence on the cassette you plan to PCR. This sequence would of course be the beginning and end portions of your GOI. Therefore for every GOI you plan to isolate from a cassette, you will need to design TWO primers; the forward primer, which is about 20 bases complementary to the beginning of the sense strand, and the reverse primer, a sequence of about 20 bases complementary to the anti-sense strand of our GOI at the opposite end. This concept is shown in the drawing below:

![](https://scontent-yyz1-1.xx.fbcdn.net/hphotos-xpa1/v/t1.0-9/12195851_1125652114126583_6805539722550046149_n.jpg?oh=12b0bbc651b7b51e4428c456dea4d12b&oe=56D10F77){: .center-image .responsive-image }	
 
[Source](https://www.youtube.com/watch?v=tUyBwiyMsSU) (also a helpful video for primer design!)

These primers will allow Taq polymerase to attach to the plasmid at your primer, and amplify only the GOI. However, at this stage we are not finished yet! We need to check the *GC content* of our primers, and add *prefixes and suffixes* as well.

###GC Content:

As shown in the picture above, so far we have the forward primer **5’ GCAATGCACTACGATTCGATC 3’** and the reverse primer **5’ GATGTCATGAGATCGAATCG 3’** (note that the reverse primer is also written from 5’ to 3’!). However, their efficiency in annealing to the complementary site on our GOI (and subsequently starting the PCR amplification cycle) depends on the percentage of Guanine or Cytosine bases in the primer. This is because G and C are connected by 3 hydrogen bonds in double-stranded DNA, while A and T are only connected by 2. The primer with more GC content will naturally anneal more reliably to the GOI. The standard GC content of a primer should be 40-60%, and if this is not the case then the primer should be extended by 1-2 bases to include an extra G or C. In our case, both primers have a good GC content, so we do not need to extend them.
 
![](https://scontent-yyz1-1.xx.fbcdn.net/hphotos-xpf1/v/t1.0-9/12208684_1125652097459918_9128906089060173895_n.jpg?oh=f4733cdc02c4ce78253988ccadffbe9f&oe=56B7E0A8){: .center-image .responsive-image }	

[Source](https://en.wikipedia.org/wiki/GC-content)
 
###Prefixes and Suffixes – Adding the Restriction Sites

At this point, we have working primers that will allow us to amplify our GOI. However, without the correct restriction sites on each end, we cannot digest the product with our restriction enzymes or ligate them to our BioBricks or plasmids. To solve this problem, we must add a prefix to the forward primer and a suffix to our reverse primer that are both the complementary sequence to the iGEM BioBrick format. The prefix or suffix followed by the original primer sequence will be our final primer design for the GOI. The prefix and suffix sequences will be incorporated in the second cycle of PCR so that the end result is our GOI with the E, X, S, and P restriction sites.

The [standard BioBrick format](http://parts.igem.org/Help:BioBrick_Primers) for prefixes and suffixes is as follows:

**Prefix-F: 5' GAATTCGCGGCCGCTTCTAG 3'** 

**Suffix-R: 5' CTGCAGCGGCCGCTACTAGTA 3'** 

Where **GAATTC** is the *EcoRI* restriction sequence, **TCTAGA** is the *Xbal* sequence, **ACTAGT** is the *Spel* sequence, and **CTGCAG** is the *Pstl* sequence. Note that **GCGGCCGC**, located between E and X as well as S and P, is a site called *Notl* that is 
not one of the 4 restriction sites used in iGEM 1a assembly. The *Notl* site also has very high GC content, which in this case would be unbeneficial since it will raise the melting temperature for our PCR cycles (calculating melting temperatures will be covered in next week’s post on PCR). Since *Notl* is not used in any digestions or ligations, and is not integral to the primer structure, our team decided to remove them from our prefixes and suffixes. When the modified prefixes and suffixes are joined with the original primers, we have:

**Forward: 5' *GAATTCTTCTAG*  GCAATGCACTACGATTCGATC 3'**

**Reverse: 5' *CTGCATACTAGTA*  GATGTCATGAGATCGAATCG 3'** 

Again, note that primers are always written from 5’-3’ even though the reverse is often 3’-5’ (see the first diagram) because this is the format for submission when you order your primers. Do not enter the sequence backwards, or you will receive an incorrect primer!

Congratulations! You now know the basics of primer design for isolating genes from cassettes using PCR, as well as adding your own prefixes and suffixes to create restriction sites that are compatible with the assembly system you choose to use. This knowledge will be applied further next week, when you learn the basics of PCR with Max.

*Have a great week, and see you next Monday!*  

![](https://scontent-yyz1-1.xx.fbcdn.net/hphotos-xat1/v/t1.0-9/12122607_1125652117459916_3782239656567916963_n.jpg?oh=19632e0d008f0470d60456e24cb96302&oe=56CC8947){: .center-image .responsive-image }	

[Source](http://www.clipartlord.com/category/halloween-clip-art/pumpkin-clip-art/jack-o-lantern-clip-art/ )





