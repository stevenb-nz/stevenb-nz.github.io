---
layout: post
title:  "Ratings system software II"
date:   2018-02-25 02:02:56 +1300
categories: scrabble xojo
---
When I made the previous post on this topic, at the end of October, the most recent commit was a stub (i.e. a menuItem with an empty function in the handler) for an export custom list facility.

Over the next three weeks, I got a dialog going for entering and verifying the parameters for a custom list, but then set this aside. The next few things (through to the end of December) were to create a stub for importing a .TOU file (as used by AuPair), add an 'edit name' button to the 'players' tab, make the first lists to include new lifetime awards be lists as at the last day of the year for which they are awarded rather than the first list of the next year, change the provisional rating calculation to something closer to a performance rating, add a button to amend a tournament name, apply a .trim to all string entry, change game expectancy formula to be clearer and more succinct, and get back to the export .TOU file function. I also wrote up a 'worked example' of calculating ratings in the new system.

Starting in January once I'd done as much on 'Advent of Code' as was useful to me, I added an 'export awards' function, finished the convert .tou file function, redesigned the dialog of exporting custom lists to make it simpler and more flexible, and finished implementing the export custom list function.

So, the two items mentioned in the last post that I haven't attended to yet are the trial compilation of a Windows version, and figuring out a more obvious way to enter the details for two tournaments that are being rated as if they are one tournament. There may well be other things that end up being higher priorities than these, as neither of them is stopping any shows. The provisional rating calculation needs a further tweak, but this will have to wait to be implemented as a recommendation of the review at the end of this year.
