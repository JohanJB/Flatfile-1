---
title: Accueil
layout: default
---

<main>
    <p>Hello</p><br/>
    
    {% for cour in site.cours %}
    <li>{{ cour.title }}</li>
    {% endfor %}
    
    {% for partner in site.data.partners %}
    <li>{{ partner.nom }} / {{ partner.github }}</li>
    {% endfor %}
    
</main>
