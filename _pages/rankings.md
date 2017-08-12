---
layout: page
permalink: /scrabble/rankings/
---

{% assign list = site.data.allratings.List | where_exp:"item", 'item.Ranking > 0' | sort: 'Ranking' %}

<table>
  {% for l in list %}
    <tr><td>{{ l.Name }}</td><td>{{ l.Rating }}</td></tr>
  {% endfor %}
</table>
