---
layout: post
title:  border for xy grids
date:   2019-09-09 21:12:58 +1200
categories: games arrays
---
I was recently reminded that when coding any game where the play area is a rectangle of rows and columns, it is a good idea to represent this not as a bare x by y array, but by an x+1 by y+1 array of whatever slots, cells, or squares characterise the game in question. I.e. define the border of the play area as cells with a defined value, not as extra conditionals or potential out-of-range errors.

For example, if one is writing a 'four in a row'-type game, testing for a win state is a matter of starting from the last-played token, and going back and forth in each direction to firstly find one end of a line of matching tokens, then count from there to the other end. On, for example, a 6 by 7 play area, if an 8 by 9 array is used, then the end of a line is defined solely by a cell not containing the kind of token being tested for. If a 6 by 7 array is used, a line could end with such a cell, or it could end whenever a line matching tokens reached an edge of the array, which would need to be tested for x< or x> and/or y< or y> conditionals.
