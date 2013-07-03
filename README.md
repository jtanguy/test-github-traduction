Test de traduction avec page de statut automatique
==================================================

Hiérarchie des fichiers
-----------------------

Le graphique suivant montre la hiérarchie des fichiers (les éléments entre
parenthèses représentent les branches dans lequel le fichier existe).

```
test-github-trad
|-- _config.yml (master, gh-pages)
|-- css (gh-pages)
|   |-- bootstrap.css
|   \-- style.css
|-- index.md (gh-pages)
|-- _layouts (gh-pages)
|   |-- default.html
|   \-- page.html
|-- chapitres (master, gh-pages)
|   |-- chap01.md (master, gh-pages, chap01)
|   |-- chap02.md (...)
|   |-- chap03.md (...)
|   \-- chap04.md (...)
\-- README.md (master, gh-pages, ...)
```

Chapitres
---------

Les chapitres peuvent être en format markdown ou html. Ils doivent cependant
comporter l'en-tête suivant:

```yaml
---
title: XX - Titre du chapitre
status: Publié/Relecture/En cours/Non traduit
layout: page
---
```

Le statut est indiqué dans l'entête status.
Il doit être modifié à chaque phase de vie du chapitre.
Concrètement, quand on change le statut d'un chapitre, il faut modifier le champ
status, commiter le changement[^1] dans la branche correspondante.
Le statut n'est mis à jour que si le commit est poussé dans la branche
`gh-pages`.


[^1]: Idéalement le commit ne devrait changer *que* le statut.
