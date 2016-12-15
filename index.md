---
layout: default
title: Accueil
--- 
<main>
    <p>Hello</p><br/>
    
    {% for cours in site.cours %}
    <li>{{ cours.title }}</li>
    {% endfor %}
    
    {% for equipe in site.data.partners %}
    <li>{{ equipe.nom }} / {{ equipe.github }}</li>
    {% endfor %}
    
</main>
