# TP GitLab CI - Pipeline CI/CD Spring Boot

## Description

Ce projet met en place un pipeline CI/CD avec **GitLab CI** pour une application Spring Boot. Le projet utilisé est **ExamJavaM1GL** — une application de gestion des Classes et Secteurs académiques développée avec Spring Boot et PostgreSQL.

Le pipeline automatise le build du projet et prépare le déploiement d'une image Docker sur Docker Hub.

---

## Prérequis

- Un compte [GitLab](https://gitlab.com)
- Git

---

## Contenu du fichier .gitlab-ci.yml

Le pipeline est composé de 2 stages :

### stage 1 : build-test
- Utilise l'image Maven `3.8.3-openjdk-17`
- Compile le projet avec `mvn clean package -DskipTests`
- Génère le JAR `thymeleaf-springboot.jar` comme artefact
- Met en cache le dossier `.m2/repository` pour accélérer les builds suivants

### stage 2 : deploy
- Utilise l'image `docker:latest`
- Build l'image Docker du projet
- Push l'image sur Docker Hub
- Déclenchement **manuel** (`when: manual`)

---

## Captures d'écran

### Projet sur GitLab
<!-- capture repo GitLab -->

### Pipeline réussi - stage build-test
<!-- capture pipeline vert -->

---

## Auteur

**Ndeye Mbaye** — M1 Génie Logiciel
