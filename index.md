---
layout: default
title: Accueil
--- 
<main>
    <p>Hello</p><br/>
    
    {% for cour in site.cours %}
    <li>{{ cour.title }}</li>
    {% endfor %}
    
    <br/><br/>
    
    {% for partner in site.data.partners %}
        {{ partner.nom }}
    {% endfor %}
    
</main>
