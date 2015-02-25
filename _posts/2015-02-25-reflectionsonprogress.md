---
layout: post
title: Reflections on my Progess
date: 2015-02-25 12:53PM
---

I think we're making good progress as a team so far. According to our [timeline](http://still-pending.wikispaces.com/Report+2), our next milestone is **February 26** where we hoped to "Have at least two issues solved at this point OR begin work on feature." 

After our meeting last Friday, February 21, we made the decision to *not* work on a feature. The feature/enhancement we were considering was [dynamic playlist](https://github.com/mopidy/mopidy/issues/620), which would've been extremely interesting but also quite difficult. We came to the conclusion that it would be in our best interest to work on several bugs or smaller enhancements. 

I'm not sure what our progress is on our latest issue, but Cameron opened up an issue [#994](https://github.com/mopidy/mopidy/issues/994) to improve the documentation regarding OSX contribution (specifically directions on installing from source with OSX). 

Given that they have not commented on the issue yet I'm not sure when this will be completed. We might just go ahead and make the changes and submit a pull request so that we can move on. 

# Looking Ahead
For our first issue involving the code base we're looking at [#910](https://github.com/mopidy/mopidy/issues/910), a request to add the option to "rescan" files. We've identified some of the areas in the code we need to look at for reference, and are trying to get a few more pointers to identify what exactly they're looking for.

In `mopidy/local/commands.py` there are two functions that we essentially want to combine to create a rescan command.
{% highlight python %}
class ClearCommand(commands.Command)
{% endhighlight %}
and
{% highlight python %}
class ScanCommand(commands.Command)
{% endhighlight %}

We believe that the rescan options needs to add files regardless if they were modified recently or not. It should look through every file and essentially do the same as an initial command (called with `ScanCommand`). As such, we've identified this code as something that could be changed:
{% highlight python %}
for track in library.begin():
            abspath = translator.local_track_uri_to_path
                (track.uri, media_dir)
            mtime = file_mtimes.get(abspath)
            if mtime is None:
                logger.debug('Missing file %s', track.uri)
                uris_to_remove.add(track.uri)
            elif mtime > track.last_modified:
                uris_to_update.add(track.uri)
            uris_in_library.add(track.uri)
{% endhighlight %}

Specifically changing:
{% highlight python %} 
elif mtime > track.last_modified:
{% endhighlight %}

to:
{% highlight python %} 
elif mtime >= track.last_modified:
{% endhighlight %}

would force scanning of files even if they've not been recently modified.

Once we get the OSX documentation issue completed we'll likely focus our efforts as a group on this code, testing it and discussing our changes with the core developers.

# Interview
Lastly we're still planning an interview with Jodal, the project creator. We've got a list of questions [here](http://still-pending.wikispaces.com/Interview+Planning) and are planning our interview for mid-march. 