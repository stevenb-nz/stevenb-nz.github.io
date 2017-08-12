---
layout: page
permalink: /scrabble/ratingsbyrating/
---

{% assign list = site.data.allratings.List | where: 'Current', true | sort: 'Seed' %}

<table>
  {% for l in list %}
    <tr><td>{{ l.Name }}</td><td>{{ l.Rating }}</td></tr>
  {% endfor %}
</table>
