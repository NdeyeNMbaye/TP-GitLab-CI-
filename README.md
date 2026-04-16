## TP GitLab CI - Pipeline CI/CD sur projet Spring Boot

Ce projet consiste à mettre en place une chaîne d’intégration continue et de déploiement continu (CI/CD) avec GitLab CI sur un projet Spring Boot existant.

Le but est d’automatiser les étapes de build et de déploiement via Docker en ajoutant un pipeline CI/CD au projet.

### Objectif du TP

L’objectif de ce TP est de :

Ajouter un pipeline CI/CD à un projet Spring Boot existant
Automatiser la compilation du projet avec Maven
Exécuter les tests unitaires
Construire une image Docker
Publier l’image sur Docker Hub

### Prérequis
Projet Spring Boot existant
Compte GitLab
Git installé
Java 17 + Maven
Docker

### Workflow du pipeline
Push du code sur GitLab
Exécution automatique du build
Génération du .jar
Construction de l’image Docker
Push sur Docker Hub

Repository GitLab

<img width="1917" height="957" alt="image" src="https://github.com/user-attachments/assets/ae3a7b52-cc17-4bb1-87c8-78758853879b" />

Pipeline réussi

<img width="1919" height="969" alt="image" src="https://github.com/user-attachments/assets/7698458c-e135-468c-96ac-f7d30dcd5329" />


<img width="1905" height="961" alt="image" src="https://github.com/user-attachments/assets/8ef01cb9-a8f8-485e-a95b-524c60143d16" />

Docker Image Build / Push

<img width="1891" height="852" alt="image" src="https://github.com/user-attachments/assets/bce4d526-86b8-4cea-8b6d-48f0df838050" />

