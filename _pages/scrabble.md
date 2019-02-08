---
layout: page
title: Scrabble
nav: true
permalink: /scrabble/
---

### links to current rankings and ratings from the new system

#### {{ site.data.currentlists.Date }}
[Rankings](/scrabble/rankings/)<br>
[Ratings by rating](/scrabble/ratingsbyrating/)<br>
[Ratings by name](/scrabble/ratingsbyname/)<br>
[All ratings](/scrabble/allratings/)<br>

### links to previous rankings and ratings from the new system

#### {{ site.data.previouslists.Date }}
[Rankings](/scrabble/oldrankings/)<br>
[Ratings by rating](/scrabble/oldratingsbyrating/)<br>
[Ratings by name](/scrabble/oldratingsbyname/)<br>
[All ratings](/scrabble/oldallratings/)<br>

### changes to the ratings system in 2017 and 2019

In 2015-16, I reviewed the 1999 ratings system, recommended changes, had these changes adopted, and implemented the new system for 2017. Here are: the two reports analysing the old system and recommending the new system; and a description of the calculations that are carried out in the new system.

[Interim report on the review of the 1999 ratings system (pdf)](/assets/pdf/interimreport_june2.pdf)<br>
[Final report on the review of the 1999 ratings system (pdf)](/assets/pdf/finalreport.pdf)<br>
[A worked example of how the 2017 ratings system was implemented (pdf)](/assets/pdf/workedexample.pdf)

In late 2018 / early 2019, a group of New Zealand Scrabble players, including myself, undertook the review of the 2017 changes that I recommended in my report above. Here is: our final report, which was adopted on 26/1/2019; and the code for the current implementation of both the 2017 and 2019 systems.

[Final report on the review of the 2017 ratings system (pdf)](/assets/pdf/2019finalreportv2.pdf)<br>
[Reference implementation of 2017 and 2019 ratings systems (code at github)](https://github.com/stevenb-nz/nzasp-ratings)

### Words utility program

Anagrams, superstrings, substrings, supersets, subsets, 'Judge' feature, Regular Expression search, 'Word Show' study aid, Quiz study aid, Mastermind-style word game.

[Xojo version at GitHub](https://github.com/stevenb-nz/Words)

### old tournament scoring program

There are two .dmg's available for download - T-Score 1.4.4 compiled for i) [PPC Macs](/assets/dmg/T-Score1.4.4(PPC).dmg) or ii) [Intel Macs](/assets/dmg/T-Score1.4.4(Intel).dmg). The PPC version hasn't been tested as I no longer have easy access to a PPC-based machine (or even one running Rosetta).
This is the last update to the old version of T-Score - the old IDE no longer supports current machines.

### new tournament scoring program

I have just started working on a Rails implementation of a tournament scoring program. It's on [Github as nztscore](https://github.com/stevenb-nz/nztscore), but not much to see as of yet. This will probably go on the back burner now that there is a more urgent need for an updated Mac version (and a Windows version). (I.e. I will probably start work on an all-new version of the tournament scoring program using the current version of Xojo rather than Rails.)

