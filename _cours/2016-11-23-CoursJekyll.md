---
title: Jekyll
---

# Installer Jekyll en local #
(Jekyll : Générateur de site codé en Ruby)
* Installer Ruby (sudo apt install ruby)
* Puis installer jekyll (sudo apt install jekyll)
* Lancer un server (jekyll server)
* Tester fonctionnement du site en local
 
 
* Jekyll build (créer un dossier _site qui regroupe tous les fichiers du site)
 
Permet de voir les modifications de son site sans passer par github, permet d'éviter de faire plusieurs push
 
Tous les fichiers / dossiers avec un préfixe "_" ne sont pas générés dans le site.
 
## Créer dossier _includes ##
* On créer le dossier _includes (mkdir _includes)
* On créer les fichiers nécéssaires dans le répertoire includes(touch head.html / header.html / footer.html)
* On copie / colle le code
* On ajoute le code suivant dans le index.html : {% include head.html %} pour chaque fichiers
 
## Créer un layout de notre site ##
(C'est la structure du site)
* Créer un nouveau répertoire _layouts
* A l'intérieur créer un fichier default.html
* Dans ce fichier, copié l'intégralité du code et à la place du contenu mettre {{ content}}
* Dans le fichier index.html mettre le code suivant:
(---layout: default--- + le contenu)

## Créer un menu ##
* lien vers fichier.md mettre .html

#### Menu dynamique ####
Menu dynamique en fonction du nombre de page avec boucle Jekyll.

Code:
            * {% for page in site.pages %}
            <li><a href="{{ page.url }}">{{ page.title }}</a></li>
            {% endfor %} 
            
## Faire un blog ##
Commencer par créer des billets de posts

ex: 2016-11-23-article.md

Puis ajouter boucle de lecture sur la page:

    *  {% for post in site.posts limit:3 %}
    <a href="{{ post.url }}">{{ post.title }}</a>
    <p>{{ post.excerpt }}</p>
    {% endfor %}

## Répertoire _assets ##
On l'utilise pour ranger:
    * css
    * img
    * favicon
    * fonts
    * scripts