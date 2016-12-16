---
layout: page
title: Equipe
---

{% for ligue in site.data.clubs %}
    {% for club in ligue[1] %}
        {{ club.name }}
    {% endfor %}
{% endfor %}