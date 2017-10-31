---
layout: post
title:  "Ratings system software"
date:   2017-10-31 20:05:08 +1300
categories: scrabble xojo
---

I've finished everything required for me to use this software to administer the ratings system, and have added a couple of small extras (most recently, a couple of ways to display the club affiliation information that gets imported with tournament entries).

The next-most-urgent items are either to do with automated rare tasks that I can now do manually (by accessing the database from the command line), or with making it easier for someone else to take over the Ratings Manager job from me sometime in the future.

In the second category, I need to finish writing the implementation guide (so that someone else could understand how to use this implementation, or perhaps reimplement the functionality in some other language or framework). I also need to do a trial compilation to Windows, in case someone needs a Windows executable to take over from me.

In the first category, I need to provide for a suitably generic way to produce a list of qualifiers for a representative tournament. I've already provided a specific implementation for the current criteria for being selected for the NZ World Champs team (as this has stayed the same for a number of years), but not for being selected for the NZ Trans-Tasman team (as this is likely to change along with the format of the competition). The generic list would involve specifying the first tournament to be included in the qualifying period (assuming the current tournament to be the last), the number of games to have been played in this qualifying period, and the number of major tournaments (Masters or Nationals) to have been played out of the previous N majors.

I also need to provide a more intuitive way to enter two one-day tournaments that are to be rated together (this may go along with more ways to input and edit tournament details for all tournaments).
