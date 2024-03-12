---
geometry: "left=1cm, right=1cm, top=1cm, bottom=1cm"
---

# Cahier technique  
le 27/02/2024

**Projet Totally Spies** (MyEasyline) avec Elia WU, Inaam VERTENEUILLE et Maïlys POULAIN

[Redirection](README.md) vers le cahier des charges

## Contexte

&emsp; L'agence de location de petits trains, Totally-Trains, souhaite pour leur processus de location un outil interne nommé Chuchu. 
&emsp; Elle aura différentes fonctionnalités décrites ci-dessous.

## Spécifications techniques 

#### Ressources de développement

* Langage utilisé : Java JDK v.21
* Framework de présentation : JavaFX
* IDE utilisé : IntelliJ IDEA 2023.3.1
* Données : BDD SQL accessible sur Internet
* Gestion du code : via Git v.2.43.0 sur un projet dédié partagé sur GitLab.com

#### Ressources nécessaires après développement

* Lien de téléchargement

## MODELE RELATIONNEL 

#### RELATIONS

Utilisateurs (id : int(7), pseudo : varchar(50), mdp : varchar(255), role : ROLE )
* Clé primaire : id (A_I)
* Clé étrangère : none

Trains (id : int(7), themeTrain : THEMETRAIN, ville : VILLE, id_chauffeur : int(7), nom : varchar(255))
* Clé primaire : id (A_I)
* Clé étrangère : id_chauffeur -> Utilisateurs.id

Clients (id : int(7), nom : varchar(255), prenom : varchar(255))
* Clé primaire : id (A_I)
* Clé étrangère : none

Reservations (id : int(7), dateReservation : date, dateEvenement : date, commentaire : varchar(255), id_train : int(7), id_client : int(7))
* Clé primaire : id (A_I)
* Clés étrangères : 
    * id_train -> Trains.id
    * id_client -> Clients.id

#### ENUMS

##### ROLE 
- ADMINISTRATEUR
- SUPPORT
- CHAUFFEUR

##### THEMETRAIN
- NOEL
- HALLOWEEN
- PAQUES
- TOTALLY-SPIES
- DISNEY

##### VILLE
- PARIS
- NICE
- LYON
- BORDEAUX
- BREST
- GRENOBLE
- LILLE
- MONTPELLIER
- NANTES
- RENNES 
- ROUEN
- STRASBOURG
- TOULOUSE

## SQL 

[Redirection](chuchu.sql) vers le fichier SQL

## Organisation du code

![Organisation_code](img/Organisation_code.png)

Le code se divise principalement en 3 parties:

    * src.main.java.fr.esiee.chuchu.chuchu contient les fichiers permettant de lancer l'application
    * src.main.java.fr.esiee.chuchu.controller contient les fichiers qui traitent les événements de l'interface utilisateur, met à jour le modèle en fonction des actions de l'utilisateur et met à jour la vue en fonction des changements dans le modèle.
    * src.main.java.ressources.fr.esiee.chuchu contient les fichiers de l'interface utilisateurs (aussi appelé vue), c'est globalement la partie visuel de l'application