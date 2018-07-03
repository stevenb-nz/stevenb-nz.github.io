---
layout: page
title: Ratings by rating
list: true
permalink: /scrabble/ratingsbyrating/
---

{% assign list = site.data.allratings.List | where: 'Current', true | sort: 'Seed' %}

<table>
  <tr><th>Change</th><th>Rank</th><th>Name</th><th>Rating</th><th>Seeding</th><th>Status</th><th>Wins</th><th>Games</th><th>%</th></tr>
  {% for l in list %}
    {% assign changeint = l.Seed | minus:l.LastSeed %}
    {% if changeint < 0 %}
      {% assign changechar = "+" %}
    {% elsif changeint > 0 %}
      {% assign changechar = "-" %}
    {% else %}
      {% assign changechar = "" %}
    {% endif %}
    <tr><td class="change">{{ changechar }}</td><td class="ranking">{% if l.Ranking > 0 %}{{ l.Ranking }}{% else %}-{% endif %}</td><td class="name">{{ l.Name }} {{ l.LifetimeAward }}</td><td class="rating">{{ l.Rating }}</td><td class="seeding">{{ l.EqualSeed }}</td><td class="status">{{ l.Status }}</td><td class="wins">{{ l.Wins }}</td><td class="games">{{ l.Games }}</td><td class="percent">{{ l.PercentText }}</td></tr>
  {% endfor %}
</table>
