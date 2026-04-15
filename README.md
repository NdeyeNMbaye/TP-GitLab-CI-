## TP GitLab CI - Pipeline CI/CD Spring Boot

### Description

Ce projet met en place un pipeline CI/CD avec GitLab CI pour une application Spring Boot.
Le projet utilisé est ExamJavaM1GL, une application de gestion des classes et secteurs académiques développée avec Spring Boot et PostgreSQL.

Le pipeline automatise les étapes de build et de déploiement via Docker.

### Objectif du projet

L’objectif de ce TP est de :

Mettre en place une intégration continue avec GitLab CI
Automatiser la compilation et les tests d’un projet Spring Boot
Générer un artefact exécutable (.jar)
Préparer et automatiser le déploiement via Docker
Comprendre le fonctionnement d’un pipeline CI/CD

### Prérequis
Compte GitLab
Git installé localement
Maven et Java 17
Docker (pour la partie déploiement)

### Pipeline GitLab CI/CD

Le pipeline est structuré en deux stages principaux.

#### Stage 1 : build-test

Ce stage utilise l’image Maven avec Java 17.

Il permet de :

Compiler le projet
Générer le fichier .jar
Exécuter les tests (selon configuration)

Commande utilisée : mvn clean package -DskipTests

Optimisations :

Mise en cache du répertoire .m2/repository pour accélérer les builds
### Stage 2 : deploy

Ce stage utilise Docker.

Il permet de :

Construire une image Docker de l’application
Pousser l’image vers Docker Hub
Déclenchement manuel du déploiement (when: manual)

Cette étape permet de contrôler le passage en production.
Workflow du pipeline
Push du code sur GitLab
Exécution automatique du stage build-test
Génération du fichier .jar
Validation du build
Déclenchement manuel du stage deploy
Construction et publication de l’image Docker

### Captures d’écran

#### Repository GitLab

<img width="1917" height="952" alt="image" src="https://github.com/user-attachments/assets/a75b4ce1-9887-4f39-98b6-6792ce6a364c" />

#### Pipeline réussi (build-test)

<img width="1909" height="950" alt="image" src="https://github.com/user-attachments/assets/cd742290-5d5c-4c39-933b-7241025e46b2" />

