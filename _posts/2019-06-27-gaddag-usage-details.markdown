---
layout: post
title:  "Gaddag usage details"
date:   2019-06-27 19:03:27 +1200
categories: datastructure gaddag scrabble
---
I've started on adapting the DAG/DAWG (trie-based) data structure I used for my Scrabble analysis tool years ago, into a GADDAG. So, I've also been thinking about how I'll need to change the move-generation algorithm to match.

I think the answer is to not change the overall strategy of generating all possible moves that include playing a tile on each particular anchor square, except those moves that would also place a tile on another anchor square above or to the left of the current one (as these moves will be generated when the current square is included in a move that starts at that other anchor square). How that works in practice remains to be seen.
