---
layout: post
title: What's Happening?
date: 2015-02-18 12:09PM
---

# TOS 7.2
Run with no flags, `diff` only shows the line(s) changed between the two files.When used with `diff` the `-u` flag provides better context on those changes. It shows the text that is the same, with the changed lines (either additions + or removals -) around it. 

# TOS 7.8
Fairly straightforward, just pipe the contents of a diff into a `.patch` file. 

# TOS 7.9
Again, easy to follow directions. It helps that I've worked with patches previously. While installing [i3wm](http://i3wm.org/) there were a few features I wanted, but were not part of the main package. These features could be obtained by installing patches for the source code. So the process is familiar to me. 

# Proofs Probable
I chose an article from *Communications of the ACM, 6/2013 Vol. 56 No. 6*. It discuses Shafi Goldwasser's and Silvio Micali's efforts towards laying the foundations for modern cryptography with contributions regarding interactive and zero-knowledge proofs. 

This article drew my attention because Shafi Goldwasser was a keynote speaker at [GHC 2014](http://gracehopper.org/), which I had the pleasure of attending. Her keynote is still availible for view [here](http://new.livestream.com/anitaborginstitute/events/3444251/videos/64324972) (Introduction begins at 47:35 and her talk starts at 48:50). 

She spoke of zero-knowledge proofs, giving a brief overview of what they were and how they were utilized. It was interesting because a lot of the audience was confused (to be fair, the talk was very technical/math oriented). The only reason I understood was because I took a Cryptography course at the University of Tartu where we covered zero-knowledge proofs. 

The article outlines the efforts of Goldwasser and Micali in the field of cryptography. How they developed a formal definition of security and worked on different secure encryption methods. Their work on interactive proofs which lead to the development of zero-knowledge proofs:

>... which allow the user to convince someone else of the correctness properties of a piece of information, without actually revealing what that information is.

They also worked on the necessity of utilizing randomness in encryption, allowance for (a very small) probability of error. Their efforts laied the foundation for modern cryptography, which today, is more important than ever. 

Both Goldwasser and Micali received the ACM Turing Award:

>For transformative work that laid the complexity-theoretic foundations for the science of cryptography and in the process pioneered new methods for efficient verification of mathematical proofs in complexity theory.

# 12 Predictions for the Future of Programming
This is the same article we had to read for the previous semester, and my opinions on it have not changed too drastically. 

##Future of programming prediction No. 1: GPUs will be the next CPUs
There are certainly benefits to utilizing GPUs for processing. And if properly harnessed it's speed can be quite impressive. I still maintain that GPUs will not replace CPUs, but we will likely see more use of both, regardless of the need for actual graphical processing.

##Future of programming prediction No. 2: Databases will perform increasingly sophisticated analysis
I absolutely agree with this one. The use of buzzwords, as stated in the article, such as "Big Data" are becoming increasingly popular and for good reason. Data mining is profitable. Companies like google with countless amounts of user data at there fingertips have figured out a way to utilize and profit off of that data. Algorithms that parse through the data and development of machine learning analytics are very popular right now and we will absolutely see an increased use of this technology in the future. Not only in the tech industry, but also in the government.  

##Future of programming prediction No. 3: JavaScript for everything
I'm not sure I agree with this one. On the one hand, JavaScript is indeed becoming more popular, especially with the related increase of web-based applications and app frameworks such as ionic. On the other hand this is always subject to change, and this is a powerful and broad prediction to make. Additionally there will always be a language that becomes popular and eventually falls into disuse because of the introduction of a new or more efficient language.

There are some that would convince you that javascript is here to stay as the next big thing, especially if they're from the valley. 

##Future of programming prediction No. 4: Android on every device
For some of the same reasons stated above, I don't agree with this. Technology is evolving and this is too bold of an assumption. It appears to biased for me to actually agree with, not that I have any issue with Android. However, many developers *do* have a problem with Android, mostly regarding writing for it and dealing with it's API breaking versions. 

##Future of programming prediction No. 5: The Internet of things -- more platforms than ever
Another solid agreement from me. Technology and Internet integration will absolutely increase and be utilized in more things.

##Future of programming prediction No. 6: Open source will find new ways to squeeze us
From my point above about the increased use of open source I think this has the potential to happen. However, one of the attractive attributes of open source software is that it's usually free. Not sure how this one will pan out, it could really go either way.

##Future of programming prediction No. 7: WordPress Web apps will abound
Absolutely *do not agree* with this one. The underlying prediction is fine, that the use of existing frameworks to build a website or app will become increasingly popular. However "WordPress Web apps" is too specific of a prediction. In addition, while the use of frameworks or web  apps may be easier you lose a lot of customization ability.

##Future of programming prediction No. 9: Long live the command line
I'm not sure that I agree with this one. The use of the command line allows for a deeper control and understanding of the processes and tasks being done. GUI may seem easier in some senses, but things can be done quicker and with more efficiency if they are done via command line. I myself have been migrating towards command-line based utilities, they run faster and allow for better and faster navigation via keyboard. That being said, the GUI is not likely to go away anytime soon.

##Future of programming prediction No. 10: Dumbing it down will fail
I don't think I agree with this, mostly based on the phrasing and flimsy argument. The simplification of technology to facilitate an easier introduction to difficult concepts is not a bad idea, and is not doomed to fail simply because the idea seems unpalatable. It certainly takes a lot of work, and there will be failed attempts but the overall approach is not a bad one.

##Future of programming prediction No. 11: Outsourcing and insourcing will remain deadlocked
It's harder for me to provide an opinion on this one, as I don't have a lot of experience or knowledge on it. It's also hard to say as it will depend on the company.

##Future of programming prediction No. 12: Management will continue to misunderstand coders and coding
This may or may not prove true. If neither party (management and coders) seek to facilitate better understanding then yes, there will be continued misunderstandings in the future. Each group seem to have a chip on their shoulder about this. Coders seem to feel that they are entitled to being understood even when they don't try and explain in more understandable terms or use different terminology. Management seem to believe they are owed something by the coders and generally don't seek any sort of understanding or wish to be spoon-fed. I feel that this is more of an individual and generational issue that is not so much related to "the future of programming" but the "future of human interaction."  