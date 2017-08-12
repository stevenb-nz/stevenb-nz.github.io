---
layout: page
permalink: /scrabble/ratingsbyname/
---

{% assign allratings = site.data.allratings | where: 'Current', true | sort: 'Name' %}

<ul>
    {% for a in allratings %}
    <li>{{ a.Name }}{{ a.Rating }}</li>
    {% endfor %}
</ul>
