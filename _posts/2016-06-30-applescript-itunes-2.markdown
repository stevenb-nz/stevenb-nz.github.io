---
layout: post
title:  "AppleScript (/ iTunes) 2"
date:   2016-06-30 09:05:00 +1200
categories: applescript
---
Not long after the previous post, the error occurred again. It seemed that iTunes was still responding to the AppleScript instructions out of order. So, I put code in to force it to wait after each repeat loop until some condition had been met. I.e. count the tracks in "done" before the first repeat loop, then after the first repeat loop, wait until the number of tracks in "done" equalled the initial count plus the number of tracks in "copy". And after the second repeat loop, wait until the track count of "copy" was equal to zero.

When the error still happened, I was briefly at a loss - the instructions I was sending must be being processed in order. Then I realised that the problem was that "source" is a smart playlist that depends on the contents of "done", and I wasn't leaving time after altering "done" in the first repeat loop for the contents of "source" to be updated accordingly before the third repeat loop.

I also realised that the sequence of actions I was trying to partially automate was actually in this order:

third repeat loop
[do manual stuff]
first and second repeat loops

I.e. I had kicked off the overall task by manually doing the third repeat loop first, and at the end of the process, the last thing to do would be to do the first and second repeat loops, then stop at that point.

So, I ended up stripping out all the waits and delays, and splitting the initial code into two separate scripts, as follows:

```
    tell application "iTunes"
      [existing code cut for bevity]
      repeat with x from 1 to (the (number of tracks of playlist "copy"))
        duplicate track x of playlist "copy" to playlist "done"
      end repeat
      repeat with x from (the (number of tracks of playlist "copy")) to 1 by -1
        delete track x of playlist "copy"
      end repeat
    end tell

    tell application "iTunes"
      repeat with x from 1 to (the (number of tracks of playlist "source"))
        duplicate track x of playlist "source" to playlist "copy"
      end repeat
    end tell
```

There were then no further problems.
