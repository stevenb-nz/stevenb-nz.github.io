---
layout: page
title: Rankings
list: true
permalink: /scrabble/rankings/
---

{% assign list = site.data.allratings.List | where_exp:"item", 'item.Ranking > 0' | sort: 'Ranking' %}

<table>
  <tr><th>Rank</th><th>Name</th><th>Rating</th><th>Wins</th><th>Games</th><th>%</th></tr>
  {% for l in list %}
    <tr><td align='right'>{{ l.Ranking }}</td><td>{{ l.Name }} {{ l.LifetimeAward }}</td><td align='right'>{{ l.Rating }}</td><td align='right'>{{ l.Wins }}</td><td align='right'>{{ l.Games }}</td><td align='right'>{{ l.PercentText }}</td></tr>
  {% endfor %}
</table>
