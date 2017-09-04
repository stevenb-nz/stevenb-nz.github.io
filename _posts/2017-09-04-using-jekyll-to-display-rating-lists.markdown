---
layout: post
title:  "Using Jekyll to display rating lists"
date:   2017-09-04 20:20:32 +1200
categories: jekyll scrabble
---
At the first Kapiti community hackathon a couple of months ago, I started work on the idea of adding a bot to the NZ Scrabble Slack I administer that would provide ratings information. To that end, I added to my existing software implementing the ratings system, the ability to export a JSON file of all current ratings information (i.e. as at the conclusion of the immediately previous tournament). The person I was working with produced a basic API to either import or serve up this information in response to HTTP requests.

Taking that approach any further went on the back burner, and then I thought to investigate whether I could use Jekyll to produce the four standard rating and ranking list from the JSON file. It turned out to be fairly straightforward to drop the JSON in Jekyll's _data folder, and use a different filter and sort on each of the four pages (after making a few changes to the the structure and content of the JSON produced by the ratings app). (See: [http://stevenb-nz.github.io/scrabble/](http://stevenb-nz.github.io/scrabble/) ).

With a few more tweaks to Jekyll, such as getting all the pages working from a _pages folder rather than the site root, tweaking which pages appear in the site navigation, and a bit of CSS, it all works quite nicely now.
