---
categories: formation
date: 2012/12/17 12:44:00
title: Catalogue formation 2013
---

En septembre 2010, j'ai lancé #gitfr pour expliquer les DVCS et Git en
particulier. 2 ans, ~30 présentations et ~10 ateliers plus tard j'ai besoin de
parler d'autres choses :). Je propose de nouveaux ateliers et présentations sur
des sujets assez variés, que ce soit en développement, administration ou
management. Si vous êtes interéssé par un sujet, il suffit de me contacter pour
se mettre d'accord sur un lieu et une date.

**Attention** : Je n'ai aucune certification, je ne suis pas estampillé
«Expert machin» ou «Champion truc». Je n'ai même jamais eu de formation sur un
quelconque sujet (j'ai appris la plupart du temps seul dans mon coin dans le
cadre professionnel).  Ce ne sont que des **modestes retours d'expérience** sur
des sujets qui m'intéressent et que je souhaite partager.

Comme pour #gitfr, le deal est le suivant :

- C'est **gratuit** (je demande juste le remboursement des frais de transport
  et d'hébergement) dans le cadre d'une action associative.
- La gestion de l'événement est à votre charge (trouver un lieu, accueillir les
  gens, etc).
- Etant un utilisateur de Logiciels Libres depuis plus de 15 ans, je me
  focalise que sur les plateformes **Linux / BSD**. Les OS «professionnels» ne
  m'intéresse pas, ni de prêt ni de loin.

