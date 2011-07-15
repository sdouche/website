---
categories: coding, python
tags: blogofile, web
date: 2011/07/15 02:00:00
title: Nouveau blog avec Blogofile
---

Cela faisait quelques temps que cela me titillait : écrire des billets avec
mon éditeur texte habituel, et de pousser en prod avec Git. C'est le blog
de [#gitfr](http://gitfr.net/blog) qui m'a donné le courage de m'y mettre.
Et c'est maintenant chose faites. Adieu Wordpress, boujour Blogofile !

Mais qu'utilises tu ?
---------------------

Un générateur statique de site, autrement un outil qui transforme les
documents textes (format `markdown` ou `rst`) en pages html, à l'aide de
templates.

Beaucoup d'avantages :

 * Tout se trouve dans des fichiers textes.
 * Plus besoin d'être en ligne.
 * Ecriture avec Vim et non un éditeur WYSIWIG dans un navigateur.
 * Maintenance pratiquement nulle.
 * Plus de problème de sécurité.
 * Sauvegarde automatique sur GitHub.
 * Liberté totale sur l'organisation du site.
 * Hébergement simplifiée (plus besoin de PHP, Python...).
 * Et bien sûr, utilisation de Git pour gérer le site :).

En contre partie, vous n'avez plus la facilité de créer un joli site en 2
clicks de souris. La, c'est à vous de créer votre template et de développer
les services supplémentaires (affichage de tweets par exemple).

Un retour en arrière ?
----------------------

Je faisais du statique en 96 quand j'apprenais l'html 3 (ou 2 je ne sais
plus), et voila que je refais du statique en 2011, est ce vraiment
raisonnable ? Il y'a en fait un changement important qui permet ce retour
aux sources : le **cloud**. Pour disposer d'un blog, il faut un moteur de rendu
de billets, mais aussi un système de commentaires, la gestion de flux RSS,
le multi-compte, des droits et authorisations, etc.

Maintenant, vous pouvez externaliser tous les services importants :

 * les commentaires : Disqus.
 * les flux RSS : Feedburner.
 * Suivi d'activité : Google Analytics.
 * Hébergement, backup, droit et travail collaboratif : GitHub.

Cela permet de se concentrer sur l'essentiel : écrire du contenu.

Organisation
------------

Il me faut deux dépôts. Pourquoi deux ? Ce n'est pas obligatoire bien sûr,
mais j'utilise le service d'hébergement gratuit de pages statiques de
*GitHub*. Ce dernier impose des contraintes, dont le nom du dépôt et
l'emplacement des fichiers. Si vous hébergé vous même le site, un seul dépôt
est suffisant.

Pour les utilisateurs de `Git`, les *submodules* font parfaitement
l'affaire puisque la version générée se trouve dans un sous répertoire.

Un exemple ?
------------

La mise en production se fait comme suit :

    $ /path/to/blogofile/blogofile build
    $ git add _site/*
    $ git commit -m "nouveau billet sur Blogofile"
    $ git push

(sans submodules, il suffit de copier le contenu manuellement).

Et voila ! Je vous laisse imaginer les possibilités intéressantes qu'offrent
un DVCS comme *Git* ou *Hg* (si ce n'est pas le cas, vous êtes bon pour voir une
de mes présentations Git ;) pour gérer votre site.

Pourquoi Blogofile ?
--------------------

* Parce qu'il est en Python, et cela me permet de coder dans mon langage préféré
  et d'apprendre des moteurs de templates que je ne connaissais pas (*Mako* et
  bientôt *jinja2*).
 
* Parce qu'il est vraiment simple. Pas fioritures, il va à l'essentiel. Ecrire
  des controlleurs ne semblent vraiment pas dur et les quelques fonctionnalités
  dont j'avais besoin (Disqus, flux RSS et blog) sont là. Un site de base tiens
  dans 700 lignes de code Python, ce qui rend la compréhension aisé. Blogofile
  fait pour sa part 900 lignes.

* Il permet de gérer les documents drafts, le multi-auteur ou les
  transformations multiples.

* Parce que je sature un peu de Ruby. Utilisant pas mal d'outils codés en
  Ruby ces derniers temps, je commençais en avoir ras la casquette des 
  erreurs d'installation ou des messages d'erreur complètement abscons. Mais
  des outils comme Jekyll ou Toto semblent pas mal du tout, j'ai fais joué
  ma fibre Pythonienne.


Alors, si vous avez un site à monter, je vous conseille fortement de jeter un oeil
sur ces logiciels, cela peut vous intéresser ! :).
