---
layout: default
title: Ligne de commande Linux
---

# À faire

- Notez toutes vos manipulations 
- Documentez chaque commande utilisés dans un document texte que vous déposerez sur e-lyco au format pdf 
- Aucune impression écran n'est permise dans le document
- format du document 
        __Nom_prenom_TP_Linux_commande.pdf__


# Objectif 

Se familiariser avec l'environement Linux et ses commandes. 


## Introduction

* [Introduction à Linux](lessons/linux)
    - man, cd, ls, cat
* [La ligne de commande sous Linux](lessons/ligne-commande-linux)
* [Correspondance Linux/windows](http://raphaello.univ-fcomte.fr/Linux/TP3.htm)
# Travail attendu 
  
- Votre premier fichier bash ou pas, ce fichier doit :            
    - créer un repertoire 'info' 
    - créer un fichier 'contenu' dans le repertoire info contenant la liste des fichier de votre répertoire personnel 
    - afficher le contenu de votre fichier bash 
    - afficher le contenu de la page manuel de motd
- Personalisation de votre environement 
    - Ajoutez l'alias ll="ls -l" à votre fichier .bash_profile
            Testez votre alias 
    
## Activités

* [La ligne de commande sous Linux](activities/ligne-commande-linux)
    
    - Faîtes les quatre exercices
    - Créer un fichier __Nom_prenom_exo_linux.pdf__ contenant votre progression.

## Accès à la documentation

- help: Aide en terminal
- help commande: Aide en terminal sur une commande particulière
- man commande: Aide en terminal sur une commande particulière
- commande -?: Aide en terminal sur une commande particulière
- commande --help: Aide en terminal sur une commande particulière

## Structure du système

- Répertoires du système:
    - /etc: Fichiers de configuration
    - /bin, /sbin, /usr, ...: Fichiers de commande
    - /dev: Devices
    - /mnt: Répertoire destiné à contenir les répertoires utilisisés pour les montages
    - /tmp: Répertoire pour les fichiers temporaires
    - /home: Répertoires home des utilisateurs
    - /root: Répertoire home de l'utilisateur root
- Variables d'environnement
    - set: Liste des variables d'environnement
    - Configuration des variables d'environnement dans le fichier /etc/bash.bashrc pour le shell bash (shell par défaut de root)
    - D'autres éléments de configuration dans le fichier /etc/profile
    - Variable PATH
    - Ajouter TEST=ESSAI
    - echo $TEST
    - Fichiers .profile et .bashrc dans le répertoire home de chaque utilisateur pour qu'il puisse gérer ses propres options de configuration
- Lancement d'une application
    - appliName: Lancement d'une application trouvée dans l'un des répertoires listés dans le PATH
    - ./appliName: Lancement d'une application trouvée dans le répertoire implicite
        - Ajouter . (répertoire implicite) dans le PATH si trop pénible
        - Attention au risque d'homonymie
        - Ajout de "." au PATH de tous les utilisateurs (sauf root) dans le fichier /etc/profile
        - Ajout de "." au PATH de root par ajout de la ligne "export PATH=.:$PATH" dans le fichier /root/.bashrc
    - sudo appliName: Lancement d'une application endossée par un utilisateur (autre utilisateur)
        - Fichier /etc/sudoers pour configurer les applications lançables par un utilisateur au moyen de sudo ainsi que le compte endossé pour le lancement de chacune de ces applications
        - Délégation
        - Complexe?!
- Gestion des processus
    - ps: Liste instantanée des processus
    - ps -lfA: Liste instantanée complète des processus
    - top: Liste rafraîchie complète des processus
    - kill: Terminaison d'un processus
    - shutdown: Extinction du sytème d'exploitation
- who: Liste instantanée des utilisateurs
    - Ctrl-Alt-F1 à Ctrl-Alt-F6 pour switcher vers des - - -  sessions supplémentaires en mode texte
    - Ctrl-Alt-F7 pour switcher vers la session en interface utilisateur graphique
- Mémoire virtuelle
    - Partition spécifique (swap) configurée par défaut par le programme d'installation
    - fdisk -l: Visualisation de toutes les partitions
    - Modification des caractéristiques du swap non décrite ici
- Installation/désinstallation d'une application
    - Faire l'installation "à la main"
    - Fichiers tar: Archives séquentielles sans compression
    - tar: Commande de gestion des archives tar
    - Fichiers gz: Archives séquentielles avec compression
    - gzip et gunzip: Commande de compactage et de décomptage des archives gz
    - Fichiers gz2: Archives tarées puis gzipées
- aptitude
    - Interface utilisateur texte minimale
- apt-get
    - Travail en ligne de commande
    - apt-get install paquet: Installation d'une application
    - apt-get remove paquet: Désinstallation d'une application
    - Installation de g++
        - apt-get install g++
    - Installation de Google Chrome
        - Ajout de la ligne "deb http://dl.google.com/linux/chrome/deb/ stable main" comme source de données supplémentaire pour Google Chrome dans le fichier /etc/apt/sources.list
        - apt-get update: Mise à jour de la base de données de paquets (warning lié à l'abscence d'un certificat numérique)
        - apt-get install google-chrome-stable: Installation de Google Chrome
    - apt-cache search keyWord: Recherche d'un mot-clé dans la base de données des paquets pour déterminer le nom précis du paquet correspondant au logiciel à installer
- Autres distributions que Debian/Ubuntu: Autres méthodes d'installation

[Source:](http://raphaello.univ-fcomte.fr/Linux/TP2.htm)

## La gestion des droits d'accès

* [Droits d'accès](https://doc.ubuntu-fr.org/permissions)

## Pour aller plus loin 
[Installer les services linux sous windows 10](http://www.laurentbloch.org/MySpip3/Installer-les-services-Linux-de-Windows-10-WSL)