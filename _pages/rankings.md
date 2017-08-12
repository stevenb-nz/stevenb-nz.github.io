---
layout: page
permalink: /scrabble/rankings/
---

{% assign allratings = site.data.allratings | where_exp:"item", 'item.Ranking > 0' | sort: 'Ranking' %}

<ul>
    {% for a in allratings %}
    <li>{{ a.Name }}{{ a.Rating }}</li>
    {% endfor %}
</ul>
