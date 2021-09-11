---
layout: page
title: Ratings by name
list: true
permalink: /scrabble/ratingsbyname/
previouslink: /scrabble/oldratingsbyname/
---

{% assign list = site.data.currentlists.List | where: 'Current', true | sort: 'Name' %}

<table>
  <tr><th>Name</th><th>Rating</th><th>Wins</th><th>Games</th><th>%</th></tr>
  {% for l in list %}
    <tr><td class="name">{{ l.Name }} {{ l.LifetimeAward }}</td><td class="rating">{{ l.Rating }}</td><td class="wins">{{ l.Wins }}</td><td  class="games">{{ l.Games }}</td><td class="percent">{{ l.PercentText }}</td></tr>
  {% endfor %}
</table>
