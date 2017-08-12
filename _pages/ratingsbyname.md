---
layout: page
permalink: /scrabble/ratingsbyname/
---

{% assign list = site.data.allratings.List | where: 'Current', true | sort: 'Name' %}

<table>
  {% for l in list %}
    <tr><td>{{ l.Name }}</td><td>{{ l.Rating }}</td></tr>
  {% endfor %}
</table>
