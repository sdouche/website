---
title: Worse is better
date: "2014-12-18T15:19:00+01:00"
categories: [ "rumination" ]
tags: [ "coding" ]
slug: "worse-is-better"
---


J'ai lu voici quelques mois un billet qui s'intitule [The Rise of Worse is Better](http://dreamsongs.com/RiseOfWorseIsBetter.html) par Richard P. Gabriel, développeur Lisp (qui a d'ailleurs monté une société autour de ce langage dans les années 80). Vieux billet puisqu'il date de 1989 dans sa version original. Il est, à l'origine, une section dans un essai nommé [Lisp: Good News, Bad News, How to Win Big](http://dreamsongs.com/WIB.html).

Dans ce billet, Gabriel expose deux visions du développement logiciel qu'il appelle la conception «The Right Thing» (approche MIT) et la conception «Worse is Better» (approche Stanford). Stanford et MIT se trouvant à San Francisco et l'autre à Boston, cela donne un arrière gout de *East Coast* vs *West Coast*.

Il définit chaque conception en quatre points : simplicité (simplicity), exactitude (correctness), cohérence (consistency) et complétude (completeness).

Worse is Better
---------------

Voici les quatre points :

- La conception doit être simple. tant dans son implémentation que dans son interface. Mais la simplicité d'**implémentation** est la plus importante.

- La conception doit être juste dans tous ses aspects observables, mais il est **préférable d'être simple que juste**.

- La conception doit être cohérente, mais on peut **sacrifier dans certains cas la cohérence pour la simplicité**. De plus, il est préférable de supprimer des bouts de conception qui introduise de la complexité ou de l'incohérence.

- La conception doit couvrir autant de situations que possible, mais on peut **sacrifier la complétude en faveur des autres caractéristiques** comme l’exactitude ou la cohérence, surtout si cela joue sur la complexité.

En schématisant, nous avons :

simplicité (implémentation) ❭ simplicité (interface) ❭ exactitude ❭ cohérence ❭ complétude

Nous pouvons voir que l'approche de Stanford se focalise avant tout sur la simplicité d'implémentation. La simplicité étant considérée comme l'objectif plus important, il peut sacrifier de l'exactitude. De même, il peut sacrifier de la cohérence si cela augmente la complexité. Et de la complétude si cela améliore les points précédents.

Gabriel décrit Unix et le langage C comme représentatif de cette approche.

The Right Thing
---------------

Voici les quatre points :

- La conception doit être simple. tant dans son implémentation que dans son interface. Mais la simplicité d'**interface** est la plus importante.

- La conception doit être juste dans tous ses aspects observables. **L'inexactitude n'est pas permise**.

- La conception doit être cohérente. On peut **sacrifier la simplicité et la complétude pour avoir de la cohérence**.

- La conception doit couvrir le plus de situations utiles. Il est **préférable d'être complet que simple**.

En schématisant, nous avons :

exactitude ❭ cohérence ❭ complétude ❭ simplicité (interface) ❭ simplicité (implémentation)

Au contraire de la première approche, l'approche MIT se focalise sur l'exactitude. La cohérence et la complétude sont plus importantes que la simplicité. Elle force le concepteur à un plus gros travail (pour avoir un code complet, exact et cohérent).

Son interprétation
------------------

Gabriel explique que l'approche qui prône la simplicité produit de meilleur résultat sur le long terme, en prenant par exemple Unix, qui pouvait être porté bien plus facilement sur de nouvelles plateformes, ce qui a permis à ce dernier de se développer plus rapidement. Pour mieux exposer les différences, il raconte une petite histoire entre deux personnes (Bill Joy et Dan Weinreb si je ne dis pas de bêtise) :

> Two famous people, one from MIT and another from Berkeley (but working on Unix) once met to discuss operating system issues. The person from MIT was knowledgeable about ITS (the MIT AI Lab operating system) and had been reading the Unix sources. He was interested in how Unix solved the PC loser-ing problem. The PC loser-ing problem occurs when a user program invokes a system routine to perform a lengthy operation that might have significant state, such as IO buffers. If an interrupt occurs during the operation, the state of the user program must be saved. Because the invocation of the system routine is usually a single instruction, the PC of the user program does not adequately capture the state of the process. The system routine must either back out or press forward. The right thing is to back out and restore the user program PC to the instruction that invoked the system routine so that resumption of the user program after the interrupt, for example, re-enters the system routine. It is called PC loser-ing because the PC is being coerced into loser mode, where loser is the affectionate name for user at MIT.

> The MIT guy did not see any code that handled this case and asked the New Jersey guy how the problem was handled. The New Jersey guy said that the Unix folks were aware of the problem, but the solution was for the system routine to always finish, but sometimes an error code would be returned that signaled that the system routine had failed to complete its action. A correct user program, then, had to check the error code to determine whether to simply try the system routine again. The MIT guy did not like this solution because it was not the right thing.

> The New Jersey guy said that the Unix solution was right because the design philosophy of Unix was simplicity and that the right thing was too complex. Besides, programmers could easily insert this extra test and loop. The MIT guy pointed out that the implementation was simple but the interface to the functionality was complex. The New Jersey guy said that the right tradeoff has been selected in Unix-namely, implementation simplicity was more important than interface simplicity.

> The MIT guy then muttered that sometimes it takes a tough man to make a tender chicken, but the New Jersey guy didn't understand (I'm not sure I do either).

