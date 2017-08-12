---
layout: page
permalink: /scrabble/ratingsbyname/
---

{% assign list = site.data.allratings.List | where: 'Current', true | sort: 'Name' %}

<ul>
    {% for l in list %}
    <li>{{ l.Name }}{{ l.Rating }}</li>
    {% endfor %}
</ul>
