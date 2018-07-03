---
layout: page
title: Rankings
list: true
permalink: /scrabble/rankings/
---

{% assign list = site.data.allratings.List | where_exp:"item", 'item.Ranking > 0' | sort: 'Ranking' %}

<table>
  <tr><th>Change</th><th>Rank</th><th>Name</th><th>Rating</th><th>Wins</th><th>Games</th><th>%</th></tr>
  {% for l in list %}
    {% assign changeint = l.Seed | minus:l.LastSeed %}
    {% if changeint < 0 %}
      {% assign changechar = "+" %}
    {% elsif changeint > 0 %}
      {% assign changechar = "-" %}
    {% else %}
      {% assign changechar = "" %}
    {% endif %}
    <tr><td class="change">{{ changechar }}</td><td class="ranking">{{ l.Ranking }}</td><td class="name">{{ l.Name }} {{ l.LifetimeAward }}</td><td class="rating">{{ l.Rating }}</td><td class="wins">{{ l.Wins }}</td><td class="games">{{ l.Games }}</td><td class="percent">{{ l.PercentText }}</td></tr>
  {% endfor %}
</table>