Il caricature l'approche Stanford en l'a nommant «Worse is Better» et non «Less is More» pour bien montrer que c'est contre intuitif à ses yeux : On fait simple même si le résultat final n'est pas aussi complet et cohérent que l'on pourrait espérer. Il dit d'ailleurs « The good news is that in 1995 we will have a good operating system and programming language; the bad news is that they will be Unix and C++.»

Mon interprétation
------------------

Il faut savoir que ce texte a pas mal fait parlé de lui (et encore maintenant, la preuve avec ce billet). Gabriel à lui-même fait une critique (il dit ne sais pas savoir quoi en penser. Il est des fois pour, des fois contre). Si vous cherchez [Worse is better](https://www.google.fr/#q=worse+is+better) dans votre moteur de recherche, vous tomberez sur plusieurs textes assassins, qui critiquent fortement cette philosophie pour avoir favorisée la médiocrité en développement logiciel. D'autres critiques mettent en avant les contraintes économiques comme explication pour certaines évolutions comme Unix ou les processeurs x86. De plus, je pense qu'il faut prendre ce texte sans y ajouter la notion de qualité. Car la plupart des critiques que j'ai pu lire partait du principe que faire simple signifiait «gros hack», ce qui n'est pas valable. La qualité est orthogonale à la discussion (on peut mal coder dans les deux philosophies).

Pour ma part, je trouve ce texte intéressant car il formalise une vision du développement que j'ai depuis longtemps, à savoir que la simplicité est la mère de toutes les vertus. Cela étant dit, faire simple ne veut pas dire simpliste, ou ne pas avoir de complexité à la fin. Mais de toujours chercher à obtenir un résultat le plus «dépouillé». Car cela sera plus simple à manipuler et à modifier par la suite.

Gabriel parle de C et d'Unix, je voudrais rajouter quelques exemples :

- Internet (la pile TCP/IP) a grandi en même temps qu'un concurrent européen : X25 (développé à partir de 1976). Ce dernier était plus robuste et fiable puisque chaque hop s'assurait de la validité des paquets. A contrario, TCP/IP ne fait aucune vérification pendant le transport, l'intelligence se trouvant dans les extrémités du réseau (et non le cœur comme X25), rendant les hop bien plus facile à développer et moins couteux. Alors que TCP/IP fait tourner Internet, X25 était désuet en 1995...

- La micro-informatique est bien plus simple (voir pauvre pour certains) que les mainframes vendus depuis les années 60. Mais bien plus facile à comprendre et à manipuler, bien moins chers, ils se sont imposés un peu partout.

- Les réseaux locaux utilisent Ethernet, protocole assez basique inventé par Bob Metcalfe (au fameux centre Xerox Palto Alto. Il fonda plus tard 3Com). Il existait d'autres protocoles plus fiables comme Token Ring d'IBM. Mais bien plus couteux, le protocole Ethernet pris rapidement le pas. Et par sa conception simple, on est passé du 10BaseT au 10000BaseT.

- Git est un outil d'une conception incroyablement simple (Linus Torvalds a utilisé Git pour ses besoins au bout de 5 jours). Basé sur une implémentation réussie du DAG et de la notion de référence, Git libère le programmeur du carcan SVN (bien plus complexe dans sa conception).

- Linux s'est développé en noyau monolithique (conception simple), alors que certains lui prédisait une mort avec l'arrivée des micro-noyaux, bien mieux sur bien des aspects. 20 ans après, on sait ce qui est advenu.

- Plus généralement, la philosophie du Libre se rapproche du *Worse is better*. Faire simple. D'ailleurs Gabriel décrit dans un autre texte la proximité de son texte avec certaines idées de Richard Stallman.

Bien sûr, les choses ne sont jamais blanc ou noir, et des décisions économiques, bureaucratiques ou d'objectifs complexes, voir le hasard sont en partie à l'origine de certains résultats. Mais je pense sincèrement que d'avoir la simplicité d'implémentation comme vecteur principal de son développement est intéressant. Les exemples ci dessus ne sont pas anodins, car provenant tous du même milieu (Internet et Unix sont étroitement liés, Stallman et Torvalds ont inventés un Unix-like), milieu qui a imposé pas mal de ses technologies.

Et pour la petite histoire, Internet est aussi issu de la cote ouest, et ce n'est pas anodin (mais cela nous mènerait bien trop loin, mais je vous engage à lire l'histoire d'Internet qui est fort instructif).

Et alors ?
----------

N'est il pas dérisoire de tenter de définir précisément un cadre au développement logiciel, domaine tellement jeune (40 ans d’existence pour la micro-informatique, 65 ans pour l'informatique) et surtout immature ? Est ce que les partisans de la conception *The Right Thing* n'ont ils pas raison après tout, en stigmatisant la médiocrité des logiciels actuels ? N'est ce pas **ma** médiocrité intellectuelle qui me pousse dans les bras du *Worse is Better* car je suis incapable de faire mieux ? Mais alors, pourquoi les défenseurs des langages comme Scala, D, Ocaml ou Haskell, qui se font «entendre» avec force sur la toile (généralement avec des commentaires assassins), ne livrent pas eux même de meilleurs logiciels : Où est le prochain système d'exploitation en OCaml ? Le futur Git en Haskell ? Pourquoi Google, qui a surement embauché un grande partie d'excellents développeurs dans la décennie passée préfère Java, Python et le C++ ? Et que le nouveau langage qui perce avec force est Go, symbole du *Worse is Better* ?

 De plus, les études que j'ai pu lire ne sont pas plus concluants (d'ailleurs si vous en avez d'autres je suis preneur car je n'ai pas tout retrouvé) :

