---
layout: page
title: Ratings by rating
list: true
permalink: /scrabble/ratingsbyrating/
---

{% assign list = site.data.allratings.List | where: 'Current', true | sort: 'Seed' %}

<table>
  <tr><th>Rank</th><th>Name</th><th>Rating</th><th>Seeding</th><th>Status</th><th>Wins</th><th>Games</th><th>%</th></tr>
  {% for l in list %}
    <tr><td class="ranking">{% if l.Ranking > 0 %}{{ l.Ranking }}{% else %}-{% endif %}</td><td class="name">{{ l.Name }} {{ l.LifetimeAward }}</td><td class="rating">{{ l.Rating }}</td><td class="seeding">{{ l.EqualSeed }}</td><td class="status">{{ l.Status }}</td><td class="wins">{{ l.Wins }}</td><td class="games">{{ l.Games }}</td><td class="percent">{{ l.PercentText }}</td></tr>
  {% endfor %}
</table>
