---
title: "Installer Python à partir des sources"
date: "2015-01-06T08:30:00+01:00"
categories: [ "feedback", "presentation" ]
tags: [ "tools", "python" ]
slug: "installer-python-sources"
---

J'ai toujours utilisé une distribution Linux à base de paquets binaires (Ubuntu, Debian...), trouvant ce mode de fonctionnement plus reposant que de compiler soi même tout un tas de projets dans divers langages. C'est souvent source d'erreurs incompréhensibles et de longs moments de solitude. Néanmoins, il existe plusieurs avantages de le faire pour un langage de programmation comme Python :

- Ne pas toucher à l'interpréteur de la distribution et aux packages utilisés par le systême.
- Utiliser un interpréteur *vanilla*, sans modification par la distribution.
- Ou inversement appliquer un patch maison.
- Tester son code sur une version en développement.
- Disposer de versions que votre distribution ne gère pas.
- Disposer d'une nouvelle version sans attendre la prochaine version de la distribution.
- Avoir des options de compilations différentes.

L'avantage le plus intéressant pour moi est de ne pas toucher à l'interpréteur de la distribution. Ubuntu utilisant massivement Python, je n'ai pas envie de trop de le trafiquer (cela dit, une utilisation systématique de *virtualenv* donne un résultat identique).

 En 10 ans de compilation maison de l'interpréteur Python (je parle de CPython, l'interpréteur de référence), je n'ai jamais eu de soucis. De plus la procédure est triviale :

