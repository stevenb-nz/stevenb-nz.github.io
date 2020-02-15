---
layout: post
title:  back-combining DAWG into GADDAG
date:   2020-02-15 23:34:25 +1300
categories: data-structures scrabble
---
While trying to get a gaddag working, it has ocurred to me that if *all* the permutations of prefix and suffix are included for each work, then the new sub-tree of the gaddag that has the pivot symbol as its root can be used the same way as a stand-alone dawg would be.

Currently, for example, the word CAT would be in the gaddag as C`AT, AC`T, AND TAC`. The remaining possibility (`CAT) is not required for the finding of Scrabble plays, but if it is included, the tree with ` at its root is a DAWG of all the words in the gaddag, and can be used for simple yes/no - is-this-a-word? searches.

Also, if the gaddag is compressed by starting at all the leaf nodes, and combining identical endings working back up a level at a time (rather than starting from the root nodes, and combining the identical bits of the same length), the extra copy of all the words will be almost entirely compressed away.
