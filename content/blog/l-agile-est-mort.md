---
title:       "L'Agile est mort"
date:        "2011-08-08T03:00:00+02:00"
categories:  [ "rumination" ]
tags:        [ "agile", "rumination" ]
aliases:     [ "/blog/2011/08/08/l-agile-est-mort/" ]
slug:        "l-agile-est-mort"
---

Sous ce titre qui peut paraitre provocateur se trouve un constat plutôt amère,
d'autant plus amère que tout cela était prévisible depuis bien des années.
L'Agile est devenu *mainstream*, on en parle régulièrement dans les
journaux de décideurs (c'est bien la preuve de sa reconnaissance non ?), les
développeurs disent le pratiquer au quotidien, les responsables de projet
assurent en faire. Alors pourquoi ce pessimisme ? Parce qu'il ne se passe un
mois sans en avoir la preuve, par exemple quand quelqu'un se pose en face de
moi et me dit :

> L'agilité, c'est vraiment de la merde !

Et cela m'arrive très souvent (certes ce n'est pas toujours aussi vulgaire).
Il ne faut pas 2 minutes pour savoir que son contexte n'est pas Agile, ni de
près, ni de loin. Mais le signe le plus tangible est d'entendre des
soit-disant *spécialistes* dirent n'importe quoi à longueur de blogs,
journaux ou listes de diffusion.

Oh, je vous vois venir : «mais qui es tu pour définir ce qui est de ce qui
n'est pas Agile ?». Excellente question ! En fait, si définir avec précision
les contours de l'agilité est difficile, surtout en 2011 où beaucoup de
pratiques ou de mouvements se disent Agile, il est bien plus facile de dire ce
qui n'est **pas Agile** quand c'est **aux antipodes de la philosophie qu'il veut
incarner**. Certes le référenciel des pratiques a augmenté, mais il y'a toujours des
fondamentaux clairs et bien visibles, et toutes pratiques agiles doivent en
découler. J'aime comparer l'agilité avec le Logiciel Libre,
deux mouvements auxquels je participe depuis longtemps (10 et 15 ans), car ils
sont dans les deux cas un mélange de technique et d'humain. Dans les deux cas,
c'est une certaine **représentation du monde** et des relations entre les
gens :

Si je diffuse un logiciel avec une licence Libre, par exemple BSD, mais que
je ne propose pas de bugtracker, de liste de diffusion, ou que je refuse toute
contribution extérieure, ou que j'obfusque mon code, ou que j'envoie sur
les roses les demandes d'utilisateurs, je fais du Logiciel Libre (ma licence
le prouve) sur papier. Dans les faits, ce n'est qu'un ersatz, je ne respecte
pas la philosophie du Logiciel Libre. Il en est de même avec l'agilité.

A mes yeux, l'agilité se résume en trois points dont leurs présences sont
faciles à juger.

La recherche de la valeur
------------------------

Souvent maladroitement appelé *un logiciel qui marche*, l'objectif est de
donner aux utilisateurs un produit fonctionnel, utilisable et pratique.
Et sauf à produire un logiciel maintes et maintes fois demandée, c'est
une découverte, autant pour le client que pour l'équipe de développement.
C'est donc une utopie de croire que l'on peut définir à l'avance les
spécifications complètes du logiciel. Le but est avant de trouver ce
logiciel agréable et fonctionnel, et non de le faire vite. La cascade
est à bien des égards l'approche la plus efficiente pour faire du logiciel
rapidement :

* J'écoute les besoins.
* Je conçois et valide les spécifications.
* Je développe.
* Je teste.
* Je livre.

Il n'y a pas plus rapide. Si vous faites depuis 20 ans la même chose, pas de
soucis. Je n'ai entendu que deux (oui deux, pas trois) sociétés
capables de livrer en temps et en heure avec de 99% succès en mode cascade.
Et sans surprise ce sont deux sociétés développant en Cobol sur une
plateforme assez ancienne des produits fortement similaires. En résumé :

* Equipe stable.
* Techno et plateforme archi connues.
* Métier fortement maitrisé.
* Produits similaires.

En sommes, un environnement idéal. Mais il est illusoire d'attendre d'un
client la capacité à définir avec précision ses besoins. Non seulement il
ne sait pas ce qu'il veut, mais il se rend souvent compte après coup que
ce qu'il a réussi à expliquer est sans intérêt ! Voire même que son business
ou ses besoins ont changés entre le début du développement et sa fin. Et je
ne parle même pas de la capacité d'une équipe de développement à livrer un
produit de bonne qualité d'une seule traite, surtout si c'est en découvrant
le métier du client. Bref, pour résumer, c'est utopique. Mettons cela sur
l'immaturité de notre métier, la jeunesse de nos outils et une formation
trop basique.

