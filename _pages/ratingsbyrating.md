---
layout: page
permalink: /scrabble/ratingsbyrating/
---

{% assign list = site.data.allratings.List | where: 'Current', true | sort: 'Seed' %}

<ul>
    {% for l in list %}
    <li>{{ l.Name }}{{ l.Rating }}</li>
    {% endfor %}
</ul>
