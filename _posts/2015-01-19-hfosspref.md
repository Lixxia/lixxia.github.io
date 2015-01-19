---
layout: post
title: My H/FOSS Preferences
date: 2015-01-19 1:23AM
---

I generally keep track of the new and popular open-source projects. All of my choices were selected from my list of starred projects on Github. They are listed in order of preference.

# Mopidy ♪

[Website](https://www.mopidy.com/) / [Github](https://github.com/mopidy/mopidy) / [Documentation](https://docs.mopidy.com/)
> **Mopidy is an extensible music server written in Python.**
> 
> Mopidy plays music from local disk, Spotify, SoundCloud, Google Play Music, 
> and more. You edit the playlist from any phone, tablet, or computer using a 
> range of MPD and web clients.

I had looked up Mopidy previously in order to find an alternative to the default Spotify client. Since then it's been on my list of interesting open-source tools/projects. 

I think this project could be a good choice for several reasons:

### Well documented
As is the norm with most open-source python projects, Mopidy is well documented utilizing ReadTheDocs. There are great details on how to install and run Mopidy, as well as documentation on how to contribute to it. 

### Large and active community
Mopidy is a fairly active project. It has 5976 commits on github, 81 releases, 44 contributers and 137 issues with the most recent update to the development branch dated 13 days ago. 

Additionally they have a [discussion forum](https://discuss.mopidy.com/), [issue tracker](https://github.com/mopidy/mopidy/issues) via github, IRC channel (#mopidy on irc.freenode.net), twitter (@mopidy) and announcement [mailing list](https://groups.google.com/forum/?fromgroups=#!forum/mopidy). 

### Labeled Issues
The issues listed on github are well organized and labeled depending on their content. Some examples of labels include the typical bugs, enhancements, local, and core. However, they've also labeled issues with "easy starters" which could be very helpful for starting contributors. 

### Test Coverage
Mopidy has "quite good test coverage, and we would like all new code going into Mopidy to come with tests." They also have [test coverage statistics](https://coveralls.io/r/mopidy/mopidy).

---

# Komanda <img src="http://komanda.io/image/komanda-solid.png" alt="Komanda" height="40px" width="40px" style="background-color:#1F4B7F;border-radius:100%;border:1px #1F4B7F solid">

[Website](http://komanda.io/) / [Github](https://github.com/mephux/komanda)
> **The IRC Client For Developers**
> 
> Komanda uses IRC for its communications protocol and as a result supports everything you're likely used to.
> 
> Komanda UI was built with html5, Javascript and CSS3 everything you see can be changed. 
> 
> Komanda ships with tight integration with github. 

This is definitely not my first choice for a project, it's a much smaller community and not quite as active. The project isn't terribly well documented and there appears to be no official communication channels (mailing list, irc) other than the github issue tracker. 

I put it up here for consideration because anything contributed would make quite the difference, as this is an IRC client still in beta. It's a good idea, and the execution so far has gone well. It would be interesting to work with, and as a client built using web-based tools/languages (node, javascript, html, css) it would be easy to test. 

---

# <img src="https://www.djangoproject.com/s/img/logos/django-logo-positive.svg" alt="Django" height="50px" width="600px">

[Website](https://www.djangoproject.com/) / [Github](https://github.com/django/django) / [Documentation](https://docs.djangoproject.com/en/1.7/)

> **Django was invented to meet fast-moving newsroom deadlines, while satisfying the tough requirements of experienced Web developers.**
> 
> Django is a high-level Python Web framework that encourages rapid development and clean, pragmatic design. Built by experienced developers, it takes care of much of the hassle of Web development, so you can focus on writing your app without needing to reinvent the wheel. It’s free and open source. 

Django is a very popular, widely utilized web framework with a *huge* community. On github: 19,796 commits, 94 releases, 761 contributors and 0 issues. That's right 0. At the time I looked at their main github page there had been a commit 3 hours prior. All issues were solved waiting to be merged with 74 total pull requests.

Now popularity of this magnitude becomes a huge drawback. The project becomes somewhat unapproachable because of the established community behind it. It is, of course, open for contribution, but it may be intimidating or more difficult than a medium-popularity project (such as Mopidy or Scrapy). 

They do have a #django channel on irc.freenode.net, archives of that channel and a [mailing list](https://groups.google.com/group/django-users) and a test suite. 

---

To me, Mopidy is the best balance of community, popularity and approachability. So my vote for our project will likely be [Mopidy](https://www.mopidy.com/) or Cameron's suggestion [Scrapy](http://scrapy.org/). 