Au contraire, l'agilité se veut une quête de sens :

* Que dois je obtenir ?
* Quelles sont les fonctionnalités réellement utiles ?
* Ce besoin est il justifié ? N'est elle pas le symptôme d'un problème
  non technique ?
* Voir même, ce logiciel est il utile ?

C'est un effort collectif, allant du développeur jusqu'au client pour
comprendre, analyser et développer de la valeur métier  à travers un
logiciel. Sans cela, vous faites de la cascade : on se met d'accord sur
une limite fonctionnelle, numéraire et temporelle et zou !

Passons au deuxième point.

L'humain est au centre
----------------------

Ce qui ressort aussi est cette volonté permanente de mettre en
avant les personnes, et non les outils ou les processus. les seconds sont
aux services des premiers, et pas l'inverse ! Le développement est une
histoire de développeurs avant tout. Vous devez **faire confiance aux gens,
les respecter dans leur capacité à produire, dans leur jugement**. Cet accent
me semble t'il est absent des approches précédentes comme la cascade ou RUP.
Ces dernières sont plutôt axées processus, avec des dizaines de procédures
et de la documentation à profusion, le développeur n'étant qu'un rouage du
système.

CMMi est un bon exemple de cette vision : la documentation officielle parle
sempiternellement d'organisation et de processus. Et pire, il faut être
certifié CMMi pour savoir lire une doc CMMi (cherchez l'erreur) tellement elle
est inbitable et truffée d'une terminologie incompréhensible. D'ailleurs la
plupart font du cascade, c'est dire leur croyance dans les processus. Il
faudra attendre 2010 pour entendre le CEI parler sérieusement d'agilité, 11
ans après le livre de Ken Beck !

Au contraire, l'agilité privilégie l'interaction sur le processus, le
résultat sur la documentation, en rapprochant physiquement tous les
participants, en  poussant les réunions courtes mais régulières, et en
écoutant les gens.

Passons maintenant au troisième point.

Le développement est une discipline
-----------------------------------

Le développeur remis en selle comme moteur du développement, on lui demande
en échange de maitriser son métier : on veut du logiciel qui fonctionne ! Il
doit remettre sans cesse se remettre en cause, apprendre à faire mieux et à
affiner ses techniques de développement.

Le milieu logiciel aime bien se traiter d'artisan (chaque profession aime se
dépeindre avec élégance) mais cela est identique chez les livreurs, les
boulangers, les cuisiniers, les musiciens... Mis à part que le développement
logiciel est un métier non seulement très complexe mais en plus à ces
balbutiements : 60 ans. Cela est bien peu.

L'agilité apporte beaucoup de solutions intéressantes : le TDD, les tests,
la revue par les pairs, l'intégration continue ou le refactoring par exemple.
Bien sûr un développeur peut très bien travailler correctement depuis très
longtemps sans avoir jamais lu un seul livre sur l'agilité. Après tout Ken
Beck et ses accolytes ont découvert ces techniques, pourquoi pas les autres ?
Certes, mais se passer de l'agilité, c'est mettre de coté des années de
réflexion sur les pratiques de développement logiciel et ca serait bien
dommage.

Alors, pourquoi dire que l'Agile est mort ?
-------------------------------------------

je ne suis malheureusement pas assez vieux pour savoir ce qui se passait dans
les années 70, 80 et 90 dans l'industrie du logiciel mais je ne crois pas me
tromper en disant que l'agilité est une étape marquante. Je suis malgré
tout un vieux Geek, j'achetais pas mal de livres sur la programmation voici 20
ans et je n'ai aucun souvenir des livres (en France en tout cas !) qui
ressemblaient peu ou prou à l'agilité, on apprenait plutôt en copiant le code
des *maitres* (en crackant des logiciels, en écoutant les démo-makers ou en
bavardant sur les BBS). Des pratiques quasi inconnues voici 10 ans sont
maintenant considérées comme des pratiques indispensables (vous faisiez
beaucoup de tests unitaires en 2000 ?).

L'agilité a **apporté la lumière à des milliers de développeurs**, dont moi,
et à fait progresser notre connaissance de notre métier, en construisant
pour la première fois un socle stable. Nous en sommes encore au début mais
nous tentons chaque jour de mieux comprendre ce métier Ô combien difficile.

Mais vous savez quoi ? **Tout le monde s'en fout !**

L'Agile est la nouvelle technique à la mode
-------------------------------------------

