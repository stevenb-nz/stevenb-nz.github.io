---
layout: page
title: All Ratings by position
oldlist: true
permalink: /scrabble/oldallratingsbyposition/
currentlink: /scrabble/allratingsbyposition/
---

{% assign list = site.data.previouslists.List | sort: 'Seed' %}

<table>
  <tr><th>Name</th><th>Rating</th><th>Seeding</th><th>Status</th><th>Wins</th><th>Games</th><th>%</th></tr>
  {% for l in list %}
    <tr><td class="name">{{ l.Name }} {{ l.LifetimeAward }}</td><td class="rating">{{ l.Rating }}</td><td class="seeding">{{ l.EqualSeed }}</td><td class="status">{{ l.Status }}</td><td class="wins">{{ l.Wins }}</td><td class="games">{{ l.Games }}</td><td class="percent">{{ l.PercentText }}</td></tr>
  {% endfor %}
</table>
