# Grid Layout

Concevez une grille colorée adaptable pour les écrans suivants :

- mobile first
- mobile > 640px
- tablette format paysage > 768px
- petits écrans > 1024px
- écrans normaux > 1280px

## Les propriétés CSS

Les propriétés CSS à exploiter dans cet exercice sont : 

 - [`display: grid`](https://developer.mozilla.org/fr/docs/Web/CSS/display) activer le mode d'affichage en grille;
 - [`grid-template-areas`](https://developer.mozilla.org/fr/docs/Web/CSS/grid-template-areas) spécifier la disposition des zones nommées;
 - [`grid-template-columns`](https://developer.mozilla.org/fr/docs/Web/CSS/grid-template-columns) définie la taille des colonnes (avec l'unité de mesure de fraction de page `fr` de préférence);
 - [`grid-area`](https://developer.mozilla.org/fr/docs/Web/CSS/grid-area) attribuer une zone du template à un élément HTML.
 
### Exemple

Voici un exemple de grille de 3 colonnes avec des zones nommées.

~~~ css
/** Définition de la grille **/
.wrapper {
	display: grid;
	grid-template-columns: repeat(3, 1fr);
	grid-template-areas:
	"header navigation navigation"
	"content content aside"
	"footer footer footer"
	;
}

/** Attribution des zones de la grille **/
.main-header { grid-area: header; }
.main-navigation { grid-area: navigation; }
.content { grid-area: content; }
.ads { grid-area: aside; }
.main-footer {grid-area: footer;}
~~~

## Meta 

Afin d'éviter des problèmes de rendu de pages, il est important d'ajouter les deux métadonnées suivantes. 

La méta non stantard `viewport`, permet de spécifier aux terminaux mobile des préférences de taille de vue virutelle (viewport). La valeur `width` permet de spécifier une largeur de vue équivalente à celle du support (`device-width`); `initial-scale` définit le ratio entre la taille d'écran du mobile et la taille de la vue virtuelle.

~~~ html
<meta name="viewport" content="width=device-width, initial-scale=1">
~~~

La méta `HTTP-equiv` `x-ua-compatible`, permet d'indiquer aux agents utilisateurs le moteur de rendu de page désiré. En l'occurence, on indique à Internet Explorer (IE) d'utiliser le moteur de rendu Edge.

~~~ html
<meta http-equiv="x-ua-compatible" content="ie=edge">
~~~


## Ressources

### Les grilles
 - [Modèle de disposition en grille](https://developer.mozilla.org/fr/docs/Web/CSS/CSS_Grid_Layout)
 - https://gridbyexample.com/
 - [Inspecteur de grille de Firefox](https://developer.mozilla.org/fr/docs/Outils/Inspecteur/Comment/Examine_grid_layouts)
 - [Flexbox ou Grid Layout?](https://developer.mozilla.org/fr/docs/Web/CSS/CSS_Grid_Layout/Mod%C3%A8le_de_grille_et_autres_mod%C3%A8les_de_disposition)
 - [Apprendre Grid Layout en s'amusant](http://cssgridgarden.com/)
 - [Apprendre Flexbox en s'amusant](http://flexboxfroggy.com/)
 - [Les balises meta](https://developer.mozilla.org/fr/docs/Web/HTML/Element/meta)
 
### Inspirations graphique

#### Cubiste, abstrait
 - [Robert Delaunay]](https://fr.wikipedia.org/wiki/Robert_Delaunay), [œuvres de Delaunay](http://www.artnet.fr/artistes/robert-delaunay/);
 - [Hilma af Klint](https://en.wikipedia.org/wiki/Hilma_af_Klint), [œuvres de Klint](https://commons.wikimedia.org/wiki/Category:Paintings_by_Hilma_af_Klint);
 - [Otto Freundlich](https://fr.wikipedia.org/wiki/Otto_Freundlich), [œuvres de Freundlich](https://commons.wikimedia.org/wiki/Category:Otto_Freundlich?uselang=fr).
 
#### Arts concret
 - [Max Bill](https://fr.wikipedia.org/wiki/Max_Bill), [œuvres de Bill](http://www.artnet.fr/artistes/max-bill/).
 
#### Neoplasticisme
- [Theo van Doesburg](https://fr.wikipedia.org/wiki/Theo_van_Doesburg), [œuvres de Doesburg](http://www.artnet.fr/artistes/theo-van-doesburg/);
- [Aurélie Nemours](https://fr.wikipedia.org/wiki/Aur%C3%A9lie_Nemours), [œuvres de Némours](http://www.artnet.fr/artistes/aur%C3%A9lie-nemours/);
- [Piet Mondrian](https://fr.wikipedia.org/wiki/Piet_Mondrian), [œuvres de Mondrian](http://www.artnet.fr/artistes/piet-mondrian/).