On s'aperçoit rapidement qu'une majorité d'organisations utilise l'Agile
parce qu'ils ont entendus que ça marche mais se foutent royalement de ce
qu'il y a dedans. Et pour cause, cela signifie aussi remettre à cause
deux visions fondamentales dans nos entreprises :

* L'informatique est un coût, pas un investissement.

* Les employés sont interchangeables, et non le socle de l'entreprise.

Ne voulant pas remettre en cause ces deux postulats, il ne peut en
résulter qu'un dévoiement du mouvement Agile. Et c'est ce qui se passe.
**L'Agile est donc une mode**, qui passe après le développement objet,
les Design Patterns, le C++, Java, les frameworks, RUP et quelques
autres. On verra dans quelques années fleurir de nouvelles modes quand les
promesses des vendeurs Agiles se seront écrasé sur le mur de la réalité
des entreprises.

Mais que font ils ?
-------------------

Du développement **itératif et incrémental**. Ils découpent leurs
développements en lots plus petits, avec vérification régulière. Le rapport
avec l'Agile tel que je le décris au début du billet ? Aucun ! Faire
confiance aux gens ? Soyons sérieux, ils pratiquent régulièrement
le *command & control*, technique qui consiste à faire travailler les
gens comme des marionnettes, et les accuser de faire du mauvais
boulot en cas de pépin. Voir le développement comme une discipline ? Vous
parlez de ces directions des achats qui écrasent le prix journalier des
développeurs vers le bas ? Quand à la recherche de la valeur, cela
signifie remettre douloureusement en cause le fonctionnement de l'organisation.

Vous commencez à me comprendre ? Ce n'est d'ailleurs pas pour rien que l'on
vend du Scrum, qui consiste à faire des lots (appelé itération) avec démo
régulière qu'on soupoudre avec une réunion quotidienne et une rétrospective
de temps en temps. Le tour est joué, on fait de l'Agile !

Dites moi si ces quelques exemples vous dit quelques choses :

* Le Chef de projet est appellé ScrumMaster, parce qu'il a fait 2 jours de
  formation.

* On n'évalue pas la pertinence business d'une fonctionnalité.

* On a pris des développeurs sous qualifiés ou inexpérimentés car par chers.

* Le pair-programming ou la revue de code ? Trop cher et inutile.

* Le ScrumMaster assigne les tâches à chaque réunion quotidienne.

* La rétrospective se fait avec le client.

* Un cahier des charges est construit avant de développer.

* On ne prend jamais le temps de revoir les parties qui posent problèmes.

* On doit travailler tard pour rattraper le retard ou gérer les nouvelles
  demandes du marketing.

* Le projet va dans le mur mais on ne fait rien.

* On micro-manage les gens.

* On découpe le projet en équipe qui ne se voit pas.

* On ne fait pas monter en compétence les membres de l'équipe.

Je pourrais ajouter bien d'autres exemples, mais vous voyez l'idée. Où est la
philosophie Agile ? Absente, car les organisations ne souhaitent pas changer
leur vision du développement logiciel, encore moins leur mode de fonctionnement.

Pourquoi en faire ?
-------------------

Parce que ça se vend, pardi ! Des sociétés de conseils se sont placés sur
le marché, des associations se sont créés pour développer ce business. Alors
ca se vend, et plutôt bien maintenant.


Mais comment faire de l'Agile :

* dans un environnement *command & control* ?

* dans une culture du blâme et de la recherche du coupable, ou chaque
  responsable sort son parapluie au moindre soucis ?

* quand on vous donne un cahier des charges sans remise en cause du besoin
  business ?

En le triturant pour que cela rentre dans les cases. Un exemple ? La grande
**tartuferie** du développement Agile au forfait. Regardons de plus près : le
forfait consiste à définir une limite fonctionnelle, temporelle et numéraire
d'un développement. Cela vous rappelle quelque chose ? Pas pour rien que le
forfait agile est un serpent de mer dans toutes les conférences Agile depuis
des années, tous les responsables de SSII se demandant comment en faire.

L'Agile est mort en 2001
------------------------

Plus précisemment en **février 2001**, à Snowbird Utah USA. C'est la
création du *Manifeste Agile* et de l'emploi du terme Agile. Plus généralement,
c'est une volonté de mettre en place un **modèle**, un cadre. C'est à partir
de 2002 que l'on voit fleurir les livres avec le terme agile dans le titre.

Cela peut paraitre surprenant de dire cela, puisque c'est aussi le début du
mouvement Agile. L'objectif de normaliser termes et principes, de les figer,
est avant tout pour mieux le vendre. Il est curieux de voir **17 consultants
sur les 17 signataires du manifeste** : tous vendent des livres, tous vendent
des formations. L'Agile Alliance fut créée dans la foulée pour en faire la
promotion.

