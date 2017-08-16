---
layout: page
title: All Ratings
list: true
permalink: /scrabble/allratings/
---

{% assign list = site.data.allratings.List | sort: 'Name' %}

<table>
  <tr><th>Name</th><th>Rating</th><th>Seeding</th><th>Status</th><th>Wins</th><th>Games</th><th>%</th></tr>
  {% for l in list %}
    <tr><td>{{ l.Name }} {{ l.LifetimeAward }}</td><td align='right'>{{ l.Rating }}</td><td align='right'>{{ l.EqualSeed }}</td><td>{{ l.Status }}</td><td align='right'>{{ l.Wins }}</td><td align='right'>{{ l.Games }}</td><td align='right'>{{ l.PercentText }}</td></tr>
  {% endfor %}
</table>
