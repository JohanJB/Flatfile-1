---
title: Accueil
layout: default
---

<main>
    <p>Hello</p><br/>
    
    {% for cour in site.cours %}
    <li>{{ cour.title }}</li>
    {% endfor %}
    
    {% for product in site.products %}
    {% include product.html %}
    {% endfor %}
    
</main>
