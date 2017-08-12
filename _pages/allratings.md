---
layout: page
permalink: /scrabble/allratings/
---

{% assign list = site.data.allratings.List | sort: 'Name' %}

<table>
  {% for l in list %}
    <tr><td>{{ l.Name }}</td><td>{{ l.Rating }}</td></tr>
  {% endfor %}
</table>
