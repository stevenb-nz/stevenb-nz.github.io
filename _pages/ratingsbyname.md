---
layout: page
title: Ratings by name
list: true
permalink: /scrabble/ratingsbyname/
---

{% assign list = site.data.allratings.List | where: 'Current', true | sort: 'Name' %}

<table>
  <tr><td>Name</td><td>Rating</td><td>Seeding</td><td>Status</td><td>Wins</td><td>Games</td><td>%</td></tr>
  {% for l in list %}
    <tr><td>{{ l.Name }} {{ l.LifetimeAward }}</td><td align='right'>{{ l.Rating }}</td><td align='right'>{{ l.EqualSeed }}</td><td>{{ l.Status }}</td><td align='right'>{{ l.Wins }}</td><td align='right'>{{ l.Games }}</td><td align='right'>{{ l.PercentText }}</td></tr>
  {% endfor %}
</table>
