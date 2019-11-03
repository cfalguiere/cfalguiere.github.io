---
title: "Un nouveau cycle commence"
categories:
  - Blog
tags:
  -
excerpt: Le blog se poursuit sur ce nouveau support
classes: wide
assets_folder: /assets/
---

Me voilà de retour après une longue absence. Un nouveau blog, avec de nouveaux sujets et plus simple à gérer pour moi.

{% assign author = site.data.authors[page.author] %}
{% assign wp_url = author.url_wordpress %}
Ce site prend la suite de mon ancien site [Claude au pays des 4J]({{ wp_url }}) sous Wordpress.

Wordpress est un outil utile pour gérer des sites pros, et en particulier quand on ne maîtrise pas trop la création d'un site Web. Ce sont les contraintes d'hébergement et le peu d'envie de gérer un serveur Web qui m'ont amenée à choisir Blogger puis Wordpress.

Au bout d'un moment, j'étais fatiguée des galères pour présenter du code correctement dans Wordpress. Alors bien sûr, il y a des plugins mais tout ça pose toujours des tas de contraintes. L'autre souci plus récent est l'apparition de publicités dans les pages.

J'avais fini par faire beaucoup de contenu dans les Wiki ou les Github Pages de mes repositories Github plutôt que dans mon blog.

Pourquoi ?
- Je peux écrire les posts en Markdown et passer en HTML si je veux un rendu plus précis
- l'intégration du code est plus simple
- je peux choisir l'éditeur de mon choix
- je peux travailler hors ligne ou gérer des branches sur plusieurs projets pour des travaux longs
- faire des pages basées sur un template et des données est plus facile
- je peux automatiser certaines tâches avec mes outils habituels

Bien sûr il y a quelques inconvénients
- pas de Wysiwyg, il faut installer jekyll et utiliser Jekyll serve pour faire le rendu
- les styles fournis par Github ne sont pas extraordinaires

J'aurais pu creuser la configuration de site Wordpress, tester des plugins et essayer d'apprendre PHP. J'ai préféré essayer autre chose.

Entre temps, j'avais essayé une autre option pour un autre site lié à mes ateliers au Coder Dojo, [Toutenalgo, le petit algonaute](http://www.toutenalgo.fr). Ce site est fait avec [Jekyll](https://jekyllrb.com/) et le thème  [Minimal Mistakes](https://mmistakes.github.io/minimal-mistake). Ce thème est bien plus complet et esthétique que les thèmes Github. Github Pages accepte tout site en Jekyll et le site peut être servi par Github. Il existe d'autres options simples comme le copier en site statique sur S3.

Ce site est fait de la même manière, Jekyll [Jekyll](https://jekyllrb.com/) et le thème  [Minimal Mistakes](https://mmistakes.github.io/minimal-mistake) et un habillage un peu différent.

J'espère mettre beaucoup de code dans ce site et quelques autres trucs. En attendant, il recence [diverses présentations](presentations/) faites depuis 2014.
