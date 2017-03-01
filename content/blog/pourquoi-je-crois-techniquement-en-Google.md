---
title: "Pourquoi je crois (techniquement) en Google"
date: "2014-12-15T07:29:44+01:00"
categories: [ "rumination" ]
tags: [ "google", "coding", "javascript", "dart" ]
slug: "pourquoi-je-crois-techniquement-en-google"
---

Si cela fait des années que je n'espère plus rien de Google sur le plan des
libertés, je reste curieux de tout ce qu'ils font sur le plan technique,
notamment pour Internet. Car c'est pour moi la seule (grosse) boite qui
fait avancer sérieusement les choses. Explication.

La différence de business model
-------------------------------

Pour expliquer mon point de vue, il faut d'abord parler de *business model* :

- Quel est le *business model* de Microsoft ? Vous faire utiliser les produits
  Microsoft.
- Quel est le *business model* d'Apple ? Vous faire utiliser les produits
  Apple.
- Quel est le *business model* de Facebook ? Vous faire utiliser les produits
  Facebook.
- Et quel est le *business model* de Google ?

Arrêtez vous 30 secondes pour répondre à cette question. Ça y est ? Alors
reprenons. Son *business model* est de vous faire **utiliser Internet**. Bien sûr,
c'est mieux au travers de leurs services mais cela n'est pas une obligation.
On l'oublie souvent, mais le CA de Google vient en **grande partie** de la
publicité (90% du CA, 30% du marché mondial de la publicité en ligne, loin
devant Facebook et Yahoo). Ils gagnent donc de l'argent quand les gens
vont sur le Net. Et plus l'expérience de navigation est plaisante, plus Google
gagne de l'argent. Je me souviens d'un tweet qui m'avait marqué : «Quand
Internet va 1/10 de seconde plus vite, Google gagne 1 milliard de dollars de
plus». Je ne peux pas valider son contenu mais j'ai trouvé à l'époque cette réflexion
intéressante.

Cela explique toutes les initiatives de Google pour améliorer le Net, non pas
par philanthropie, mais par besoin. Regardons de plus près ce que Google a fait.
Voici une petite liste de mémoire (je pense que l'on peut en rajouter bien plus) :

- La mise à disposition gratuite de CDN pour les librairies Javascript les
  plus populaires ainsi qu'une longue liste de fontes.
- Le financement de nombreux Logiciels Libres par l'intermédiaire du Google
  Summer of Code.
- Le développement du Javascript avec le projet v8. Rappelez vous l'état
  de délabrement du langage avant que Google s'en charge (un navigateur
  moderne va plus de 100x plus vite que Firefox 2 coté JS).
- Le financement de successeur de HTTP1 (SPDY et HTTP2).
- Le financement des «Web Components» pour standardiser le développement Web.
- Le financement de 2 langages, un backend (Go), l'autre frontend (Dart).
- Le financement du framework AngularJS.
- Le financement de la fibre optique dans plusieurs régions des USA.
- La mise à disposition gratuite d'une forge (Google Developers).
- La mise à disposition gratuite des formats WebM et WebP, développés en
  interne.
- La mise à disposition gratuite d'une suite bureautique.
- La mise à disposition gratuite d'un large espace de stockage cloud.
- Le développement d'un «OS Internet», ChromeOS, pour disposer d'un
  notebook pas cher.

Sans compter le moteur de recherche qui a révolutionné l'utilisation du Net.
Bref, je m'arrête la mais vous voyez le tableau. Google veut votre confort,
car elle gagnera encore plus d'argent. C'est pour raison que Google est bien
plus dangereux á mes yeux que Microsoft, ce dernier se bornant à vous
bloquer dans leur techno. Il suffisait donc de trouver mieux (merci Linux
et le Logiciel Libre) pour facilement se libérer. Mais pour Google, c'est
une autre histoire. Qui aide autant les développeurs qu'eux ? Facebook ?
Apple ? Mozilla ?

Maintenant regardons de plus près le dernier rebondissement : Angular 2.
Suite à l'annonce de la nouvelle version du framework (qui ne sortira qu'en
2016), des cris d'effroi et de rage se sont fait entendre : Google
se fout de la gueule du monde en cassant la compatibilité et rendra
orphelin tous les utilisateurs de la version 1. Alors prenons un peu de recul.

Petite note
-----------

Tout d'abord, il est intéressant de noter que les projets techniques sont
financés par Google, mais pas «dirigés» par elle. AngularJS est autonome,
comme Go ou Dart. Savez vous ce qu'on dit les développeurs de Go quand la
1.0 est sortie ? «Maintenant, on va tenter de **convaincre** en interne». Bien
que financé par Google (les 3/4 des core devs sont chez eux), cela ne veut
pas dire que cela rentre dans un projet global. Google finance «pour voir»,
et utilisera potentiellement le projet. C'est pour moi sa grande force.

De GWT à Angular 2
------------------

Voici, toujours de tête, un petit timeline :

- 2006 : GWT 1.0, un framework Java pour faire du développement Web.
- 2008 : Chrome 1.0 / v8 1.0.
- 2009 : AngularJS 1.0.
- 2011 : Disponibilité des technologies PNaCI / PNaCI.
- 2013 : Dart 1.0, tout nouveau langage pour le Web.
- 2013 : Parallèlement à Dart, travail sur les «Web Components» avec Dart Web UI.
- 2013 : Normalisation des «Web Components».
- 2013 : Lancement de Polymer, librairie de «Web Components» normalisés.
- 2013 : Lancement d'AngularDart, le pendant Dart d'AngularJS.
- 2013 : GWT est géré par la communauté (Google continue de payer des core devs).
- 2014 : Dart est normalisé (ECMA-408)
- 2016 : Angular 2 s'appuiera sur ES7/ES8 et l'expérience de Dart2JS pour transformer
         le code en JS ou Dart. Il fusionnera les 2 projets AngularJS et AngularDart.

Au lieu de simplement s'appuyer sur ES5 (la dernière version officielle JS), l'équipe
Angular saute plusieurs cases pour s'appuyer directement sur ES7/ES8. Cela fait suite au portage d'Angular sur Dart et de l'apprentissage qui en découle. D'abord dans la possibilité
d'avoir un langage plus «moderne» et moins lourd, d'autres part dans la transformation
automatique de code du projet Dart2JS (permettant de transformer du code Dart en code ES5).

Je trouve que c'est plutôt cohérent : d'un coté ils travaillent sur le futur, avec Dart
comme base d'expérimentation, qui a permit notamment l'émergence des «Web Components» et
l'utilisation de JS comme «assembleur» du Web. Et de l'autre, le présent avec le Javascript. Bien sur, il y'a pas mal de tâtonnements dans les projets mais globalement, les nouveaux projets pérennisent les avancées, ce qui me semble rassurant.

Et pour ceux qui ont misés sur AngularJS 1.x, je pense que le projet sera
(à l'instar de GWT) transféré à la communauté tout en laissant quelques core devs. Il est
déjà annoncé que AngularJS 1.3 aura 2 ans de support **après** la sortie de la 2.0 (soit ~2018).
