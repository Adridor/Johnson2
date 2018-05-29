# Le SSH

## Qu'est ce que le SSH

Le SSH ou Secure Shell est un protocole de communication mis au point en 1995 par le Finlandais Tatu Ylönen, permettant à un client (un utilisateur ou bien même une machine) d'ouvrir une session interactive sur une machine distante (serveur)afin d'envoyer des commandes ou des fichiers de manière sécurisée :

 - Les données circulant entre le client et le serveur sont chiffrées, ce qui garantit leur confidentialité (personne d'autre que le serveur ou le client ne peut lire les informations transitant sur le réseau). Il n'est donc pas possible [d'écouter le réseau](https://www.commentcamarche.com/contents/68-analyseurs-reseau-sniffers) à l'aide d'un [analyseur de trames](https://www.commentcamarche.com/contents/68-analyseurs-reseau-sniffers).
 - Le client et le serveur s'authentifient mutuellement afin d'assurer que les deux machines qui communiquent sont bien celles que chacune des parties croit être. Il n'est donc plus possible pour un pirate d'usurper l'identité du client ou du serveur ([spoofing](https://www.commentcamarche.com/contents/71-usurpation-d-adresse-ip-mystification-spoofing)).
 
## Pourquoi en a t-on besoin (en tant que web dev)

Dans le métier de développeur web on sera amené à devoir developper des sites en local (serveur sur notre machine physique)  et puis les transfèrer sur notre machine de production (un serveur en ligne, quelque part dans le monde, qui n’est qu’en soit un autre ordianteur). 

## Concrètement comment ça marche

Pour l’exemple nous allons utiliser une Raspberry. Celle-ci déjà pré-configurée par votre formateur avec un [serveur Apache](https://fr.wikipedia.org/wiki/Apache_HTTP_Server) et connexion SSH activée.

Pour se connecter en SSH à une autre machine on aura besoin de 3 choses
– La commande ssh
– Le nom d’utilisateur avec lequel on veut se connecter
– Le nom de la machine en réseau ou son ip

Notre commande complète ressemblera à ceci:

**ssh pi@10.20.0.34**

**‘ssh’ ‘user’ @ ‘machineIP/machineName’**

Utiliser votre terminal et introduisez la commande suivante:
**ssh pi@10.20.1.62**

Un mot de passe vous sera demandé. Introduissez: **Whitep@per127.0**

**ATTENTION: L’ADRESSE IP ET/OU L’UTILISATEUR ET/OU MOT DE PASSE NE SERONT SANS DOUTE PAS LES MÊME. DEMANDEZ À VOTRE FORMATEUR LES INFOS.**

Une autre manière de trouver l’adresse IP de la machine est d’utiliser dans votre terminal la commande:

**arp -a**

Celle-ci affichera les adresses IP des différentes machines connectés au même réseau que vous.
Il existe aussi une application nomée “Fing” qui vous permet plus facilement de trouver les ip sur votre smartphone.

## Maintenant que je suis conencté, je fais quoi

Maintenant qu’on est connecté on peut tout faire. Du moins ce que l’utilisateur au quel on est connecté à l’autorisation de faire !

Dirigez vous dans le dossier **/var/www/html** en utilisant la commande cd:

**cd /var/www/html**

Créez un repertoire portant votre nom. 
ATTENTION pas de spaces ! Utilisez les “_ “ (underscore) si besoin !
Voici la comamnde:
**mkdir mon_nom_prenom**

## Revenons à notre machine physique

Créez un fichier **index.html** sur votre bureau.

Modifiez votre fichier html et ajoutez "Hello I'm votre_nom". Enregistrez et fermez.

Ouvrez un nouveau terminal et accedez au dossier de votre bureau:

Tapez la commade **cd** et puis appuyez su la touche enter. 

Ceci vous palce dans votre dossier **home** ou **~** qui sera indiqué sur le terminal.

Il sera maintenant plus facile d’accèder à votre dossier desktop ou bureau en fr.

Introduisez la commande **ls** pour lister les dossier et fichier disponibles dans le dossier où vous êtes situé. Vous devriez voir votre dossier bureau (Desktop).

Introduisez la commande **cd Desktop** puis enter pour accèder à votre bureau. (Attention des fois les noms de dossiers sont différents référez vous à vos noms de dossier exemple Bureau à la place de Desktop dans le cas ou votre pc est en français).

Introduisez la commande **ls**, vous devriez voir le fichier html que vous venez de créer et peut-être d'autres fichier/dossier sur votre bureau.

## Allez on transfère sur le serveur distant (notre raspberry)

Maintenant que nous sommes dans le terminal et situé dans le dossier bureau on va pouvoir transfèrer notre fichier html sur le serveur. Souvenez-vous, on a créé un dossier portant votre nom. On va transfèrer dans ce dossier.

Pour cela on va utiliser la commade **scp**.

Toujours dans votre terminal et dans le dossier bureau, tapez la commande:

**scp ./index.html pi@10.20.1.62:/var/www/html/mon_nom_prenom/**

**ATTENTION “mon_nom_prenom” correspond à votre nom de dossier créé précédenment dans le serveur.**

Explications sur la commande.

**scp** pour secure copy 

**./index.html** c’est la localisation du fichier que je souhaite tranfèrer
**pi** mon login de connexion au serveur 
**10.20.1.62** ip de mon serveur distant
**:/var/www/html/mon_nom_prenom/** repertoire où je veux copier sur mon serveur distant

SI TOUT VA BIEN VOTRE FICHIER HTML SERA VISIBLE À l’ADRESSE:

**“http://10.20.1.62/mon_nom_prenom/index.html”**

Tapez-la dans votre navigateur.

Bravo vous avez utilisez le SHH pour copier un fichier !
