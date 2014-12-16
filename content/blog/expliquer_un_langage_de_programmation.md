---
title: Expliquer un langage de programmation
date: "2014-12-16T09:00:00+02:00"
categories: [ "rumination" ]
tags: [ "coding" ]
slug: "expliquer-un-langage-de-programmation"
---

Lors d'une présentation d'un langage de programmation, ou lors d'une discussion entre développeurs, il arrive bien souvent que l'on utilise les termes «avantage» et «inconvénient». Par exemple, cela peut donner comme argument pour Java : «Java c'est cool, tu codes sur la JVM et cela fonctionne sur plusieurs plateformes». Hors pour moi, la JVM est loin d'être un avantage. C'est gros, lourd, géré par Oracle qui impose des restrictions alacon... L'exemple illustre un défaut dans l'argumentation : l'utilisation d'un **argument subjectif présenté comme objectif**. Un avantage pour l'un peut être un défaut pour l'autre, et vice-versa, et la conversation peut donc rapidement tourner à l'affrontement stérile de ce qui est positif ou non.

Pour contrer cela, je voudrais vous présenter une autre approche, qui part de l'objectif (ou au moins tente de l'être) pour aller vers le subjectif, en détachant bien les deux aspects. Explication.

«Opportunité» vs «contrainte»
-----------------------------

Je préfère remplacer avantage vs inconvénient par **opportunité vs contrainte**, ici avec l'exemple de la JVM cité plus haut :

- Une contrainte est une **obligation**, on ne peut y échapper. Coder en Java oblige à utiliser la JVM.
- Une opportunité est une **possibilité** que l'on peut profiter. Utiliser la JVM permet de faire fonctionner son code sur plusieurs plateformes comme Linux ou MacOS.

Ces 2 points tentent d'être objectifs, et peuvent être accepter par ceux qui aiment Java, comme par ses détracteurs. Si vous avez un consensus, alors il est possible de glisser vers la subjectivité car on partage maintenant un **référentiel commun**.

C'est dans l'acceptation des contraintes ou dans la recherche d'opportunités que le choix de chacun va se faire. Voici 2 courts exemples :

- Un amoureux de Scala va apprécier l'opportunité de disposer d'un code plus solide en production et de refactorer plus facilement son code. Pour cela il acceptera que le compilateur soit strict et lui renvoie de temps en temps des messages d'erreur compliqués. Il acceptera aussi une courbe d'apprentissage plus lourde et exigeante, une syntaxe un peu alambiquée et une sémantique chargée.

- Un amateur de Python va aimer la simplicité syntaxique, la sensation de productivité à court terme. Il devra par contre subir la GIL, être plus vigilant sur sa gestion des erreurs.

Vous choisirez alors un langage parce que :

- les opportunités offertes sont intéressantes.
- les contraintes sont bloquantes.

C'est ici que la subjectivité intervient, et qu'il fait prendre à chacun de nous des chemins différents. Si je parle de mes propres choix, je pourrais par exemple dire que j'envie la capacité de gros refactoring que permet Scala, mais la complexité sémantique me rebute suffisamment pour éliminer le langage des mes choix. Et que si j'ai apprécié développer en Python pendant 10 ans, certaines contraintes se font de plus en plus douloureusement ressentir. Nous sommes ici dans la plus parfaite subjectivité. Subjectivité qui dépend de notre expérience, de nos douleurs, de nos envies, de notre travail et de nos objectifs en tant que développeur...

La volonté des concepteurs
--------------------------

Cette dualité «opportunité» vs «contrainte» mets aussi en lumière un point important : les concepteur d'un langage de programmation naviguent en permanence entre un équilibre fragile d'opportunités et de contraintes. Il est de plus très rare de disposer d'une opportunité sans contrainte associée. Faire beaucoup de vérification à la compilation ? Dites alors adieu à une compilation ultra-rapide. Vous voulez un langage avec des concepts avancés de programmation ? Ne vous attendez pas alors à maitriser le langage en 1 an, mais plus en 5 ans, et d'avoir de sérieux mal à la tête sur certains messages d'erreurs. Tout est question d'équilibre. A ma gauche des opportunités, á ma droite des contraintes.

C'est maintenant comme cela que je présente un langage, en faisant au préalable, en introduction, l’équivalent du texte que vous venez de lire. Non pas comme une liste d’avantages (que les auditeurs prendront ou nous comme tel), mais comme un ensemble de contraintes et d'opportunités, et laissant chacun d'entre eux faire leur opinion. Le plus important, je pense, est de montrer en quoi cet équilibre est intéressant.
