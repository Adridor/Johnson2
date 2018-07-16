# PHP


Ce parcours sur l'apprentissage du PHP est _made in BeCode_ mais libre à toi d'aller sur OpenClassroom, CodeaCaMachin, voire trucMuche... 

## Configurer son PC pour pouvoir jouer avec du PHP
- [Configurer un environnement de développement local (LAMP) sur Ubuntu](https://github.com/becodeorg/BeCode/wiki/Installer-LAMP-sur-Ubuntu) - si le lien ne fonctionne pas, [cliquez ici](https://github.com/becodeorg/BeCode/wiki) puis cliquez sur [Pages] puis choisissez le bon post.
- [Installer LAMP sur Linux](https://doc.ubuntu-fr.org/lamp)
- [Et y'a le tuto de Thomas aussi](https://github.com/Rivanos/projet-client-connectbx/tree/master/Le%20site#installer-linux-apache-mysql-php-lamp)
- [Installer PHPMyAdmin](https://doc.ubuntu-fr.org/phpmyadmin)


## Introduction
- [Introduction au PHP](https://docs.google.com/presentation/d/133tChXIMvfqRgaf9329WOymsGTXLzIVXyIZpW0Z1mFI/edit?usp=sharing)
- [Comprendre en quoi consiste la programmation !](https://www.video2brain.com/fr/tuto/en-quoi-consiste-la-programmation) (3 min vidéo)

Quel que soit le chemin choisi, ce qui est important est que tu atteignes ces...
## Objectifs d'apprentissage
### Temps 1 : parcours 06-PHP

- Comprendre l'utilité du PHP (donc pour quels types de problèmes il est une technologie adéquate)
- Pouvoir résoudre des problèmes en utilisant la syntaxe de PHP pour mettre en place 

	- des opérateurs,
	- des variables,
	- des tableaux,
	- des structures de contrôle (conditions, switch & boucles),
	- des fonctions,
	- des objets;

- Pouvoir traiter des données envoyées via un formulaire en POST, en passant systématiquement par ces étapes :

	1. **sanitisation** 
	2. **validation**
	3. **exécution**
	4. **feedback**

- Faire du *DRY* (Don't Repeat Yourself) via les `include()` 
- Mettre en place un script servant de *Router*
- Traiter l'upload de fichiers
- Séparer le calcul de l'affichage (le plus de PHP possible avant tout HTML)
- Pouvoir faire un script qui lit et écrit dans un fichier texte
- Savoir comment ne pas réinventer la roue grâce à l'Open Source
- Ecrire une fonction `mail()` qui utilise un serveur SMTP externe.

### Temps 2 : parcours 07 - SQL/DB
- Se familiariser avec la syntaxe SQL
- Récupérer les données stockées dans une base de données
- Savoir penser et construire une base de données relationnelle
- Organiser un CRUD
- Réaliser un REST API

### Temps 3 : parcours 08 - MVC
- L'architecture MVC
- Prendre en main un framework MVC
- Créer une application "produit" permettant à un utilisateur de se créer un compte, d'opérer des mises à jour et de se déconnecter

### Temps 4 : parcours 09 - OOP
- La programmation Orientée Objet (OOP)
- Gérer ses dépendances via Composer

## Table des matières

### Temps 1 : Parcours permettant de maîtriser la syntaxe PHP
(Attention à l'épilepsie, *lots of gifs ahead!* )

1. [Introduction](php-introduction.md)
2. [Variables](php-variables.md)
3. [Conditions](php-conditions.md)
4. Quizz: [PHP / intro + variables](../../Quizz/PHP/php-base-1.md)
5. Drill: [Exercices sur les Conditions](php-exercices-conditions.md)
6. [Tableaux (array)](php-array.md)
7. [Boucles](php-boucles.md)
8. [Fonctions](php-fonctions.md)

### Temps 1 : Exercices pratiques
Une fois ces étapes du parcours effectuées, utilisons ces nouveaux acquis dans des exercices concrets, inspirés de situations réelles.

<!--
## Exercices complémentaires

1. Formulaire de contact de la société Hackers Poulette
1. QCM
1. Questionnaire en ligne: Nomophobie ou pas?
1. Pinterest
1. Todolist + json
1. Todolist + SQL-->
