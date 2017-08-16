---
layout: page
title: Rankings
list: true
permalink: /scrabble/rankings/
---

{% assign list = site.data.allratings.List | where_exp:"item", 'item.Ranking > 0' | sort: 'Ranking' %}

<table>
  <tr><td>Rank</td><td>Name</td><td>Rating</td><td>Wins</td><td>Games</td><td>%</td></tr>
  {% for l in list %}
    <tr><td align='right'>{{ l.Ranking }}</td><td>{{ l.Name }} {{ l.LifetimeAward }}</td><td align='right'>{{ l.Rating }}</td><td align='right'>{{ l.Wins }}</td><td align='right'>{{ l.Games }}</td><td align='right'>{{ l.PercentText }}</td></tr>
  {% endfor %}
</table>
