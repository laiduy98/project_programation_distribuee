---
# pandoc report_prog_dist.md -o pdf/report_prog_dist.pdf --from markdown --template eisvogel.tex --listings --pdf-engine=xelatex --toc --number-sections

papersize: a4
# lang: vi-VN
# geometry:
#     - top=30mm
#     - left=20mm
#     - right=20mm
#     - heightrounded
documentclass: article
title: Rapport Projet du module Programmation distribuée
author: LAI Khang Duy - Lylia DJALI
date: 29-01-2022
titlepage: true
toc-own-page: true
titlepage-logo: assets/images/uparis.png
header-includes: 
      - |
        ``` {=latex}
        \let\originAlParaGraph\paragraph
        \renewcommand{\paragraph}[1]{\originAlParaGraph{#1} \hfill}
        ```
...

# Bonus work Qwiklabs
Please find the link here 

- [LAI KHANG DUY](https://www.qwiklabs.com/public_profiles/b3802779-0893-4f19-a16a-f7e5309c3219)

- [LYLIA DJALI](https://www.qwiklabs.com/public_profiles/d8f6c6b9-ecc2-44ae-8bda-78e65fc5874b)

# Ressource
Cliquez ci-dessous pour visualiser le code source de notre projet cliq. 

[**CLICK HERE**](https://github.com/laiduy98/project_programation_distribuee)

# Présentation du projet
L'objectif de ce projet était de montrer le concepet d'utilisation de plusieures technologies pour une programmation distribuée. A travers ce projet, on a pu construire un full web serveur avec 2 backends , 1 frontend et une base de données en utilisant les technologies étudiées dans le cours 

chaque service tourne dans un docker container avec docker compose qui définit et établit la communication entre chaque service

Le front end récupére des données depuis 2 backends avec 2 taches indépéndantes. 

![Show weather module](assets/images/show_weather_module.png)


Notre projet consiste à réaliser une application web tout en utilisant les technologies acquises lors du cours Programmation distribuée.

Et pour cela nous avons créé une application qui affiche la température pour n’importe quelle ville au monde ainsi qu’un enregistrement des températures précédentes récupéré depuis la base de données.


![Show record module](assets/images/show_record_module.png)

# Introduction des technologies utilisées 

## Django
Django est un framework web Python de haut niveau qui encourage le développement rapide et une conception propre et pragmatique.

## React.JS
Une bibliothèque JavaScript pour la création d'interfaces utilisateurs


## PostgreSQL
PostgreSQL est une base de données objet-relationnelle puissante et open source.


# Architecture de l’application
Pour expliquer le fonctionnement de notre application web, nous avons schématisé l’architecture logicielle de notre application comme on peut le voir sur la figure ci-dessous:

![Architecture de l’application](assets/images/program_architechture.png)


Notre application web est composé de :

- Un front end ( qui nous sert de navigateur) codé en REACT JS ,
- Deux back end : un qui sert à stocker et à extraire les données depuis notre base donnée codé en python en utilisant DJANGO , le deuxième qui sert à récupérer la température d’une autre API codé en python en utilisant DJANGO 
- Base de donnée POSTGRESQL

# Technologies de programmation distribuée utilisées dans ce projet:

## Micro-services 
Concrètement, les microservices sont une méthode de développement logiciel permettant de concevoir une application comme un ensemble de services modulaires. Chaque module répond à un objectif métier spécifique et communique avec les autres modules.

Dans notre projet, on a utilisé deux backend d'ou la notion microservices

## Docker
Les conteneurs fonctionnent un peu comme les VM, mais de manière beaucoup plus spécifique et granulaire. Ils isolent une seule application et ses dépendances - toutes les bibliothèques logicielles externes dont l'application a besoin pour fonctionner - à la fois du système d'exploitation sous-jacent et des autres conteneurs.
	
Dans notre application chaque application tourne et contenue dans un docker container,
Ce qui permet une utilisation plus efficace des ressources du système, des cycles de livraison de logiciels plus rapides, mais surtout très efficace dans architecture micro-service telle que la nôtre.

## Docker compose
Compose est un outil permettant de définir et d'exécuter des applications Docker multi-conteneurs. Avec Compose, on utilise un fichier YAML pour configurer les services de votre application. Ensuite, avec une seule commande, on crée et démarre tous les services à partir de notre configuration. 

## Kubernetes
minikube est un outil qui nous permet d'exécuter Kubernetes localement. minikube exécute un cluster Kubernetes à un seul nœud sur notre ordinateur.
Dans notre cas , comme on a utilisé minikube , tous nos conteneurs sont orchestrés par un  seul node.


# Conclusion
Ce projet nous a initié aux notions Docker ainsi que Kubernetes d’ou Docker aide à "créer" des conteneurs, et Kubernetes permet de les "gérer" au moment de l'exécution. Utiliser Docker pour emballer et expédier l'application et utiliser Kubernetes pour déployer et mettre à l'échelle l’application.
Utilisés ensemble, Docker et Kubernetes servent de facilitateurs de la transformation numérique et d'outils pour une architecture cloud moderne.
