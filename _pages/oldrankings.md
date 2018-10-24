---
layout: page
title: Rankings
oldlist: true
permalink: /scrabble/oldrankings/
currentlink: /scrabble/rankings/
---

{% assign list = site.data.previouslists.List | where_exp:"item", 'item.Ranking > 0' | sort: 'Ranking' %}

<table>
  <tr><th>Rank</th><th>Name</th><th>Rating</th><th class="ratingchange">Rating<br />change</th><th>Wins</th><th>Games</th><th>%</th></tr>
  {% for l in list %}
    <tr><td class="ranking">{{ l.Ranking }}</td><td class="name">{{ l.Name }} {{ l.LifetimeAward }}</td><td class="rating">{{ l.Rating }}</td><td class="change">{{ l.RatingChange }}</td><td class="wins">{{ l.Wins }}</td><td class="games">{{ l.Games }}</td><td class="percent">{{ l.PercentText }}</td></tr>
  {% endfor %}
</table>
