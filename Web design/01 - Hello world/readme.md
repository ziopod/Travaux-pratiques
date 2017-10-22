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
      - fonts
        - libre-baskerville.css
        - libre-baskerville
            - LibreBaskervilleRegular.eot
            - LibreBaskervilleRegular.svg
            - LibreBaskervilleRegular.ttf
            - LibreBaskervilleRegular.woff
            - LibreBaskervilleRegular.woff2        
  - index
    - medias
      - unicorn.gif
~~~

Vous remarquez **le dossier** `assets`, celui-ci contiendras tout les ressources nécessaire à l'affichage et au fonctionnement du site.

Dans notre cas il contient un dossier `CSS` pour notre feuille de style principale et un sous-dossier `fonts`qui contiendras nos jeux de fontes de caractères dans divers formats. La feuille de style `libre-baskerville.css` est une [definition de notre police de caractère](https://developer.mozilla.org/fr/docs/Web/CSS/@font-face).

Le dossier contenant **des éléments rapportés à une page** spécifique devrons êtres placés dans un dossier portant le nom de la page. Par exemple, cela sera le cas de votre média image à ajouter sur la page d'index, le fichier devra être stocké dans le dossier `index/unicorn.gif`.

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

Présentez le contenu texte du fichier "[La Licorne.txt](La Licorne.txt)", y inclure un fichier média image sans omettre de mentionner l'auteur du média et les conditions de partage.

## Feuille de style

Votre feuille de style devras être simple et permettre une bonne lisibilité du contenu (police de caractère, presentation du visuel, légende, etc.). N'utiliser pas de frameworks CSS ou de librairies CSS tierces autre que les jeux de polices de caractères.

Veillez à porter un soin particuiier au [noms de vos classes CSS](http://thesassway.com/advanced/modular-css-naming-conventions) et à respecter la convention d'écriture [CSS codeguide.io](http://codeguide.co/#css).

## Police de caractère

Veuillez [définir et appliquer au minimum un jeu de police de caractère](https://developer.mozilla.org/fr/docs/Web/CSS/@font-face). Choisissez une police de caractère Open Source et utilisez un [convertisseur de polices de caractères](https://everythingfonts.com/font-face) afin d'avoir à disposition les divers formats compatibles avec les différents agents utilisateurs (navigateurs web).

Pour intégrer vos définitions de polices de caractères, vous exploiter [la directive `@import`](https://developer.mozilla.org/en-US/docs/Web/CSS/@import).

## Ressources

 - [Codeguide.io](http://codeguide.co)
 - [Conventions de nommage CSS](http://thesassway.com/advanced/modular-css-naming-conventions)
 - [MDN](https://developer.mozilla.org)
 - [Les sélécteurs CSS avec CSS Diner](http://flukeout.github.io/)
 - [Polices de caractères Open Sources](https://github.com/brabadu/awesome-fonts#free-fonts)
 - [Définir une police de caractère](https://developer.mozilla.org/fr/docs/Web/CSS/@font-face)
 - [Convertir une police de caractère dans divers format](https://everythingfonts.com/font-face)
 - [Chargement dynamique de polices de caractères](https://www.filamentgroup.com/lab/font-events.html)