Un modèle sclérosé
------------------

Résultat en 2011 ? Malgré quelques avancées, le discours Agile officiel est
proche de 2001. N'a t on rien appris en 10 ans ? Bien sûr que si : le
développement par flux, la prise en compte de l'organisation dans le
développement ne sont que deux  exemples fondamentaux. Mais pourtant, le modèle
Agile reste assez hémertique à ces changements. On a bien vu quelques
nouveautés mais rien de bien méchant. Pourquoi ? Parce qu'on est plus
intéressé à vendre qu'à réfléchir, car pour réfléchir **il faut avant tout
faire** ! Ce n'est pas en écrivant des livres et en faisant du consulting
qu'on peut produire. XP est le résultat de très nombreuses années de
pratique de développement logiciel. Taiichi Ono (fondateur du *Toyota
Production System*) à passé plusieurs décennies pour perfectionner son
organisation. Il ne faisait surement pas passer des certifications TPS 5 ans
après avoir débuté sa nouvelle organisation !

Il y a bien eu un déplacement léger du développeur vers l'organisation. Même
si le modèle Agile s'ouvre sur l'extérieur, cela reste limité : il suffit
de voir le rôle du *PO* (Product Owner), proxy du reste de la société, où
se trouvent des *stakeholders*. Ou est le marketing commercial ? Technique ?
La recherche de nouveaux marchés ? Le déploiement ? L'opérationnel ?
L'expérience utilisateur ? Le design ? En gros, où est tout le reste ?!
Le vide, les têtes pensantes du modèle Agile sont encore à rabacher TDD et
planning poker, la belle affaire !

Pire, ce léger déplacement est contre balancé par le **mouvement craftmanship**,
qui se veut un retour au source, auto-centré sur le développeur. La seule
avancée intéressante vient de partir à l'eau ! Si vous voulez savoir pourquoi,
regardez juste le business du fondateur de mouvement, Bob Martin, vendeur
de livres et de formations... sur le code. Forcément, l'organisation, ce n'est
pas utile pour son business. Il est d'ailleurs marrant d'entendre certains se
pâmer devant ce mouvement comme ci c'était nouveau. XP disait peu ou prou la
même chose  voici 13 ans. Ce n'est d'ailleurs pas anodin que ce soit
majoritairement des Scrumistes qui ont font (en France) la promotion, alors
qu'ils critiquaient XP ouvertement.

Conclusion
----------

J'espère avoir éclairci mon propos sur Twitter (140 caractères, c'est des
fois trop court :). Non, il ne faut pas arrêter de faire des tests,
du pair programming ou des réunions quotidiennes. Et non, il ne faut surtout
pas minimiser l'impact de l'agilité sur notre métier, bien au contraire ! Je
vous encourage à lire livres et blogs et à prendre ce dont vous avez besoin.

Il faut seulement avoir une vision systémique du mouvement, comprendre d'où
il vient, pourquoi il a été créé et pourquoi certaines personnes vendent le
modèle Agile. Cela permet par exemple de comprendre le *Manifeste Agile*
au lieu de répéter bêtement son contenu qui est loin d'être optimal en 2011.
Cela permet aussi de comprendre que ce modèle créé en 2001 (Scrum en 96, XP
en 99) et qui a mis du temps à se propager n'apporte plus rien de neuf
depuis de nombreuses années. Si l'argent fut toujours le moteur, le modèle
est maintenant dévoyé **pour rentrer dans la matrice consulting**, loin des
objectifs initiaux. Et ni les voix *officielles* (Agile Alliance, Scrum
Alliance), ni ses *têtes pensantes* se sont élevés contre cela. Pire, elles
ont participé activement à ce dévoiement (qui a dit certification ?).

Je pourrais résumer ma pensée ainsi : **L'agilité est une avancée importante,
mais le modèle Agile est inutile**. C'est peut être le destin de tout
modèle. En tout cas il est temps que chaque organisation invente, à l'instar de
Toyota, son propre modèle de production. Un modèle **adapté à son business,
ses clients, ses collaborateurs**. Un modèle qui **prend en compte toutes les
nouvelles avancées** que l'on peut trouver dans les mouvements tels que Devops,
Lean, Lean startup ou Kanban. Un modèle **qui évolue** sans cesse avec la
maturité et la capacité de l'organisation à produire.

Mais pour essayer de le faire sans relâche depuis 4 ans, je vous concède que
c'est bien plus difficile et pénible qu'une formation de 2 jours ou de
répéter à l'envie ce que l'on a lu dans un livre...