- [A Large Scale Study of Programming Languages and Code Quality in Github](http://macbeth.cs.ucdavis.edu/lang_study.pdf) (2014)

> «Most notably, it does appear that strong typing is modestly better than weak typing, and among functional languages, static typing is also somewhat better than dynamic typing. We also find that functional languages are somewhat better than procedural languages. It is worth noting that
these modest effects arising from language design are overwhelmingly dominated by the process factors such as project size, team size, and commit size. However, we hasten to caution the reader
that even these modest effects might quite possibly be due to other, intangible process factors, e.g., the preference of certain personality types for functional, static and strongly typed languages.»

- [An Empirical Study of Student Programming Bugs](http://digitalcommons.usu.edu/cgi/viewcontent.cgi?article=1077&context=honors) (2011)

> «By far, the most common frustration involved problem solving, i.e., students had difficulty understanding the problem statement on their assignment and designing a solution.»

- [An Analysis of Production Failures in Distributed Data-Intensive Systems](https://www.usenix.org/system/files/conference/osdi14/osdi14-paper-yuan.pdf) (201)

> «We found the majority of catastrophic failures (ndlr: 92%) could easily have been prevented by performing simple testing on error handling code – the last line of defense – even without an understanding of the software design. We extracted three simple rules from the bugs that have lead to some of the catastrophic failures, and developed a static checker, Aspirato, capable of locating these bugs. Over 30% of the catastrophic failures would have been prevented had Aspirator been used and the identified bugs fixed. Running Aspirator on the code of 9 distributed systems located 143 bugs and bad practices that have been fixed or confirmed by the developers.»

- [An Empirical Study of the Influence of Static Type Systems on the Usability of Undocumented Software](http://dl.acm.org/authorize?6743202) (2012)

> «We report on a controlled experiment where 27 subjects performed programming tasks on an undocumented API with a static type system (requiring type annotations) as well as a dynamic type system (which does not). Our results show that forsome tasks, programmers had faster completion times using a static type system, while for others, the opposite held.»

- [Programmers’ Build Errors: A Case Study (at Google)](https://static.googleusercontent.com/media/research.google.com/de//pubs/archive/42184.pdf) (2014)

> « An analysis of the errors found during the build process revealed that, independent of programming language, approximately 10 percent of the error types account for 90% of the build failures.»

- [Impact of aspect-oriented programming on software development efficiency and design quality](http://madeyski.e-informatyka.pl/download/Madeyski07g.pdf)

> «It turned out that aspect-oriented programming approach did not significantly affect software design quality metrics i.e. Dn, W OM, CBM, RFM, LCO, NCLOC and NCLOC2. It means that the impact of aspect-oriented programming on software design modularity and size (related to the goal 1) was not confirmed. In fact, the impact of aspectoriented programming on class-level software quality metrics (W OM, CBM, RFM, LCO) as well as on NCLOC and NCLOC2 was extremely weak, as suggested by the obtained effect size (r) values»

Ces études sont perfectibles à bien des égards mais se pourrait il que les arguments tant vantés par la communauté *The Right Thing* ne reposent en fait que sur des impressions, des envies ou des expériences passées ? Ne pourrait elle pas s'expliquer par une valorisation personnelle du type «j'utilise un langage avec plein de concepts compliqués ce qui me valorise ou m'amuse intellectuellent» ?

Ma **croyance** est que la simplicité est la clé du développement logiciel, car les objectifs de compréhension, de relecture et de modification sont les plus importantes. Ce qui implique le moins de connaissances à acquérir. Et ce n'est il pas finalement dans la recherche à 360 degrés de la simplicité (dans les techniques, les outils et l'organisation) que l'on peut puiser les meilleurs résultats et non un langage *The Right Thing* ? Par exemple :

- Un langage adapté aux besoins, possédant une petite spécification et qui ne demande pas de connaissances poussées en logique mathématique.
- La conception pilotée par les tests (TDD) qui pousse à réduire la complexité cyclomatique.
- La revue de code (et pair-programming) qui diminue le code «mappé du cerveau», car compréhensible par d'autres.
- Le refactoring pour raffiner le code (cohésion, découplage, extraction ,etc).
- Une taille d'équipe réduite et cohérente pour contrôler la complexité relationnelle.
- Le Kanban qui modélise une seule métrique organisationnelle (le temps de cycle)
- Le déploiement continue qui force à un déploiement maitrisé, donc simple.
- Garder une taille de code raisonnable.

Et que donc, la qualité passe avant tout par une **culture de la simplicité** ? Culture qui doit être régulièrement questionnée et travaillée ?

Un dernier mot sur Rust
-----------------------

Un dernier mot sur [Rust](http://www.rust-lang.org/), langage en court d'élaboration chez Mozilla. Je suis ce langage de près car il me semble être une tentative intéresasnte de rapprochement  de ces deux voies. Exact, complet, cohérent mais tentant de ne pas trop sacrifier la simplicité. Réponse dans un an avec la 1.0...
