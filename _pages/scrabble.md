---
layout: page
title: Scrabble
nav: true
permalink: /scrabble/
---

### old tournament scoring program

There are two .dmg's available for download - T-Score 1.4.4 compiled for i) [PPC Macs](/assets/dmg/T-Score1.4.4(PPC).dmg) or ii) [Intel Macs](/assets/dmg/T-Score1.4.4(Intel).dmg). The PPC version hasn't been tested as I no longer have easy access to a PPC-based machine (or even one running Rosetta).
This is the last update to the old version of T-Score - the old IDE no longer supports current machines.

### new tournament scoring program

I have just started working on a Rails implementation of a tournament scoring program. It's on [Github as nztscore](https://github.com/stevenb-nz/nztscore), but not much to see as of yet. This will probably go on the back burner now that there is a more urgent need for an updated Mac version (and a Windows version). (I.e. I will probably start work on an all-new version of the tournament scoring program using the current version of Xojo rather than Rails.)

### implementation of new ratings system

I have reviewed the old ratings system, recommended changes, had these changes adopted, and implemented the new system. Here are the two reports, analysing the old system and recommending the new system; a description of the calculations that are carried out in the new system; and the code for the current implementation of the new system.

[Interim report on the ratings system review (pdf)](/assets/pdf/interimreport_june2.pdf)<br>
[Final report on the ratings system review (pdf)](/assets/pdf/finalreport.pdf)<br>
[A worked example of how the new ratings system is currently implemented (pdf)](/assets/pdf/workedexample.pdf)<br>
[Reference implementation of new ratings system (code at github)](https://github.com/stevenb-nz/nzasp-ratings)

### links to current rankings and ratings from the new system

#### {{ site.data.currentlists.Date }}
[Rankings](/scrabble/rankings/)<br>
[Ratings by rating](/scrabble/ratingsbyrating/)<br>
[Ratings by name](/scrabble/ratingsbyname/)<br>
[All ratings](/scrabble/allratings/)<br>
