---
layout: post
title:  "The Sequence Matters!"
date:   2015-10-12 08:00:00
author: Yu Fei Xia
categories: 
- blog

img: post08.png
thumb: thumbs08.jpg
---
#Week 8: The Sequence Matters!

Hey guys, guess what?!? We’re already a good half-way through this blog series!!! Can you believe it? I didn’t think the time would go so fast, but I’m so glad we’re able to come this far together. This week will be our last post in the first portion of this series. Up until now, we’ve essentially covered how to clone, starting from plasmids that contain your DNA interest. Last week we ended with ligation, and we now have our successful recombinant DNA plasmid, exactly as we’ve designed it. Now the only thing left is to transform it into our E. coli, and we will have successfully completed cloning! But how do you confirm that you have the right plasmid? Even if your transformation is successful, as a scientist you must quantifiably prove that the sequence of the new plasmid is identical to the one you’ve designed. This is where sequencing comes in. Intrigued? Well not so fast! Before we start, here’s a fun fact from Max (didn't see that coming did you!):


**Max’s Laboratory Wisdom:**

![](http://mcmastergem.com/img/team/t16.jpg){: .center-image .responsive-image }

It is a common misnomer that Redsafe, the DNA dye used in gel electrophoresis is safe. While safety is literally part of the name, don’t be fooled! It is deemed *safer* (strictly in a relative sense) than ethidium bromide (a carcinogen), which was the dye used previously. However, you should still be careful when handling the substance. Always practice proper lab safety - wear gloves, wash your hands after working in the lab, and don’t eat food in the lab!!

![](https://scontent-yyz1-1.xx.fbcdn.net/hphotos-xta1/v/t1.0-9/12141696_1114139875277807_612088632114683270_n.jpg?oh=b1ba4b66ffd1c241a09a3ac3585ab35d&oe=568A9E3E){: .center-image .responsive-image }

[Source](http://www.froggabio.com/products/387/RedSafe%99+Nucleic+Acid+Staining+Solution+1ml)

Alright, now that you all know about the deceptive Redsafe, on to sequencing! This will be a relatively short post since all the leg work is automated by now (it is 2015, thank gosh), but I will try to give you some tips and a general idea on the concept of sequencing. :)

**DNA Sequencing:**

When you send in your plasmid for sequencing, you will receive your results in the form of a string of bases (think an endless sequence of stuff like AGTTCCAAGTCGATCGCGGA), as well as a copy of the electropherogram (an electropherogram is a plot of your results).

![](https://scontent-yyz1-1.xx.fbcdn.net/hphotos-xat1/v/t1.0-9/12112361_1114139905277804_4461628532264324827_n.jpg?oh=fb61f771cf8b6c759c66457f10cf6dc0&oe=56C6E5F3){: .center-image .responsive-image }

[Source](http://www.udel.edu/dnasequence/Site/Interpreting_Electropherograms.html)


The most common sequencing method today is the Sanger method, which is based on fluorescently tagging deoxynucleotide (ddNTP) bases with different colours, then separating them by size and reading the sequence of colours (and therefore bases)<sup>1</sup>. You can learn more about the history of DNA sequencing [here](https://www.youtube.com/watch?v=8n2LvJ-m0n0). 

The main points you need to know to interpret your data however, is that DNA sequencing only reads the first 500-1000 bases, whether it is in the forward or reverse direction. This means that if you’re plasmid consists of 2 genes, each around 1kB long, then you must check both the forward *and* reverse sequencing results to confirm that both genes are *present*, and in the *right order*. Other than that, it’s just a matter of matching up bases between your results and your Biobrick gene sequences. If they match, congratulations - you’ve successfully created your plasmid!

Of course, nothing in life is this straight to the point (especially in science and technology), and you might get some weird readings in your results. In your sequence, there will be N’s interspersed throughout in the place of a DNA base, or even several N’s in a row. These results have many names and categories, and each has a different manifestation on the electropherogram. To read more on the specific causes of the different factors, you can go [here](http://ampliconexpress.com/troubleshooting-dna-sequencing-evaluating-sanger-dna-sequencing-chromatogram-data/).

![](https://scontent-yyz1-1.xx.fbcdn.net/hphotos-xap1/v/t1.0-9/12115787_1114139915277803_3602710999639504653_n.jpg?oh=08c04e8eeece8a7c66a9385457f532c9&oe=569CED9E){: .center-image .responsive-image }
[Source](http://ampliconexpress.com/troubleshooting-dna-sequencing-evaluating-sanger-dna-sequencing-chromatogram-data/)


When you receive unexpected results, check your primers for sequence errors (especially if you’ve designed them yourself). as well as expired reagents you may have used or inhibitory enzymes in your sample that may have affected the sequencing enzymes<sup>2</sup>.You may also want to check the concentration of your DNA sample to see if there is a significant amount, and how long the sample has been stored (perhaps there has been UV damage, or damage from repeated freezing and thawing)<sup>2</sup>. There are many other reasons you can investigate, and this is all part of the troubleshooting process. There is no specific protocol that will prevent or solve all problems, and sometimes things just don’t work out. However, don’t fret! Just keep looking over your steps, and you will find a solution.


And that’s all for this week! Relatively short post, I know! But I figured you wanted to quickly get back to your turkey dinner - it is Thanksgiving after all! So have a great Thanksgiving, and know that this year one of the things I’m thankful for is being able to create this blog through mGEM and meet all of you! See you guys next week!
----------
**Sources:**
----------
1. iBiology. Jonathan Weissman (UCSF/HHMI): DNA Sequencing [Internet]. [cited 2015 Oct 10]. Available from: (https://www.youtube.com/watch?v=8n2LvJ-m0n0)[https://www.youtube.com/watch?v=8n2LvJ-m0n0]

2. Dillon C. Troubleshooting DNA Sequencing: Evaluating Sanger DNA Sequencing Chromatogram Data | Amplicon Express [Internet]. Ampliconexpress.com. 2014 [cited 2015 Oct 10]. Available from: (http://ampliconexpress.com/troubleshooting-dna-sequencing-evaluating-sanger-dna-sequencing-chromatogram-data/)[http://ampliconexpress.com/troubleshooting-dna-sequencing-evaluating-sanger-dna-sequencing-chromatogram-data/]
