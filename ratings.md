---
layout: page
permalink: /scrabble/ratings/
---

{% assign allratings = site.data.allratings.ratings | where: 'Current', true | sort: 'Seed' %}

<ul>
    {% for a in allratings %}
    <li>{{ a.name }}{{ a.rating }}</li>
    {% endfor %}
</ul>