- Télécharger le tarball sur le site web (par exemple la [3.4.2](https://www.python.org/ftp/python/3.4.2/Python-3.4.2.tar.xz))
- Décompresser
- Lancer `configure; make; make install`

Et c'est tout. La compilation se passe en 4 étapes :

1. *configure* vérifie que vous avez les dépendances requises le cœur de l'interpréteur
2. Compilation du cœur
3. Compilation des modules
4. Installation

Le plus difficile est d'avoir toutes les dépendances nécessaires pour les modules. Je vous conseille d'y faire attention pour éviter des erreurs stupides à l'exécution. Il faut vérifier à la fin de la compilation les modules non compilés, par exemple :

```
Python build finished successfully!
The necessary bits to build these optional modules were not found:
_dbm                  _gdbm                 _tkinter
To find the necessary bits, look in setup.py in detect_modules() for the module's name.
```

 Voici les paquets à installer sur Ubuntu 14.10 avant de compiler Python :

```
$ sudo apt-get install build-essential libz-dev libreadline-dev libncursesw5-dev libssl-dev \
 libgdbm-dev libsqlite3-dev libbz2-dev liblzma-dev libdb-dev zlib1g-dev libdb-dev libdb5.3-dev \
 libffi-dev libgdbm-dev libmpdec-dev libxft-dev tcl-dev tcl8.6-dev tk-dev tk8.6-dev
```

Vous pouvez aussi utiliser la commande `sudo apt-get build-dep python2.7 python3.4` pour installer automatiquement les dépendances des paquets de la distribution, ou tout simplement vous en inspirer. N'oubliez pas cependant d'ajouter les sources dans votre configuration apt.

Et comme je suis fainéant, j'utilise un outil pour me simplifier la vie : pyenv.

Présentation de pyenv
---------------------

Pyenv ([lien](https://github.com/yyuu/pyenv)) est un outil qui permet :

- d'installer une version de Python en une seule commande.
- de surcharger votre environnement pour utiliser un Python local.
- de switcher facilement entre vos interpréteurs.
- de lancer une version précise pour un besoin ponctuel.

Installation
-------------

L'installation sous Linux est triviale :

```
$ git clone git://github.com/yyuu/pyenv.git ~/.pyenv
```

Puis modifier son environnement pour ajouter un chemin (configuration qui depend de votre shell, je vous laisse lire la documentation). Vous avez maintenant un pyenv fonctionnel :

```
$ pyenv
pyenv 20141211-6-g995da2d
Usage: pyenv <command> [<args>]

Some useful pyenv commands are:
   commands    List all available pyenv commands
   local       Set or show the local application-specific Python version
   global      Set or show the global Python version
   shell       Set or show the shell-specific Python version
   install     Install a Python version using python-build
   uninstall   Uninstall a specific Python version
   rehash      Rehash pyenv shims (run this after installing executables)
   version     Show the current Python version and its origin
   versions    List all Python versions available to pyenv
   which       Display the full path to an executable
   whence      List all Python versions that contain the given executable

See `pyenv help <command>' for information on a specific command.
For full documentation, see: https://github.com/yyuu/pyenv#readme
```

Fonctionnement
--------------

Le principe de pyenv est d'utiliser un *shim*, autrement dit d'intercepter les commandes que vous tapez pour les rediriger le bon interpréteur en lisant sa configuration. Cela fonctionne de la même façon pour tout logiciel que vous installez avec lui :

```
$ which python
/home/sdouche/.pyenv/shims/python
$ which pip
/home/sdouche/.pyenv/shims/pip
```

Utilisation
-----------

Vous avez beaucoup de versions à votre portée :

```
$ pyenv install --list
Available versions:
  2.1.3
  2.2.3
  2.3.7
  2.4
  2.4.1
  2.4.2
  2.4.3
  2.4.4
  2.4.5
  2.4.6
  2.5
  2.5.1
  2.5.2
  2.5.3
  2.5.4
  2.5.5
  2.5.6
  2.6.6
  2.6.7
  2.6.8
  2.6.9
  2.7-dev
  2.7
  2.7.1
  2.7.2
  2.7.3
  2.7.4
  2.7.5
  2.7.6
  2.7.7
  2.7.8
  2.7.9
  3.0.1
  3.1-dev
  3.1.3
  3.1.4
  3.1.5
  3.2-dev
  3.2
  3.2.1
  3.2.2
  3.2.3
  3.2.4
  3.2.5
  3.2.6
  3.3.0
  3.3-dev
  3.3.1
  3.3.2
  3.3.3
  3.3.4
  3.3.5
  3.3.6
  3.4.0
  3.4-dev
  3.4.1
  3.4.2
  3.5-dev
  ...
  ```

Pour installer Python 3.4.2 (ajoutez l'option `-v` pour voir la sortie standard) :

```
$ pyenv install 3.4.2
```

Puis mettre la 3.4.2 en version par défaut :

```
$ pyenv global 3.4.2
$ pyenv versions
  system
* 3.4.2 (set by /home/sdouche/.pyenv/version)
```

L’interpréteur se trouve dans le répertoire `~/.pyenv/versions/3.4.2/`.

Une fois l'interpréteur installé, pyenv télécharge et installe automatiquement Setuptools et Pip, ce qui vous évite ces tâches fastidieuses.

La commande `pyenv shell` change simplement la variable d'environnement `PYENV_VERSION` qui permet de surcharger le choix de l'interpréteur dans le shell courant :

```
$ pyenv shell 2.7.9
setenv PYENV_VERSION "2.7.9"
$ pyenv versions
  system
* 2.7.9 (set by PYENV_VERSION environment variable)
  3.4.2
```

La commande `pyenv local` permet quand à elle de définir un interpréteur par répertoire, en y écrivant un fichier `.python-version` (la variable d'environnement `PYENV_VERSION` étant prioritaire) :

```
$ mkdir test
$ cd test
$ pyenv local 2.7.9
$ cat .python-version
2.7.9
$ pyenv versions
  system
* 2.7.9 (set by /home/sdouche/test/.python-version)
  3.4.2
```

N'oubliez pas de taper la commande `pyenv rehash` quand vous installez des applications.

Couplage avec Virtualenv
------------------------

Pyenv possède une extension pour virtualenv, permettant d'utiliser un environnement virtualisé comme un envionnement classique pyenv.

Installation de l'extension :

```
$ git clone https://github.com/yyuu/pyenv-virtualenv.git ~/.pyenv/plugins/pyenv-virtualenv
```

Vous pouvez maintenant créer un environnement virtualisé :

```
$ pyenv virtualenv venv342
$ pyenv versions
  system
* 3.4.2
  venv342
```

Conclusion
----------

Cela fait des années que j'utilise avec succès ce type d'outil (pyenv maintenant, pythonbrew avant), autant en perso qu'en pro sans souci particulier. L'association pyenv + pyenv-virtualenv permet de toujours avoir un environnement propre, n'hésitant pas à multiplier les environnements virtualisés pour chaque besoin particulier. Et je peux aisément tester mon code avec plusieurs versions de Python et changer de version quand j'en ai besoin. Bref un outil de **base** dans ma panoplie.
