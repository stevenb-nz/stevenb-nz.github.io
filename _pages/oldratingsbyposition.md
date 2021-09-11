---
layout: page
title: Ratings by position
oldlist: true
permalink: /scrabble/oldratingsbyposition/
currentlink: /scrabble/ratingsbyposition/
---

{% assign list = site.data.previouslists.List | where: 'Current', true | sort: 'Seed' %}

<table>
  <tr><th>Rank</th><th>Name</th><th>Rating</th><th class="ratingchange">Rating<br />change</th><th>Wins</th><th>Games</th><th>%</th></tr>
  {% for l in list %}
    <tr><td class="ranking">{% if l.Ranking > 0 %}{{ l.Ranking }}{% else %}-{% endif %}</td><td class="name">{{ l.Name }} {{ l.LifetimeAward }}</td><td class="rating">{{ l.Rating }}</td><td class="change">{{ l.RatingChange }}</td><td class="wins">{{ l.Wins }}</td><td class="games">{{ l.Games }}</td><td class="percent">{{ l.PercentText }}</td></tr>
  {% endfor %}
</table>
