---
layout: post
title:  "AppleScript (/ iTunes)"
date:   2016-06-18 21:40:00 +1200
categories: applescript
---
In iTunes, I have set up a group of playlists which let me manually batch-process my library. There's one smart playlist, which is the source of each batch (a random selection of tracks that I haven't marked as 'done' yet (by copying them to the done playlist)), and two ordinary playlists, one of which is a copy of the current contents of the source playlist, and the other of which is the 'done' playlist.

So, before yesterday, I would start with an empty 'done' playlist, I'd copy the 'source' playlist to the 'copy' playlist, I'd manually re-order the songs in 'copy', I'd run an applescript from the scripts menu which would reassign certain properties for that group of songs based on the order they were now in, I'd copy 'copy' to 'done' (which would force the 'source' playlist to choose a new random selection), and I'd delete the current 'copy', then go back to copying the new selection in 'source' to 'copy'.

Yesterday, having done a bit of this, I decided to try extending the applescript (which I'd written some years ago) to include a few more of the above manual steps, namely the copy contents of 'copy' to 'done', delete contents of 'copy', and copy contents of 'source' to 'copy' steps.

After a bit of mucking around trying to record my manual process (didn't happen), then trying to figure out the appleScript equivalent of 'select all' and copy selection (or each member of selection), I eventually ended up with:

```
    tell application "iTunes"
      [existing code cut for bevity]
      repeat with x from 1 to (the (number of tracks of playlist "copy"))
        duplicate track x of playlist "copy" to playlist "done"
      end repeat
      repeat with x from (the (number of tracks of playlist "copy")) to 1 by -1
        delete track x of playlist "copy"
      end repeat
      repeat with x from 1 to (the (number of tracks of playlist "source"))
        duplicate track x of playlist "source" to playlist "copy"
      end repeat
    end tell
```

The loops change from ascending values to decending and back to ascending so that the tracks are copied in the order they are in (and not reversed), but deleting tracks doesn't affect the track numbers of the tracks yet to be deleted. This worked fine running the script from Script Editor and observing the results in iTunes, but as soon as I saved the script, and invoked it from the iTunes script menu instead, I ran into problems.

For the sake of a simple example, if there had been only 5 tracks in each batch, then 'copy' would have had a1,a2,a3,a4,a5 to start with, these get copied to the end of 'done', deleted from 'copy', and b1,b2,b3,b4,b5 get copied into 'copy' from done. But running from the scripts menu, what actually happened was - a1-a5 got copied to 'done', then 'copy' would end up containing something like a1,b2,b3,b4,b5 or a1,a2,b3,b4,b5. Obviously, it 'tells' the various repeat requests to iTunes, and then starts on the second copy before iTunes has finished the deleting. But the exact details of how it goes wrong to the extent it does, but still ends with the right number of tracks in the right places (albeit from the wrong playlists) is still a mystery to me.

I seem to have fixed the problem by inserting a 'delay 1' line for the final repeat loop, then changing it to 'delay 0', which still works. If it goes wrong again, it'll be easy enough to spot, and at that point I'd put some more time into figuring out exactly what is happening. But that's not an immediate priority.