Certains ateliers sont plutôt bien avancés, d'autres n'existent que dans ma tête.
Ne vous étonnez donc pas si je vous réponds qu'il me faut plusieurs mois pour
en préparer certains :). J'ai mis une petite présentation sans prétention pour
chaque sujet (la plupart sont à l'état de brouillon) pour vous donner un aperçu
du contenu et de l'objectif recherché. Les durées sont des estimations à la
louche, ne vous focalisez pas trop dessus.

**Note 1** : Cette page devrait évoluer, n'hésitez donc pas à venir de temps en
temps.

**Note 2** : Chaque atelier peut évidemment être transformé en présentation
si c'est ce format que vous recherchez. De même, si le sujet vous intéresse
mais qu'il manque un contenu particulier, n'hésitez pas à en faire la
demande.

**Note 3** : j'ai mis à la fin des idées de sujet. Si vous avez d'autres, 
postez un commentaire. Si j'ai les compétences nécessaires, je tenterai
d'en faire quelque chose.

Introduction à la virtualisation
--------------------------------

**Domaine** : infra / **Type** : atelier  / **Durée**: : 5h

La virtualisation offre de nombreux avantages, autant pour le développeur qui
peut tester facilement et sans danger son code que pour l'administrateur qui
peut gérer une infrastructure avec beaucoup moins de machines.

Objectif :

- Comprendre les différentes techno de virtualisation
- Apprendre à créer des machines virtualisées
- Déployer une infrastructure virtualisée
- Distribuer des VMs

Contenu :

- QEMU / KVM
- LXC
- VirtualBox
- OpenVZ ?
- Xen ?
- Apprentissage des formats d'image (RAW, VDI, QCOW2, VMDK)
- Apprentissage du format de description OVF
- Libvirt
- Virt-tools
- Guestfs et sa suite d'outils


**Note** : L'atelier se focalise principalement sur la techo KVM qui devient la
référence dans le monde du Libre. Je rajoute LXC qui est simple et pratique. Je
ne suis pas sûr pour OpenVZ et Xen.

Monter son cloud avec OpenStack
-------------------------------

**Domaine** : infra / **Type** : atelier  / **Durée**: : 5h

Si Amazon AWS est la référence du cloud, il peut être plus intéressant de
disposer d'une technologie que l'on maitrise de bout en bout, que ce soit pour
monter un cloud privé ou public. Le projet OpenStack, monté par Rackspace et
dirigé maintenant par une organisation mondiale composée de dizaines de
société, est devenu la technologie cloud Libre la plus en vue.

Objectif :

- Comprendre l'architecture OpenStack
- Installation et configuration
- Déployer une VM

Gérer son cloud Amazon AWS en Python
------------------------------------

**Domaine** : infra / **Type** : atelier  / **Durée**: : 3h

Aprés une rapide introduction au Cloud IAAS, nous verrons comment en partant de
zéro, mettre en place des machines virtuelles sur Amazon AWS et les exploiter
avec Boto et SaltCloud.

Objectif :

- Déployer ses propres images sur le cloud Amazon

Contenu :

- Présentation rapide d'Amazon AWS
- Créer une image Amazon
- Déployer avec Boto
- Déployer avec SaltCloud

La virtualisation du réseau
---------------------------

**Domaine** : infra / **Type** : atelier  / **Durée**: : 3h

Après le IAAS, le PAAS et la SASS, voici le NAAS (Network As A Service). Si
la virtualisation de vos machines est un pas en avant, il manque un élément :
la capacité de gérer aisèment votre réseau qui alimente vos machines
virtualisées. Venez découvrir dans cet atelier OpenVSwitch, la référence
Libre dans le domaine.

Objectif :

- Comprendre l'architecture OpenVSwtich
- Déployer un switch virtuel

Contenu : 

- Introduction à la virtualisation réseau
- OpenFlow et contrôle automatisé
- Installation
- Configuration de base
- Monitoring : Netflow, sFlow, SPAN, RSPAN
- QoS
- Modification à la volée de paquets
- gestion de VLAN
- Contrôle de votre réseau avec POX / MOX

Sécuriser votre réseau avec PF
------------------------------

**Domaine** : infra / **Type** : atelier  / **Durée**: : 3h

Trop souvent, les sociétés ne mettent pas de firewall ou utilisent ceux
intégrés à des produits comme les routeurs Internet. Et quand ils en mettent
un, ce sont des technos propriétaires lourdes. Pourtant, OpenBSD à créer
le pare-feu PF, très simple de mise en place (surtout comparé à son équivalent
Linux Iptables) et agréable d'utilisation. Avec PF, la sécurisation est un jeu
d'enfant.

Objectif :

- Comprendre PF
- Déployer un pare-feu

Contenu :

- Introduction à la sécurité des réseaux
- Les différents modèles de PF
- Installation d'OpenBSD
- Configuration PF simple pour un petit réseau
- Configuration PF simple pour un réseau élaboré
- Configuration PF avancée pour un réseau élaboré
- Mise en place du QOS
- Supervision de son pare-feu

**Note** : L'utilisation d'un live-CD est envisagée pour sauter l'étape
installation.

Développer des scripts en Python
--------------------------------

**Domaine** : développement / **Type** : atelier  / **Durée**: : 5h

Vous écrivez encore vos scripts en Shell à base de cut, grep, awk ? Vous
souffrez pour les maintenir quand ils dépassent 100 lignes ? Venez découvrir
le langage Python qui vous offre l'accès à de nombreuses librairies pour
coder des scripts systèmes allié à une maintenance bien plus aisée.

Objectif :

- Apprendre les bases de Python
- Ecrire de petits programmes (système, graphique, réseau)

Contenu : 

- Installation de Python
- Premiers pas (variable, affectation, opérateur, expression)
- Contrôle du flux d'exécution
- Principaux types de données
- Les fonctions
- Approfondir les structures de données
- La programmation objet en Python
- Maitriser les outils de base : pip, virtualenv
- Introduction à l'outil Buildout
- La sémentique Python
- Apprentissage de  quelques modules importants
- Etude de quelques librairies intéressantes
- Débugger du code Python
- Comprendre le packaging Python

Maitriser le packaging Python
-----------------------------

**Domaine** : développement / **Type** : atelier  / **Durée**: : 3h

Distutils, Setuptools, format source, binaire ou Egg, easy-install, pip,
distribute, PyPI... Êtes vous perdu ? Si ces mots vous sont inconnus ou vous
donnent mal au crane, cette session est donc pour vous. Des premiers pas
jusqu'à la diffusion de vos programmes, cette session vous aide dans vos
premiers pas dans le monde Python.

Objectif :

- Comprendre le packaging Python
- Maitriser son environnement de travail
- Savoir distribuer ses programmes Python

Contenu :

- Décortiquer le packaging Python (distutils, distribute)
- Outil PIP
- Outil Buildout

Gérer sa documentation avec Sphinx
----------------------------------

**Domaine** : infra / **Type** : atelier  / **Durée**: : 1.5h

LibreOffice ou Word pour écrire et maintenir de la documentation, c'est la
plaie ! Développé originalement pour la documentation officielle Python, Sphinx
vous permet de créer une documentation HTML, PDF ou EPUB simplement et surtout
maintenable puisque tout est sous forme de fichier texte. Il devient alors
possible de gérer sa documentation comme on le fait pour son code : utilisation
du DVCS, revue des pairs, etc.

Objectif :

- Créer une documentation HTML et PDF

Infra : Gérer son parc machine avec Salt
----------------------------------------

**Domaine** : infra / **Type** : atelier  / **Durée**: : 2h

Si vous entendez souvent parler de Puppet et Chef, ce n'est pas le cas d'un
nouveau venu qui se nomme Salt. Intégrant un shell distribué, rapide, facile
d'utilisation et aisèment extensible en Python, Salt facilite gradement la
gestion de votre parc de machines.

Objectif :

- Comprendre l'architecture Salt
- Contrôler une machine virtualisée

Contenu :

- Installation
- Configuration basique
- Utiliser quelques modules Salt
- Apprendre à coder un module Salt
- Salt pour le cloud

Présentation du langage Go
--------------------------

**Domaine** : développement / **Type** : présentation  / **Durée**: : 1.5h

La version 1.0 de Go est sortie début 2012. Pourquoi apprendre Go et non Nodejs
ou Erlang ? Qu'apporte t'il par rapport à Python, Ruby ou PHP ? L'objectif de
cette session est de faire le tour de ce langage et de montrer concrétement son
positionnement ainsi ses avantages et incovénients.

Objectif :

- Positionner Go par rapport aux autres langages
- Comprendre le modèle objet de Go
- Voir l'apport de Go dans la programmation concurrente

Atelier Go
----------

**Domaine** : développement / **Type** : atelier / **Durée**: : 5h

Vous êtes curieux de voir ce que donne ce langage mais vous n'avez jamais
osé coder ? Voici un atelier pour s'initier.

Objectif :

- Coder quelques scripts système
- Coder un service réseau concurrent

Contenu : 

- Installation de Go
- Structuration d'un projet
- Types de base (boolean, int, string)
- Types collection (array, slice, map)
- Programmation procédurale (if, switch, for)
- Les fonctions
- Gestion des erreurs
- Programmation orienté objet en Go (custom type, interface, struct)
- Visite de la librairie standard
- Channel et goroutine
- Programmation parallèle
- Test unitaire
- Debuggage d'un code Go
- Installation d'un package
- Création d'un package
- Déploiement d'un projet Go

Présentation du langage Dart
----------------------------

**Domaine** : développement / **Type** : présentation  / **Durée**: : 1.5h

Développé d'abord comme un projet de R&D par une partie de l'équipe v8, Dart
est annoncé le 10 octobre 2011 par Google comme un nouveau langage pour le
web.


La version 1.0 de Go est sortie début 2012. Pourquoi apprendre Go et non Nodejs
ou Erlang ? Qu'apporte t'il par rapport à Python, Ruby ou PHP ? L'objectif de
cette session est de faire le tour de ce langage et de montrer concrétement son
positionnement ainsi ses avantages et incovénients.

Objectif :

- Positionner Dart par rapport à Javascript
- Montrer comment Dart modifie la façon de développer un site web

**Note** : Pas avant la sortie de Dart 1.0.

Atelier Dart
------------

**Domaine** : développement / **Type** : atelier / **Durée**: : 5h

Vous êtes curieux de voir ce que donne ce langage mais vous n'avez jamais
osé coder ? Voici un atelier pour s'initier.

Objectif :

- Coder une page dynamique (one page website)

Contenu : 

- Installation de Dart
- 1er programme en ligne de commande
- Vérification avec dart-analyser
- Découverte de l'éditeur Dart
- Dart natif et Dart2js
- Architecture d'application web une page
- Types de base (number, string, boolean, list, map)
- Programmation procédurale (if, while, do while, switch, for)
- Accéder au DOM (dart:html)
- Fonction et closure
- Gestion des erreurs
- Programmation orienté objet en Dart (classe, interface)
- Generics
- Librairie et visibilité
- Programmation concurrente (isolate)
- Organiser son code Dart
- Gestion de package avec pub
- Programmation asynchrone
- Développement d'une application Dart coté client
- Développement d'une application Dart coté serveur
- "Web component"
- Test unitaire et Mock
- Debuggage d'un code Dart
- Installation d'un package
- Création d'un package
- Déploiement d'un projet Dart

**Note** : Pas avant la sortie de Dart 1.0.

Retour d'expérience sur le deploiement continue
-----------------------------------------------

**Domaine** : management / **Type** : présentation  / **Durée**: : 1.5h

L'intégration continue est considérée depuis plusieurs années comme une bonne
pratique de gestion de projet, et sa généralisation dans les équipes de
développement est une avancée notable. Mais pour s'assurer que son produit
fonctione, rien ne vaut un déploiement dans un environnement réaliste. D'ou
l'émergence d'une nouvelle pratique : le déploiement continue. Cette session
est un retour d'expérience de 3 ans de cette pratique chez un éditeur logiciel.
Nous parlerons d'outil d'intégration continue et de virtualisation ainsi que
d'outil de gestion de source. Nous aborderons aussi la philosophie Devops dont
cette pratique est en droite ligne.

Retour d'expérience sur la revue de code
----------------------------------------

**Domaine** : management / **Type** : présentation  / **Durée**: : 1.5h

Depuis 3 ans, nous pratiquons la revue de code systématique, chaque ligne de
code (ainsi que l'infra ou le packaging) étant revue avant de passer en
production. Coûteuse en temps, elle permet néanmoins d'augmenter la qualité en
trouvant erreurs et bugs potentiels. Mais surtout, elle permet d'aligner
l'équipe autour de pratiques communes, en normalisant le code et en échangeant
ses connaissances. Cette session est un retour d'expérience de ces années de
pratique : comment mettre en place la revue de code ? Quelles sont les
différentes façons de faire de la revue ? Quel mentalité doit on avoir ?
quelles sont les avantages et inconvénients ? Les bonnes pratiques et les
erreurs à éviter ? Nous passerons également en revue deux Logiciels Libres pour
mettre en place la revue de code : ReviewBoard et Gerrit.

Simplifier vous la vie avec Buildout (Python)
---------------------------------------------

**Domaine** : dev / **Type** : atelier  / **Durée**: : 3h

Une difficulté quand on travaille en équipe est d'avoir un environnement
parfaitement identique et répétable, surtout qu'on possède beaucoup de
composants Python. Il faut bricoler un environnement virtuel, installer les
bonnes versions de chaque composant et modifier le sys.path à la main pour
utiliser ses composants en cours de développement. Et les choses se complique
quand il est nécessaire de disposer des logiciels non Python. Certains
développeurs utilisent l'outil Virtualenv associé à l'outil PIP. Mais il existe
pourtant un outil bien plus puissant et adapté : Buildout. Sous une doc austère
se cache un outil puissant et efficace, et relativement simple d'utilisation
qui permet de reproduire rapidement et efficacement un environnement donné,
grace notamment à un système de plug-ins (appelé recettes). L'objectif de cette
session est de vous rendre autonome sur l'outil et d'apporter en plus un retour
d'expérience de 4 ans d'utilisation chez un éditeur logiciel où il est utilisé
en sus comme outil de déploiement. Nous aborderons aussi Distutils, Setuptool
et Virtualenv.

Objectif :

- Comprendre l'intéret de ce type d'outil
- Passer son projet Python sous Buildout
- Développer avec Buildout
- Déployer avec Buildout

Contenu :

- Fonctionnement de Buildout
- Ajouter des recettes
- Déployer avec Buildout
- Développement de recette

Les outils Devops en Python
---------------------------

**Domaine** : dév / **Type** : présentation  / **Durée**: : 2h

Depuis l'éclosion du mouvement Devops, des outils comme Chef ou Puppet sont
omniprésents et tiennent le haut du pavé. Mais du shell distribué aux outils de
déploiement en passant par le Cloud, il existe des outils de très bonnes
qualités en Python. Cette session est un tour d'horizon des outils disponibles
: Fabric, Ansible, Buildout, Salt...

Objectif :

- Connaitre les principaux outils en Python

Contenu :
- Présentation de Fabric
- Présentation de Ansible
- Présentation de Buildout
- Présentation de Salt

Présentation de Git
-------------------

**Domaine** : dev / **Type** : présentation  / **Durée**: : 3h

Utilisateur de SVN pendant de nombreuses années, j'avais la sensation
croissante de me battre avec mon outil de travail. Pire, il s'adaptait très mal
à mes exigences collaboratives. De guerre las, nous en avons choisi un outil de
gestion de source décentralisé (Hg puis Git) début 2008. La différence était
flagrante, je me sentais comme libéré d'un poids qui me ralentissait, et la
production de l'équipe s'est fortement améliorée (quantitativement et
qualitativement). 

Cette présentation vous donnera la compréhension nécessaire pour aborder
sereinement l'utilisation de Git (et aux DVCS en général) : La première partie
sera consacrée à la théorie, en passant en revue tous les concepts nécessaires
avec l'aide de nombreux schémas didactiques. Nous mettrons en pratique nos
nouvelles connaissances dans la seconde partie, en abordant les commandes qui
font la «différence», les workflows, l'utilisation de GitHub, le tout saupoudré
de conseils pour bien démarrer.

Débuter avec Git
----------------

**Domaine** : dev  / **Type** : atelier  / **Durée**: : 5h

Vous voulez apprendre les bases de Git ? C'est session est pour vous. Mixant
théorie et pratique, cette sesion de 3 heures vous donnera les clés pour
comprendre cet outil fanstatique mais un peu rugueux à prendre en main.
Seront passés en revue les 3 concepts fondamendaux ainsi que les différentes
manipulations qu'offre Git. Nous terminerons par les commandes de base.

Gérer le développment logiciel avec le Kanban
---------------------------------------------

**Domaine** : management / **Type** : présentation / **Durée**: : 2h

Agiliste forcené depuis de nombreuses années mais non satisfait par
les outils de suivi de projet que j'employé jusqu'alors, j'ai décidé
de passer voici 5 ans, au développement par flux, représenté par l'outil
Kanban. 

Objectif : 

- Comprendre le développement par flux
- Comprendre l'importance du *lead time*
- Etudier le fonctionnement d'un Kanban

Petit précis de management à l'égard des informaticiens
-------------------------------------------------------
**Domaine** : management / **Type** : présentation  / **Durée**: : 3h

«Pourquoi devrais-je m'y connaitre en management ? je ne suis pas manager !».
Tel est la remarque que vous pouvez vous faire en lisant le titre.
Et pourtant, le management et l'organisation sont les 2 plus importantes
facettes du travail : remplacer «management» par **gestion des hommes** et
«organisation» par **gestion des relations entre les hommes** et vous comprendrez
qui est suicidaire de laisser cela à des prétendus managers, qui sans
aucune connaissance de leur métier prennent des décisions qui vous impactent
quotidiennement. Disposer d'une culture, même faible, permet de mieux comprendre
votre environnement et d'agir en conséquence.

Objectif :

- S'intéresser aux fonctionnement de son entreprise
- Avoir une culture managérial et organisationnel

Je veux devenir un manager
--------------------------

**Domaine** : management / **Type** : présentation  / **Durée**: : 5h

A travers mes 7 ans d'expérience en tant que manager (et 8 en ayant subi des
managers), moi qui était au départ le stéréotype de geek seulement intéressé
par ma relation avec les ordinateurs, je vous propose un voyage initiatique
dans le monde fascinant du management.


Objectif :
- 

Contenu :
- Le management, du 17eme siècle à nos jours
- Le mouvement Lean
- Le mouvement Agile
- System Thinking
- Monter une équipe
- La vision par flux
- Le Kanban

Idées
-----

- Monter son premier IPBX avec Asterisk (atelier / 3h)
- Présentation du langage Dart (présentation / 2h)
- Introduction au lanagage Dart (atelier / 3h)
- Debugguer du code Python (présentation / 1h)
- Les libraires du développeur Python (présentation / 2h)
- Apport du mouvement Lean dans le développement logiciel (présentation / 3h)
- Apport du mouvement Agile dans le développement logiciel (présentation / 3h)
- Monter une équipe de développement logiciel (présentation / 2h)
- Développer une application réseau en Python avec 0MQ (atelier / 2h)
