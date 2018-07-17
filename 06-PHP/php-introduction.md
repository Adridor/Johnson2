# PHP

## Table des matières

- [Introduction](php-introduction.md)   ←
- [Variables](php-variables.md)
- [Conditions](php-conditions.md)
- Drill: [Exercices sur les Conditions](php-exercices-conditions.md)
- [Tableaux (array)](php-array.md)
- [Boucles](php-boucles.md)
- [Fonctions](php-fonctions.md)


## PHP : "Hypertext Preprocessor"
PHP est un logiciel qui tourne du côté **Backend**, càd. au niveau du _serveur web_. (Le **Frontend** désigne à contrario ce qui se passe du côté _Client_ càd. le _navigateur_).

PHP permet au Serveur Web de "**réfléchir avant de parler**".   
En informatique, "réfléchir" c'est calculer, càd, manipuler des informations et les retourner au Client (le navigateur) dans n'importe quel format (très souvent: du HTML, du XML, du JSON, voir du texte simple, du CSS, du javascript...).

## Pourquoi utiliser du php si cela retourne autre chose que du php ?

Parce que cela vous permet de créer des pages de manière **dynamique** plutôt que **statique**.

Par exemple, imagine que tu doives créer une page web permettant de dire "Bonjour!" à chacun des quelque 7 milliards d'habitants vivant actuellement sur la planète.
Cela signifie que tu dois créer 7 milliards de pages html telles que celle-ci, accessibles à une adresse url du style: http://citizens.net/humans/jose-garcia.html

```HTML
<html>
<head>...</head>
<body><h1>Bonjour José Garcia!</h1></body>
</html>
```
...Cela te prendrait des années, non? Et en plus, tu ne serais pas arrivé(e) à la millième page qu'il te faudrait déjà en effacer (les décès) et en ajouter (les naissances)... Pas terrible.

Et si tu ne créais qu'un seul fichier (un "script php") à qui l'on envoie le nom de l'humain via l'adresse url et qui "crée" l' html dynamiquement?

L'adresse url deviendrait, par exemple,  http://citizens.net/humans/index.php?name=jose-garcia


```PHP
<html>
<head>...</head>
<body><h1>Bonjour <?php echo $_GET['nom']; ?>!</h1></body>
</html>
```

Il suffirait alors que chacun reçoive son URL personnalisé et voilà! Un monde un peu plus doux, un peu plus accueillant!

## Mise en pratique

Essaye de deviner ce qu'est censée retourner cette requête :   
`https://github.com/becodeorg/BXLCentral/issues/2`

## Installation

### Serveur de développement / de staging / de production
Quand on développe, on ne travaille pas directement sur le serveur hébergeant le site ou l'application car la moindre faute de frappe pourrait provoquer une erreur et "casser" le site, incommodant des milliers de personnes. Pas bien...

Pour éviter cela, on travaille sur son propre ordinateur, c'est plus facile et cela permet de tester sans gêner personne. Cela permet aussi de travailler sans connexion internet (dans le train par exemple). C'est ce qu'on appelle un _environnement de développement local_  ou simplement un _serveur de développement_. Le serveur final est appelé lui un _serveur de production_. C'est lui que l'on rend accessible à tout le monde.
Il t'arrivera aussi de travailler avec un _environnement de staging_ présentant du code à faire valider avant sa mise en production.

### Installer un serveur de développement local

Un "stack de développement" désigne les logiciels nécessaires à une application web, côté serveur. Les stacks PHP les plus courants sont LAMP et LEMP : Linux/Windows/MacOS + Apache (ou nginx qui se prononce "engine X", d'où le E) + MySQL + PHP.  

Si tu es sur Windows, tu peux donc chercher "WAMP" et sur mac "MAMP". 


#### 1. Installation:

1. Voir les instructions pour [installer un environnement LAMP](https://github.com/becodeorg/BeCode/wiki/Installer-LAMP-sur-Ubuntu). Si tu préfères, tu peux aussi utiliser Docker pour télécharger et installer un environnement de développement tout fait qui tournera en machine virtuelle sur ta machine. [Voici un Docker LEMP parfait](https://github.com/becodeorg/docker-compose-lemp) pour ton parcours à BeCode. 

Quel que soit le chemin que tu choisis, tu dois avoir un serveur qui serve l'adresse http://localhost:PORT/ pour pouvoir continuer.

2. Crée un dossier "test"
3. à l'intérieur, crée un fichier index.php et mets-y ceci: 

```php
<?php
echo "Hello!";
?>
```

#### 2. A présent, ouvre ton navigateur à l'adresse http://localhost/test

Tu devrais voir le sympathique message "Hello!" que tu t'es adressé. Tu viens de créer ton premier script en PHP. Fais-toi un gros câlin, tu l'as bien mérité.

![Giphy](http://media1.giphy.com/media/35gNg6o2HYjSg/giphy.gif)

### Exercices

- Prends quelques minutes et joue avec ton fichier index.php. Mets-y une image de chats.
- Crée une deuxième page dans le même dossier (`cats.php`) et ajoute un peu de contenu et surtout un lien sur chacune des deux pages permettant de passer de l'une à l'autre.
- Fait? Bravo, tu viens de créer un site internet chat-oyant !
Voici un chaton pour fêter cela.

![Giphy](http://media0.giphy.com/media/nsMPhWK6bfxHq/giphy.gif)


Rendez-vous à la prochaine leçon: [Variables et Conditions](./php-variables.md).


