# Game of grids

Introduction aux grilles CSS.

Dans cet exercice, vous devrez concevoir une grille web CSS afin de présenter
de manière simple et lisible un contenu sous plusieurs plateformes (smartphone,
tablette et écran de portable ou de bureau).

Veillez à produire un code concis en respectant les principes [KISS](https://en.wikipedia.org/wiki/KISS_principle) et [DRY](https://fr.wikipedia.org/wiki/Ne_vous_r%C3%A9p%C3%A9tez_pas).
Pour conserver une bonne tenue du code, il est recommandé d'appliquer
les conventions d'écriture [SMACSS](https://smacss.com/) et [Codeguide](http://codeguide.co/).

Vous devez aborder la conception en commençant par considérer la plateforme
qui demande le plus d'attention selon la méthode du "[mobile first](https://responsivedesign.is/strategy/page-layout/mobile-first)".

Connaissances requises : 

 - les base du CSS
 - les bases de HTML
 - le flux HTML
 - les modèles de boites CSS
 - les medias queries CSS

Méthodologies et principes à respecter : 

 - [KISS](https://en.wikipedia.org/wiki/KISS_principle) et [DRY](https://fr.wikipedia.org/wiki/Ne_vous_r%C3%A9p%C3%A9tez_pas)
 - [SMACSS](https://smacss.com/) et [Codeguide](http://codeguide.co/)
 - [Mobile First](https://responsivedesign.is/strategy/page-layout/mobile-first)

 Contenu à afficher (6 entrées min.) : 

 - Titre
 - Visuel
 - Description
 - Caractéristiques

Ressources avec autorisation de publication pour cet exercice : 

 - <https://fr.wikipedia.org/wiki/Personnages_du_Tr%C3%B4ne_de_fer>
 - <https://commons.wikimedia.org/wiki/Category:Coats_of_arms_from_A_Song_of_Ice_and_Fire>

## Le contenu

Le contenu est de type « index de contenu », il est composé de multiples entrées
d'un catalogue de contenu.

En voici un exemple

	<article>
		<h1>Maison Stark</h1>
		<figure>
			<img src="house_stark.jpg" alt="Visuel de la maison Stark">
		</figure>
		<p>
			La maison Stark est la maison suzeraine du Nord et son siège se
			situe à Winterfell. Leur blason est un « loup-garou » gris sur
			champ blanc.
		</p>
		<ul>
			<li>Lieu : Winterfell</li>
			<li>Devise : « L'hiver vient »</li>
			<li>
				Personalités : 
				<ul>
					<li>Eddard Stark</li>
					<li>Catelyn Stark</li>
				</ul>
			</li>
		</ul>
		<dl>
			<dt>></dt>
			<dt>Devise de la maisons Stark</dt>
			<dl>« L'hiver vient »</dl>
		</dl>
	</article>

À vous de compléter le contenu, un minimum de 6 entrées est demandé.

## La grille
La grille seras conçues avec la méthode du flottant avec colonnes fluides, pour cela les règles
CSS suivantes devront être utilisées :

**Le conteneur**, servant à centrer le contenu dans la fenêtre du navigateur.

 	.wrapper {
 		width: 100%;
 		margin-left: auto;
 		margin-right: auto;
 	}

L'**initialisation** d'une colonne.

	.column {
		box-sizing: border-box;
		float: left;
		/** Gouttières **/
		padding-left: .5em;
		paddint-right: .5em;
	}

**Définition** de la largeur d'une colonne.

	.column-1-2 {
		width: 50%;
	}

Un **utilitaire** de désamorçage de flottant.

	.clear {
		clear: both;
	}

## Rendu adaptatif

La page devras être adptative avec l'usage des medias queries. Cela passera
par la gestion de la largeur du conteneur (wrapper) et de l'application de
diverses tailles de colonnes aux éléments HTML en fonction de l'espace
d'affichage disponible.

Il est demandé de rendre la page adpatable aux largeurs d'écrans suivantes : 

 - smartphone,
 - écrans de tablettes,
 - écrans d'ordinateurs portables.

La directive CSS `@media` vous permettras de déclencher des régles CSS en
fonction de la largeur de fenêtre de navigation (points d'arrêts).

Pour définir vos points d'arrêts, vous pouvez utiliser les largeurs de
fenêtres de navigateurs suivantes :

 - phone > 0
 - tablet > 768px
 - laptop > 1024px

N'oubliez pas que vos points d'arrêts doivent être définis en unité de mesure
relative à la taille de fonte de l'élement HTML body. Il vous suffit
d'appliquer la règle de trois suivante `target-size / base-font-size = em-size`.

Par exemple, pour un point d'arrêt d'écran d'ordinateur portable avec une
taille de corps de fonte par défaut (16px), faite le calcul suivant :

	1024 / 16 = 64

Spécifiez votre point d'arrêt ainsi : 

	@media only screen and (min-width: 64em) { … }

À titre d'exemple, voici les points d'arrêts par défaut de quelques framework CSS : 

 - Pure : 568px, 768px, 1024px, 1280px
 - Bootstrap: 544px, 768px, 992px, 1200px
 - Foundation: 640px, 1024px

### Le conteneur

Le conteneur devras avoir une largeur contrainte en fonction de la taille
d'écran.

En premier lieu, veillez à définir une largeur maximum pour votre wrapper,
ajouter la règle suivante à la délcaration de votre wrapper :

	max-width: 1280px; /** Laptop au maximum **/

Il sera nécessaire de spécifier une nouvelle largeur de wrapper à chaque
nouvelle taille d'écran, par exemple pour les écrans de tablettes :

	@media only screen and ( min-width: 48em ) {
		.wrapper { width: 1000px; }
	}


### Les colonnes

Plusieurs méthodes peuvent utiliser afin de gérer les définitions de colonnes
(fluide, fixe, semantique, …). Nous utiliserons la méthode la plus simple à mettre
en œuvre : les colonnes fluides appliqués par classes CSS.

Les largeurs seront exprimés en pourcentage, d'une valeur equivalent à `100 /
grid-system * column-numbers`. Par exemple pour une colonne correspondant au
deux tiers (4 colonnes) d'un sytème de grille de 6 colonnes, nous calculerons :

	100 / 6 * 4 = 66,667

Ce qui donnera une définition de colonne comme ceci : 

	.column-4-6 { width: 66.667%; }

Il s'agit de déclarer en premier lieu les colonnes pour les supports mobiles
(moblie first), un système de grille de 2 colonnes est généralement suffisant :

	.column-1-2 { width: 50%;}
	.column-2-2 { width: 100%;}

Puis, pour les tailles d'écrans supérieurs, nous déclencherons un système de grille de 3 :

	@media only screen and ( min-width: 48em) {
		.column-1-3 { width: 33.334%; }
		.column-2-3 { width: 66.667%; }
		.column-3-3 { width: 100%; }
	}

Ainsi pour definir un bloc d'une demi-largeur pour mobile et de deux tiers
pour tablette, il suffira de déclarer dans notre structure HTML :

	<div class="column column-1-2 column-2-3">
		…
	</div>

Vous remarquerez que certaines déclarations de classes appliquent exactement
les mêmes propriétes et valeurs CSS, elle devront être regroupées
afin d'optimiser le code.

À vous de completer et d'appliquer le reste du système de grille.

## Lectures sur le sujet

Design web :

 - <http://alistapart.com/article/dao> en Français : <http://www.pompage.net/traduction/dao>

Les points d'arrêts : 

 - <http://alistapart.com/article/designing-for-breakpoints>
 - <https://responsivedesign.is/strategy/page-layout/defining-breakpoints>
 - <https://cloudfour.com/thinks/the-ems-have-it-proportional-media-queries-ftw>

Tutoriels sur la conception de grilles web : 

 - <https://css-tricks.com/dont-overthink-it-grids/>
 - <http://alistapart.com/article/fluidgrids>
 - [Five simple steps for designing grid system - part 1](http://www.markboulton.co.uk/journal/five-simple-steps-to-designing-grid-systems-part-1)
 - [Five simple steps for designing grid system - part 2](http://www.markboulton.co.uk/journal/five-simple-steps-to-designing-grid-systems-part-2)
 - [Five simple steps for designing grid system - part 3](http://www.markboulton.co.uk/journal/five-simple-steps-to-designing-grid-systems-part-3)
 - [Five simple steps for designing grid system - part 4](http://www.markboulton.co.uk/journal/five-simple-steps-to-designing-grid-systems-part-4)
 - [Five simple steps for designing grid system - part 5](http://www.markboulton.co.uk/journal/five-simple-steps-to-designing-grid-systems-part-5)
