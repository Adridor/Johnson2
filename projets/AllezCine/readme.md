# Travail Intégration : AllezCiné

- Repository : `frontend-AllezCine`
- Temps nécessaire : 2 semaines
- Deadline : vendredi 29/06 à 17:00
- Travail : équipe de 2
- Formulaire de remise du projet : https://goo.gl/forms/pvYuVv1UOUFyT3PA3

## Objectifs d'apprentissage
- respecter un design fourni
- consolider les acquis en git, HTML, CSS, Bootstrap
- utiliser javascript et jQuery dans un projet réaliste
- avoir un nouveau projet à ajouter à son portfolio

## Le Travail d'intégration Front-End

Vous avez **2 travaux en rendre** :
- Un site en ONE PAGE [avec un design fourni](./layout-one-v2.jpg) que vous devez respecter au maximum. [[Accès rapide]](#a--site-avec-layout)
- Création d’une newsletter pour faire la promo des nouveautés sur votre site. [[Accès rapide]](#b-la-newsletter)

Pour cela, vous devez utiliser les technologies vues depuis le début, c’est à dire :
- HTML
- CSS
- JavaScript
- jQuery
- Responsive design
- Bootstrap
- Font Awesome Icons

**Avant toute chose**, sachez qu'il vous faudra 
- rédiger un readme.md indiquant (au minimum) la description du projet ainsi que le noms des membres de l'équipe ;
- rédiger une brève description dans le repo

**Utilisation d'un kanban**

Utiliser l'onglet [Projects] de votre repo pour créer et organiser votre travail grâce à ceci :
![kanban](https://github.com/becodeorg/BeCode/blob/master/img/kanban.jpg)

Des colonnes "to do", "in progress", "done" pour faire simple et des tickets attribués aux bonnes personnes. Ceci pour vous/nous permettre de visualiser clairement et simplement l'avancement du projet.

## A . Site avec LAYOUT

Vous allez réaliser, en groupe, un site internet de location et vente des films. ATTENTION, il s'agit d'un site en **one-page** !

- [Cliquez ici pour voir le layout](layout-one-v2.jpg)
- On met également à votre disposition quelques affiches de films, histoire de vous faire gagner un peu de temps (les titres, années et genre sont dans les noms des images. De rien.)

### Entrée
Lorsqu’on entre dans le site, il faut **contraindre l’utilisateur à indiquer son âge**.
S’il a 18 ans et plus, l’autoriser à entrer sur le site, sinon le rediriger vers IMDB. (Pour cela utiliser JS ou jQuery pour un pop-up).

Une fois sur le site, faire apparaître n’importe où sur le site une box pour la **mise en garde de cookies**. Pour un exemple GDPR friendly, [consultez le site de la CNIL](https://www.cnil.fr/fr/site-web-cookies-et-autres-traceurs).

 Lorsqu’on clique sur les boutons [login] ou [register], faire apparaître en JS ou jQuery dans une box un formulaire de connexion. (voir le site http://www.commeaucinema.com)
 
 Ce formulaire de connexion contiendra :
 - identifiant,
 - password,
 - un bouton [OK],
 - un bouton [Créer un compte],
 - un [rester connecté],
 - un lien [Si vous avez oublié votre mot de passe],
 - et un lien [cancel].
 
 Pour le formulaire register
 - Nom
 - E-mail
 - Password
 - Confirm password
 - Conditions générales d'utilisation bouton [Select]
 - Bouton [Register]

(Difficulté : faire disparaître le formulaire lorsqu'on clique sur CANCEL, en-dehors du formulaire ou sur le bouton register).

### Menu
Un **menu** en bootstrap avec des sous-menus. (**Menu hamburger pour le responsive**).

Comme c’est une onepage, les liens du menu doivent pointer vers les sections dédiées.

### En-tête
Le **jumbotron** de l'entête doit faire 100% de la largeur de l'écran dans lequel il y a un slide (Cf layout). Faire fonctionner le **slide** en CSS ou en JS ou jQuery)

### Les boutons réseaux sociaux
Les **boutons de réseaux sociaux** sont en position fixe. Si on clique sur un bouton, il doit s’allonger avec une animation (ici utilisez juste du CSS). Les réseaux sont twitter, facebook, dribbble et google plus.

### Section Films
Chaque film doit comporter :
- une affiche,
- un titre,
- l’année de sortie,
- et le genre.

Si on clique sur l’image ou titre du film, faire apparaître dans un modal (Bootstrap) le trailer youtube du film, la description, le réalisateur, l’année de sortie du film, le genre, les acteurs…

### Section Featured Movies
Créer des boutons pour filtrer les films par genre (jQuery ou JS).
Si on clique sur le bouton ACTION par exemple, afficher uniquement les films d’actions, etc...

Lorsqu’on clique sur le bouton “plus des films”, afficher les autres films cachés. Faire disparaître le bouton “plus des films” et le remplacer par le bouton “moins des films” si on clique sur “moins des films”, cacher les films et faire réapparaître le bouton “plus des films“  (En jQuery, ce sera plus facile, avec un toggle par exemple).

### Section Shop Movie
Utiliser les deux petits boutons à droite pour faire défiler les films de gauche à droite et vise-versa (jQuery, Bootstrap, JS au choix)

### Section Contact Us
Créer un formulaire (dans la page HTML, pas dans un pop-up). Lorsque l'utilisateur clique sur [send message], faites en sorte que les entrées du formulaire s'affichent dans un pop-up. (Pas de traitement en PHP, prochainement promis)

Petite précision, petit rappel : la section contact n'est pas à faire sous forme de pop-up. Elle est bien intégrée à la page. Considérez que "Contact us" est intégralement visible et lisible.

Bonus : mettre une google map dans la section Contact us.

### Section Footer
Faites en sorte que lorsqu’on clique sur le petit bouton rouge avec la flèche blanche, on monte jusqu’à l'entête du site, le petit bouton disparaît une fois que l'entête apparaît.

CONTRAINTE : créer ce bouton en pur JS avec createElement(), createTextNode() et compagnie(), l’afficher sur le DOM, le positionner puis le styler en CSS dans la feuille de style.

FAITES QUE LE SITE SOIT RESPONSIVE (Bootstrap + Media queries)


## B. La newsletter

Utiliser ce site https://putsmail.com/tests/new pour tester votre newsletter.
Vous pouvez utiliser les tables, ou du HTML5 (certains webmails acceptent du HTML5 mais mais mais attention avec le CSS)

Référence : [Voici une newsletter que j’ai reçu de la part de Yves Rocher](http://pictures.yvesrocher.com/NL/2017-06/06/be-fr/jun_6_be-fr_a2_online.html), s’inspirer à souhait et c’est essentiellement des tables.

Bonne chance et bon courage. (PS : on vous aime)

### REMARQUES :
Vous travaillez en groupe :
- Organisez-vous : utiliser un kanban (onglet [projects] dans GitHub).
- Si vous avez des remarques ou des questions, n'hésitez pas à utiliser l'onglet [Issues] de GitHub pour vous exprimer.
- Communiquez : rappelez-vous les bienfaits des réunions SCRUM.

### Cat Tax : Maru

![Maru](https://s-media-cache-ak0.pinimg.com/736x/01/db/73/01db734bfbebad88776671495bc09cf5.jpg)

### Rappel des équipes

- Guillaume Kreit & Jesse Fumba
- Nicolas de Liedekerke & Marie Cambie
- Thibault Gribaumont & Marco Bove
- Adrien d'Oreye & Merieme Lamri
- Jean-François Geerinckx & Cedric Fournier
- Nathan Houtain & Stephane Wilfort
- Marie Louise Ogdoc & Charlotte Tusset
- Antoni Dalle Nogare & Alexandre Infanti
- Ajay Shinde & Colombe Sechehaye
- Liam Carlier & Geraldine Winand
- Hakan Poyraz & Eric Lavachery
- Massimo Regaglia & Guillaume Deruwez
