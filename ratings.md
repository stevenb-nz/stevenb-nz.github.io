---
layout: page
permalink: /scrabble/ratings/
---

{% assign allratings = site.data.allratings.ratings | where: 'current', true | sort: 'seed' %}

<ul>
    {% for a in allratings %}
    <li>{{ a.name }}{{ a.rating }}</li>
    {% endfor %}
</ul>
