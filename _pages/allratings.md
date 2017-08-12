---
layout: page
permalink: /scrabble/allratings/
---

{% assign allratings = site.data.allratings | sort: 'Name' %}

<ul>
    {% for a in allratings %}
    <li>{{ a.Name }}{{ a.Rating }}</li>
    {% endfor %}
</ul>
