---
layout: page
permalink: /scrabble/ratings/
---

{% assign allratings = site.data.allratings | where: 'Current', true | sort: 'Seed' %}

<ul>
    {% for a in allratings %}
    <li>{{ a.Name }}{{ a.Rating }}</li>
    {% endfor %}
</ul>
