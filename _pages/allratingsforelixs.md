---
layout: page
title: All Ratings for Elixs
list: true
permalink: /scrabble/allratingsforelixs/
previouslink: /scrabble/oldallratingsforelixs/
---

{% assign list = site.data.currentlists.List | sort: 'Seed' %}

<table>
  <tr><th>Rank</th><th>Name</th><th>Rating</th><th class="ratingchange">Rating<br />change</th><th>Seed</th><th>Status</th><th>Wins</th><th>Games</th><th>%</th><th>Club</th></tr>
  {% for l in list %}
    <tr><td class="ranking">{% if l.Ranking > 0 %}{{ l.Ranking }}{% else %}-{% endif %}</td><td class="name">{{ l.Name }} {{ l.LifetimeAward }}</td><td class="rating">{{ l.Rating }}</td><td class="change">{{ l.RatingChange }}</td><td class="seed">{{ l.Seed }}</td><td class="status">{{ l.Status }}</td><td class="wins">{{ l.Wins }}</td><td class="games">{{ l.Games }}</td><td class="percent">{{ l.PercentText }}</td><td class="club">{{ l.Club }}</td></tr>
  {% endfor %}
</table>
