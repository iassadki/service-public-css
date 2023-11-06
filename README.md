# TP CSS - Ilias ASSADKI
Lien pour acceder au site : https://iassadki.github.io/tp_css/

### Logique générale du site 
Une grande partie du site est fait en `CSS`. Pour certaines grids, j'ai utilisé **Bootstrap**.

#### Header
Pour l'image du header, je l'ai géré avec background repeat de l'image `bg-contenu2.jpg`.
```css
	header {
		background-color: #cddee8;
		background-image: url('assets/bg-contenu2.png'); ### ICI ###
		background-repeat: repeat;
		padding: 10px;
	}
```

#### Navbar
Pour l'image de la navbar, je l'ai géré avec background repeat de l'image `bkg_menu_demarches.jpg`.
```css
	.menu-list>li>a {
		color: #0059cd;
		background-color: #cddee8;
		background-image: url('assets/bkg_menu_demarches.jpg'); ### ICI ###
		background-repeat: repeat;
		padding: 20px;

		text-decoration: none;
		padding: 10px;
		display: block;
		text-align: center;
		width: 100%;
	}
```

#### Organisation de `contenu_principal` et de `colonne_droite`
Pour le `contenu_principal` ainsi que la `colonne_droite`, j'ai utilisé classe `row` et la grid de bootstrap pour la gestion des layouts sur PC, Tablette et Smartphone.

La section globale du site est ici divisée en deux parties principales : `main` (à gauche) et `aside` (à droite)

- col-xl : device supérieur ou égal à 1200px
- col-md : device supérieur ou égal à 768px
- col-xs : device inférieur à 576px

- En version PC, j’utilise "col-xl-9". Ici, la colonne occupera 9/12 de l'écran sur des écrans de grande taille (XL).
- En version tablette, j’utilise "col-md-12". Ici, la colonne occupera 12/12 de l'écran sur des écrans de taille moyenne (MD).
- En version smartphone, j’utilise "col-xs-12". Ici, la colonne occupera 12/12 de l'écran sur des écrans de très petite taille (XS).

À l'intérieur de la colonne `main`, les éléments de **`contenu_principal`** sont configurés pour s'adapter à différentes tailles d'écran. 
J’utilise respectivement pour les ordinateurs, tablettes et mobile  `col-xl` `col-md-12` `col-xs-12`
La colonne `aside` contient la **`colonne_droite`**. J’utilise ici respectivement pour les ordinateurs, tablettes et mobile `col-xl` `col-md-12` `col-xs-12` 

#### Footer
Pour le footer, en version PC, je l'ai géré en CSS. J'ai utilisé la grid pour le diviser en 6 colonnes. Et je l'ai ensuite stylisé. 
Pour la version mobile et tablette, j'ai pas eu besoin d'utiliser grid, vu que les elements s'empilent les uns sur les autres. 
```css
	/* Grid du Footer */
	.grid {
		display: grid;
		grid-template-columns: repeat(6, 1fr);
		text-align: left;
	}

	.grid>div {
		padding: 1px;
		border: 0px solid #ccc;
	}

	.grid p {
		font-weight: bold;
	}

	.grid a {
		font-size: 12px;
		color: white;
		text-decoration: none;
	}
```

#### Gestion des media queries
**Desktop**
```css
@media screen and (min-width: 1024px) and (max-width: 2000px)
```

**Tablette**
```css
@media (min-width: 500px) and (max-width: 1023px)
``` 

**Smartphone** 
```css
@media screen and (min-width: 0px) and (max-width: 500px)
```
