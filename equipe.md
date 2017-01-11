---
title: Equipe
layout: page
---

{% for ligue in site.data.clubs %}
    {% for club in ligue[1] %}
        {{ club.name }}
    {% endfor %}
{% endfor %}