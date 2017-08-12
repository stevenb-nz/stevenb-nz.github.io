---
layout: page
permalink: /scrabble/allratings/
---

{% assign list = site.data.allratings.List | sort: 'Name' %}

<ul>
    {% for l in list %}
    <li>{{ l.Name }}{{ l.Rating }}</li>
    {% endfor %}
</ul>
