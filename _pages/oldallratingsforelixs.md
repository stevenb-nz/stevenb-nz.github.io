---
layout: page
title: Ratings for Elixs
oldlist: true
permalink: /scrabble/oldallratingsforelixs/
currentlink: /scrabble/allratingsforelixs/
---

{% assign list = site.data.previouslists.List | sort: 'Seed' %}

<table>
  <tr><th>Rank</th><th>Name</th><th>Rating</th><th class="ratingchange">Rating<br />change</th><th>Seeding</th><th>Status</th><th>Wins</th><th>Games</th><th>%</th></tr>
  {% for l in list %}
    <tr><td class="ranking">{% if l.Ranking > 0 %}{{ l.Ranking }}{% else %}-{% endif %}</td><td class="name">{{ l.Name }} {{ l.LifetimeAward }}</td><td class="rating">{{ l.Rating }}</td><td class="change">{{ l.RatingChange }}</td><td class="seeding">{{ l.EqualSeed }}</td><td class="status">{{ l.Status }}</td><td class="wins">{{ l.Wins }}</td><td class="games">{{ l.Games }}</td><td class="percent">{{ l.PercentText }}</td></tr>
  {% endfor %}
</table>
