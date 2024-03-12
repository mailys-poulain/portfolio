---
geometry: "left=1cm, right=1cm, top=1cm, bottom=1cm"
---

# Cahier des charges   
le 18/01/2024

**Projet Totally Spies** (MyEasyline) avec Elia WU, Inaam VERTENEUILLE et Maïlys POULAIN

## Contexte - Demande

&emsp; L'agence de location de petits trains Totally-Trains souhaite pouvoir simplifier le processus de location avec un nouvel outil interne nommé Chuchu.

&emsp; Elle attend différentes fonctionnalités.

### Fonctionnalités

**INTERNES**

Admin
* Ajouter, modifier, supprimer un petit train
* Ajouter, modifier, supprimer un chauffeur

Admin + Support
* Récupérer les info d'un petit train
* Récupérer les info d'un chauffeurs
* Récupérer la liste des petits trains (avec filtre : dispo, pas dispo ou tous)
* Récupérer la liste des chauffeurs (fonctionnels ou pas)
* Affecter/Désaffecter un chauffeur à un petit train
* Pouvoir modifier la disponibilite du service d'un petit train
* Verifier la disponibilite d'un chauffeur
* Voir, gérer, modifier, supprimer une réservation
* Voir une liste de réservation

Chauffeur
* Consulter ses jours de travail + informations
* Dire s'il est dispo ou pas

Processus de réservation réalisé par le support
1. Choisir un lieu (parmi une liste)
2. Choisir une date 
3. Voir la liste des petits trains disponibles et leurs infos (parmi ceux disponibles)
4. Réserver avec id du client 

## Contraintes 

* Langage utilisé : Java
* Framework de présentation : JavaFX
* Données : BDD SQL accessible sur Internet
* Gestion du code : via Git sur un projet dédié partagé sur GitLab.com

## Usecases 

![Usecases](img/Usecases_screen.png)

## Diagramme de classes 

![Diagramme de classes](img/diagramme_de_classe.png)

## Modèle relationnel

[Fichier Markdown](img/modele_relationnel.md) vers le modèle relationnel

## Maquette

Lien Figma vers la maquette entière :
https://www.figma.com/file/IjRka4BD7kWjrbMOYFnN5I/CHUCHU?type=design&node-id=0%3A1&mode=design&t=pGxu88t2cFq1NkZ3-1

* Zoom sur les pages de la maquette concernant le chauffeur et la page login (qui est la même pour tous): 

![Maquette Chauffeur + Login](img/Maquette_chauffeur.png)


* Zoom sur les pages de la maquette concernant le support (sans page login qui est la même pour tous): 

![Maquette Support](img/Maquettes_support.png)

* Zoom sur les pages de la maquette concernant l'administrateur (sans page login qui est la même pour tous): 

![Maquette Administrateur](img/Maquette_administrateur.png)

## Diagramme de Gantt 

- Rose : Elia Wu
- Vert : Inaam Verteneuille
- Bleu : Maïlys Poulain

![Diagramme de Gantt](img/gantt.png)

## Plus 

* Trello : https://trello.com/invite/b/IHQXu634/ATTIf6cb89b9f5579200ca1ba38473af9b1905108ABB/totally-train 

