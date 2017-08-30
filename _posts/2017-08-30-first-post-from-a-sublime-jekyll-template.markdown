---
layout: post
title: First post from a sublime-jekyll template
date: 2017-08-30 13:19:51 +1200
categories: jekyll
---
The title should be fairly self-explanatory - just getting used to using this before starting a couple of more substantial posts.

I may need to type the double-quotes around the title when prompted for the title - just testing that now. No, not the problem.

The problem is that the insert datetime command in sublime-jekyll doesn't include the +1200 timezone at the end of the datetime, so the post was published, but wasn't going to appear until 13:19:51 server time, whenever that is (certainly still in the future right now). Maybe it's a setting, or maybe it's a change that could be made to sublime-jekyll - will investigate.

Okay, the default datetime Python format string looks like this: "%Y-%m-%d %H:%M:%S"<br/>
Overriding it like this to try to include the timezone offset at the end doesn't work: "%Y-%m-%d %H:%M:%S %z"<br/>
Overriding it with the literal offset, like this, does work: "%Y-%m-%d %H:%M:%S +1200"<br/>
I'll just need to remember to change it to +1300 when daylight savings starts.
