---
title:       "Nomenclature des tests logiciels"
date:        "2017-11-13T20:34:00+01:00"
categories:  [ "coding" ]
tags:        [ "testing" ]
slug:        "nomenclature-des-tests-logiciels"
---

Lors de discussion sur les tests logiciels, je suis régulièrement surpris d'entendre que cela se résume à *test unitaire*, *test d'intégration* et *test fonctionnel*. En schématisant, le premier permet de tester le code, le deuxième l'intéraction de composants et le troisième le logiciel dans son ensemble. Hors, cette liste est largement incomplète.

Objectif d'un test
------------------

Avant de tenter une classification, il me semble opportun de s'interroger sur l'objectif d'un test :

- **Qui** exécute les tests ?
- **Òu** sont exécutés les tests ?
- **Comment** sont exécutés les tests ?
- **Quand** sont exécutés les tests ?
- Et enfin, qui est le principal **intéressé** par les résultats ?

Répondre à ces questions donne à mon sens une meilleure compréhension de ce que l'on cible, qui se retrouvera bien souvent dans la qualité des tests. Nous y reviendrons. Néanmoins je vous en parle dés maintenant pour vous pousser à répondre à ces questions à chaque type de test que vous allez lire par la suite dans ce billet. C'est un exercice certes un peu long mais à mon sens utile voir nécessaire pour mieux les appréhender. Je vous incite aussi à chercher ci et là d'autres nomenclatures pour complèter votre vision du sujet.

Introduction à la classification
--------------------------------

Il existe différentes charactéristiques que je tente humblement de lister, les critères n'étant pas simples à définir. Il existe surement d'autres critères ou de type de tests, je tente ici de donner ce qui me semble les plus importants.

**Note** : Je ne tente pas d'expliquer en détail chaque test, la documentation abondante sur le Net vous donnera largement satisfaction à ce sujet. Je laisse d'ailleurs la terminologie anglaise à cette fin.

Isolation
---------

C'est la caractéristique la plus usitée, qui correspond à l'introduction de ce billet : quelles sont mes dépendances ? J'aime à mettre en avant le terme isolation, même si je lis souvent *level testing* pour définir ce critère.


| Nom                              | Description                                                               |
| ---------------------------------| --------------------------------------------------------------------------|
| *Component testing*              | test sans aucune dépendance hormis le langage                             |
| *Integration testing*            | test d'intéraction sur plusieurs composants afin de tester les interfaces |
| *System testing*                 | test avec l'ensemble des composants                                       |
| *Operational acceptance testing* | test qui inclus l'environnement de production                             |

On voit souvent le terme de *end-to-end testing* (test de bout en bout) pour parler de tests qui cible l'ensemble des composants.

Le niveau integration est vaste, cela peut concerner du code comme des services.

Connaissance
------------

