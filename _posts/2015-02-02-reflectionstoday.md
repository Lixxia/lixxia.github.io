---
layout: post
title: Reflections on Open Source in Today's World
date: 2015-02-02 11:39AM
---
# Freeciv Exercise
Pulling from the svn repository took quite some time, mostly while retrieving the graphical assets (there were a lot). 

This was really the only "difficult" part. Everything else was fairly straightforward. There were some conflicting instructions but I didn't run into too much trouble. Since I've messed around with C and C++, as well as installing code from source there wasn't much left for me to actually install in terms of dependencies. Most of the dependencies were already on my system. The few I needed were easily installed with a simple `apt-get`. 

Then I ran `./autogen.sh` and was ready to `make`. I almost ran `make install` by habit, but thankfully remembered that the article mentioned it was not necessary. 

It was not a particularly eventful article, but I'm sure if I hadn't read the article first I would've encountered most if not all of the errors mentioned. I've definitely had my fair share of dependencies issues.

# Article One
## [Good Design Matters for Open Source Projects](http://opensource.com/life/15/2/good-design-matters-open-source-projects)

This article overviews the importance of design in open source projects. For a while open source projects had a mostly unfair reputation of being clunky in terms of UX/UI. Design was not often the main importance. Given the recent increase in popularity of web-apps, design frameworks and other similar things; design has started to become important to both the user and the developer. 

And it's true, there has been a recent increase in well-designed open source projects. The article mentions a few: [ElementaryOS](http://elementaryos.org/) and [Ghost](https://ghost.org/) being two popular ones that I've heard of. The most recent example I've seen is [Paperwork](https://paperwork.rocks), an OpenSource note-taking & archiving alternative to Evernote, Microsoft OneNote & Google Keep. 

>We are not a part of any design ecosystem, and there was no mentor we could ring up and ask for recommendations.

This is fairly common, and it's important to know the structure of a project and admit that nobody has design experience. There are tons of experienced designers out there, and while it can be expensive it's often better than stumbling along and ultimately turning out a messy product. 

That being said, there have been a *lot* of frameworks based on specific styles of design emerging. People with no design experience but a good eye can often jump right in by utilizing these frameworks. Some examples are:

- [Bootstrap](http://getbootstrap.com/)
- [Material-UI](http://material-ui.com/#/)
- [Materialize](http://materializecss.com/)
- [Skeleton](http://getskeleton.com/)

There are also other design assets such as icons:

- [FontAwesome](http://fontawesome.io/)
- [Ionicons](http://ionicons.com/)

This allows more people to create a more well-designed framework, which can be both a good and bad thing.

# Article Two
## [The current state of video editing for Linux](http://opensource.com/life/15/1/current-state-linux-video-editing)

Within this article I learned a bit about some open-source alternatives for video editing. But more importantly I saw another example of a common FOSS vs. Proprietary software issue.

Often times there is some proprietary software that fulfills a specific requirement or niche. It usually operates very well and fulfills most if not all of the user's needs. Some examples are as follows:

## 1. Document Editing
This is a prime example. The standard is generally accepted to be Microsoft Word. It works well, must be paid for, and is used by many. There are, of course, open source alternatives. The popular ones are [Libre Office](http://www.libreoffice.org/) and [Apache Open Office](https://www.openoffice.org/). 

Now I've used both, and although I love OSS, there are some things that Microsoft word just does better. That's not to say it's perfect, but it generally works better for me than LibreOffice. 

## 2. Photo Editing
Another great example. The giant in this field is [Adobe Photoshop](http://www.photoshop.com/). It's a full suite of tools, with support and frequent updates by Adobe. Again, it's by no means perfect but it's largely regarded as the 'standard' for photo editing or really anything involving digital art/composition. 

The most common FOSS alternative is GIMP. It has a lot of the same functions as Photoshop and can perform the same basic tasks. Again, I've used both, and personally I don't think GIMP even holds a candle to Photoshop. It's clunky in UI and the interface is very non-intuitive. I hate the fact that Photoshop is so expensive, but just works so much better. 

## 3. Video Editing
And we come back to the focus of the article, I see the same patterns here. The author mentions 3 main tools: Avid Media Composer, Final Cut Pro and Adobe Premiere.

>In the VFX industry these three tools are used extensively among studios for cutting video and film and are both very simple to use for noobs and professionals alike as well as can be pushed very far in the hands of guru artists. The VFX industry has for the most part of the last 30 years been reliant on Mac and PC for video editing, primarily because all of the Linux-based FOSS tools have been less than great.

He then discusses the multiple FOSS alternatives he had to try, there were seven total. In the end he did find one he was happy with by the name of [Blender](http://www.blender.org/). He also states:

>I would say [blender] can go head to head with the best of what I've used in the VFX industry. And, I'm genuinely surprised!

So great, he found a FOSS tool that works as well as the proprietary versions. I'm not saying this is uncommon or impossible. (Do note that he said he was surprised though.) There are excellent pieces of open source software, and most of the time I prefer those versions. *But* it often takes some digging and struggling through learning curves before you find what works best for you.

It's nice to have such a variety for those who are willing to do the leg work, and for everyone else there's always that semi-standard proprietary software. 

