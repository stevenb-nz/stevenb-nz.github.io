---
layout: page
permalink: /scrabble/rankings/
---

{% assign list = site.data.allratings.List | where_exp:"item", 'item.Ranking > 0' | sort: 'Ranking' %}

<ul>
    {% for l in list %}
    <li>{{ l.Name }}{{ l.Rating }}</li>
    {% endfor %}
</ul>