Quel est le niveau de connaissance du *SUT* (System Under Test, terme consacré voulant dire « le truc que l'on teste ») ?

| Nom                              | Description                                                                               |
| ---------------------------------| ------------------------------------------------------------------------------------------|
| *White-box testing*              | test en me connectant directement à l'implémentation                                      |
| *Black-box testing*              | test sans aucune connaisance de l'implémentation mais seulement du comportement extérieur |
| *Grey-box testing*               | test black-box tout en connaissant l'implémentation ou un mélange des 2 types de tests    |

Période
-------

Je regroupe ici les tests dont la temporalité joue : à quel moment est-il important d'avoir le résultat ?

| Nom                              | Description                                                                                           |
| ---------------------------------| ------------------------------------------------------------------------------------------------------|
| *Acceptance testing*             | test de validation d'une demande de fonctionnalité utilisateur                                        |
| *Regression testing*             | test (sur un code déjà testé) de validation de la correction d'un bug ou d'un changement involontaire |
| *Alpha testing*                  | test très en amont pour tester des idées sur un petit panel d'utilisateurs volontaires                |
| *Beta testing*                   | test en amont sur un nombre restreint d'utilisateurs volontaires avant la livraison officielle        |
| *Canary testing*                 | déploiement sur un petit nombre d'utilisateurs pour valider les changements                           |
| *A/B testing*                    | test permettant de deployer plusieurs versions d'un élément pour tester le comportement utilisateur   |
| *Sanity testing*                 | sous-ensemble de tests quand le temps manque pour jouer l'ensemble des tests                          |
| *Smoke testing*                  | test d'un sous-ensemble des cas d'utilisation qui couvre les fonctionnalités de base                  |

Quel est la différence entre *smoke* et *sanity* ? Les tests sanity sont le plus souvent lancés soit par manque de temps ou suite à de nombreux aller / retour en interne, permettant de tester la partie modifiée de l'application. Smoke est une approche plus « globale », par exemple en lançant tous les jours pour vérifier que l'ensemble des fonctionnalités de base est opérationnel.

Automatisation
--------------

| Nom                              | Description                                                               |
| ---------------------------------| --------------------------------------------------------------------------|
| *Manual testing*                 | test manuel                                                               |
| *Automation testing*             | test automatisé                                                           |
| *Semi-automation testing*        | test automatisé qui demande une interprétation manuelle des résultats     |

Les tests automatisés sont le saint graal que l'on doit atteindre. Mais il ne faut pas négliger le **coût** que cela peut atteindre, notamment en ce qui concerne les tests d'interface graphique, très lourd à maintenir. Dans ces conditions, il arrive souvent que des équipes optent pour un mélange de tests manuels, automatiques et semi-automatiques.

Couplage
--------

Je ne suis pas sûr du terme mais c'est pourtant celui qui, à mon sens, décrit le mieux la relation entre le code et le test.

| Nom                              | Description                                                               |
| ---------------------------------| --------------------------------------------------------------------------|
| *Functional testing*             | le test dépend du code                                                    |
| *Non-functional testing*         | le test ne dépend pas du code                                             |

« Test fonctionnel » est un des termes les plus mal employés. Pour mieux le définir, il est intéressant de partir de son contraire : le test non-fonctionnel. Nous pouvons lister par exemple les tests de type :

- performance / scalabilité
- configuration
- sécurité
- documentation
- UX
- interface graphique
- l10 / i18n

L'écriture de ces tests ne dépendent pas d'une action particuliére de l'utilisateur ou d'une fonction spécifique : écrire un test de peformance peut se faire quelque soit la technologie employée, idem pour un test de sécurité. Il est intéressant de noter que les tests non-fonctionnels donnent généralement une bonne idée de la qualité globale du produit, la faillite de ces dernières pouvant se traduire bien souvent par des problèmes systémiques.

On peut lister dans les tests fonctionnels :

- installation / mise-à-jour
- données / base de données
- fonctionnalité

Positivité
----------

| Nom                              | Description                                                               |
| ---------------------------------| --------------------------------------------------------------------------|
| *Positive testing*               | test pour aider les développeurs                                          |
| *Negative testing*               | test pour casser le code ou le produit                                    |

On voit souvent le terme de *destructive testing* pour ce dernier.

Je trouve ce critère fort intéressant et peu mis en avant. Si bien souvent les développeurs écrivent des tests pour se rassurer, proposer dans sa chaine de développement des tests négatifs est un gros plus. On peut ici parler de *fuzzing testing* et de *monkey testing* (ou *chaos testing*) qui consistent à trouver des erreurs en proposant un « comportement anormal » (du code, de l'utilisateur ou de l'environnement). Je vous engage à lire les résultats de tests de fuzzing qui sont souvent assez impressionnants, voir vous pousser à utiliser de temps en temps ce type de tests.

De même, une équipe qualité doit avant tout être dans une mentalité de casser le produit qu'elle teste pour le bien de tous (car il vaut mieux trouver une erreur avant que le client final). Et à titre personnel, j'attends aussi d'une revue de code une volonté de le casser, car c'est une autre façon de démontrer sa qualité.

Exemples
--------

Que peut on tirer de tout cela ? Prenons deux exemples très simples, en commençant par le test unitaire :

- Qui ? Le développeur.
- Òu ? Sur sa machine.
- Comment ? En lançant le framework de test unitaire.
- Quand ? À chaque fois que le développeur veut tester son code, idéalement à chaque modification.
- Intéressé ? Les développeurs.

Un test unitaire est donc un test écrit par ĺe développeur **pour** le développeur. Il est donc utile si ce dernier est lancé à chaque fois que le développeur en ressent le besoin, en étant rapide et facile à exécuter. Idèalement cela donne des tests qui se lance **dans** l'environnement de développement et dans le même langage de programmation que le code, et être inclus dans le workflow de ce dernier (revue de code, intégration continue, etc). En reprenant les caractéristiques listés précédemment, un test unitaire est de type :

- composant car le plus bas possible.
- automatique car c'est du code lancé par un framework de test (intégré ou non au langage).
- boite blanche car je connais l'implémentation du code puisque c'est exactement cela qui est testé.
- fonctionnel car dépendant de l'implémentation.

Essayons de réfléchir à un autre type de test, les tests d'acceptations :

- Qui ? Le PO (ou tout rôle qui conçoit les fonctionnalités utilisateur).
- Òu ? Dans un environnement complet.
- Comment ? En simulant un utilisateur.
- Quand ? À la livraison de la fonctionnalité.
- Intéressé ? Le PO.

Ah, c'est ici moins évident. Tout d'abord ce test peut-être écrit par le PO ou par le développeur. Il peut-être manuel ou automatisé. Ce dont on est sûre :

- boite noire car je me place du point de vue de l'utilisateur.
- fonctionnel car je teste la fonctionnalité.

Je laisse comme exercice au lecteur de définir les autres type de tests, par exemple le smoke testing et le sanity testing afin de mieux cerner les différences.

Conclusion
----------

J'espère que cet article sans prétention vous a donné envie d'en savoir plus sur le sujet passionnant qu'est le test logiciel et d'avoir un vocabulaire plus étoffé. Pour finir, un petit mot sur la norme ISO/CEI 9126 (remplacé par la 25010) qui définit un langage pour modéliser les qualités d'un logiciel appelée *SQuaRE* (software quality requirements and evaluation). Vous y trouverez peut-être une source d'inspiration:

- Functionality (existence de l'ensemble des fonctionnalités qui satisfont les besoins exprimés) : Suitability, Accuracy, Interoperability, Security, Functionality compliance.
- Reliability (capacité à maintenir un niveau de performance dans certaines conditions ou de durée) : Maturity Fault tolerance Recoverability Reliability compliance.
- Usability (effort pour utiliser) : Understandability, Learnability, Operability, Attractiveness, Usability compliance.
- Efficiency (relation entre niveau de performance et ressources utilisées) : Time behaviour, Resource utilization, Efficiency compliance.
- Maintainability (effort pour effectuer des modifications) : Analyzability, Changeability, Stability, Testability, Maintainability compliance.
- Portability (capacité à transférer d'un environnement à un autre) : Adaptability, Installability, Co-existence, Replaceability, Portability compliance.