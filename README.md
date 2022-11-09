# Gabarit Rmd pour le mémoire à l'Université Laval

Voici un gabarit .Rmd pour mémoire de maîtrise conforme aux normes de l'Université Laval.

En même temps de produire un pdf, le knit du fichier `index.Rmd` produit aussi un fichier LaTeX.
Ce fichier LaTeX peut être transmis en même temps que le dépôt de votre mémoire.

NB: Ce gabarit n'est pas approuvé officiellement par l'Université Laval.

# Dossier `/index`

Mis à part ce ReadMe, tout se trouve dans le dossier `/index`. Vous ne devez pas le renommer (car plus rien ne fonctionnera!).

## À l'intérieur du dossier `/index`

* Le dossier `/index` est le plus important. C'est ce fichier Rmd que vous «knitterez» pour produire votre pdf et votre tex (qui apparaitront dans `/_book`). Vous pourrez rédiger l'introduction de votre mémoire au bas de ce fichier, et inscrire vos informations pour la page titre en haut.

* Le dossier `/_book` va être là où apparaitront vos fichiers pdf et tex après le knit.

* Vos sources doivent se trouver dans le fichier `bibfile.bib`, inclus dans le dossier `/bib`.

* Le dossier `/csl` contient le bon format pour la bibliographie.

* Vous devez insérer toutes vos figures dans le dossier `/figure`.

* Le dossier `/_misc` contient un ramassis de trucs utiles, mais à ne pas toucher.

* `_bookdown.yml` permet de renommer vos fichiers pdf et tex et d'indiquer les noms des fichiers Rmd à inclure dans le knit.

* Les fichers Rmd numérotés suivent. C'est à l'intérieur que vous rédigerez les différentes section de votre mémoire. Ce n'est pas, par contre, les fichiers que vous devez «knitter».

* Ne touchez pas à `chemarr.sty`.

* `template.tex` contient le code pour produire le format de votre mémoire. Normalement, à moins de problème ou de demande de modification, vous ne devriez rien y changer.

* `ulaval.cls` contient les normes ULaval pour le mémoire. Normalement, à moins de problème ou de demande de modification (comme l'année, à la ligne 337), vous ne devriez rien y changer.

# Comment utiliser ce gabarit

Installer les prérequis

```
install.packages(c('tinytex', 'rmarkdown'))
tinytex::install_tinytex()
# Après le redémarrage de RStudio, confirmer que vous avez LaTex avec
tinytex:::is_tinytex()

if (!require("remotes")) 
  install.packages("remotes", repos = "https://cran.rstudio.org")
remotes::install_github("rstudio/bookdown")
remotes::install_github("ismayc/thesisdown")
```

Créer le fichier PDF final: ouvrir le fichier `index.Rmd` et knit.

# Crédits

* Maxime Blanchard
* Adrien Cloutier
* Judith Bourque

Ce gabarit est basé sur le package [thesisdown](https://github.com/ismayc/thesisdown)
