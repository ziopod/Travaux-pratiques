# Hello World

Dans cette exercice, organisez un projet web très simple mais complet (HTML, CSS, sémantique, méta-données, etc.) d'une seule page.

L'exercice est simple, mais vous devez être rigoureux sur l'écriture du code et sur l'organisation et nommage des fichiers. 

Connaissances requises : 

 - gestion des fichiers et dossiers
 - connaissance générale de la composition d'une page web (HTML et CSS)


## Organisation du projet web

Un site internet est composé de multiple fichiers, leurs nombre augmenteras en même temps que l'évolution du projet. Ainsi il est capital de mettre en place une méthode permettant d'organiser fichiers et dossiers.

Une des permière chose à appliquer est de réspecter la sépartion des langage afin de simplifier l'évolution, et la maintenance du projet. Pour notre projet nous allons distinguer les différents composants de cette manière : 

~~~
  - index.html
  - assets
    - css
      - master.css
      - librairies
        - reset.css
  - index
    - medias
      - unicorn.gif
~~~

Vous remarquez **le dossier** `assets`, celui-ci contiendras tout les ressources nécessaire à l'affichage et au fonctionnement du site.

Dans notre cas il contient un dossier `CSS` pour notre feuille de style principale et un sous-dossier `librairies` qui contient une ressource `reset.css`, il s'agit d'une feuille style de remise à zéro maintenu et mis à disposition par d'autre développeur web (en l'occurence, il s'agit d'un des pères de la conception web moderne,  Eric Meyer).

De cette façon nos distingerons le code personnalisé (celui que l'on vas régulièrement modifier) du code provenant de librairies tierces (le code de provenant de librairies tierces ne doit en aucun cas être modifié au sein de notre projet).

Néanmoins, si vous avez vraiment besoins d'apporter des améliorations ou des corrections au code source d'une librairie, vous pouvez surclasser le fichier avec votre propre code dans un fichier séparé (en dehors de `librairies`) ou encore mieux, proposer l'amélioration aux personnes en charge de la publication de la librairie en question.

Le dossier contenant **des éléments rapportés à une page** spécifique devrons êtres placés dans un dossier portant le nom de la page. C'est le cas du médias `index/unicorn.gif` qui devras être affiché dans la page `index.html`.

L'organisation d'un projet peut varier en fonction des technologies ou des méthodes choisies par l'équipes de développement. Bien que le simple bon sens et l'expérience permettent de mettre au point une méthode  d'organisation efficace pour des petites projets; vous serez probalement amener à travailler sur des projets existants, il est donc important de ne pas trop dépendre d'une méthode d'organisation particulière, d'être curieux et de savoir s'adapter.

## Structure HTML

Votre fichier HTML devras suivre le standard W3C HTML5. Exploitez au mieux les marqueur HTML sémantiques et les marqueurs de méta-données.

Veillez à respecter la convention d'écriture [HTML codeguide.io](http://codeguide.co/#html).

## Les métas informations requises

Indiquez : 

 - la langue du contenu
 - l'encodage de caractère
 - description
 - mentions de l'auteur
 - Licence

## Le contenu

Présentez le contenu texte du fichier "[La Licorne.txt](La Licorne.txt)", y inclure le fichier média "unicorn.gif" sans omettre de mentionner l'auteur du média et les conditions de partage.

## Feuille de style

Votre feuille de style devras être simple et permettre une bonne lisibilité du contenu (police de caractère, presentation du visuel, légende, etc.). N'utiliser pas de frameworks ou librairies tierces.

Veillez à porter un soin particuiier au [noms de vos classes CSS](http://thesassway.com/advanced/modular-css-naming-conventions) et à respecter la convention d'écriture [CSS codeguide.io](http://codeguide.co/#css).

## Ressources

 - [Codeguide.io](http://codeguide.co)
 - [Conventions de nommage CSS](http://thesassway.com/advanced/modular-css-naming-conventions)
 - [MDN](https://developer.mozilla.org)
 - [reset.css](http://meyerweb.com/eric/tools/css/reset/)
