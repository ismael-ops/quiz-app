# 🗡️ SNK Quiz Application

> Application Web Full-Stack de quiz dédiée à l’univers de **Shingeki no Kyojin (Attack on Titan)**.  
> Réalisée dans le cadre du projet **E4FI – Développement Web Full Stack 2023-2024**.

---

## 📚 Table des matières

- [📖 Introduction](#-introduction)
- [🎯 Contexte du projet](#-contexte-du-projet)
- [⚙️ Fonctionnalités](#️-fonctionnalités)
- [🛠️ Technologies utilisées](#️-technologies-utilisées)
- [🏗️ Architecture du projet](#️-architecture-du-projet)
- [🗄️ Schéma de la base de données](#️-schéma-de-la-base-de-données)
- [🚀 Installation et lancement](#-installation-et-lancement)
- [📌 Améliorations possibles](#-améliorations-possibles)
- [👨‍💻 Auteur](#-auteur)

---

## 📖 Introduction

La **SNK Quiz Application** est une application web interactive permettant aux utilisateurs de tester leurs connaissances sur l’univers de *Shingeki no Kyojin*.

L’application propose :

- Des questions à choix multiples  
- Un calcul automatique du score  
- Un enregistrement des participants  
- Une comparaison des performances  

L’objectif est de proposer une expérience ludique, fluide et interactive tout en respectant une architecture full-stack propre et scalable.

---

## 🎯 Contexte du projet

Ce projet a été réalisé dans le cadre du module :

> **E4FI – Projet Quiz Web Full-Stack**

L’objectif pédagogique était de :

- Concevoir une application web complète (Front + Back)
- Implémenter une API REST
- Concevoir une base de données relationnelle
- Appliquer une architecture claire et modulaire
- Respecter un cahier des charges précis

---

## ⚙️ Fonctionnalités

### 👤 Gestion des participants

- Création d’un participant
- Enregistrement du score
- Historique des parties

### ❓ Gestion du quiz

- Affichage dynamique des questions
- Questions à choix multiples
- Gestion des réponses correctes
- Ordre des questions configurable

### 📊 Résultats

- Calcul automatique du score
- Enregistrement en base de données
- Classement des participants

### 🔌 API REST

- CRUD des questions
- CRUD des réponses
- Gestion des participants
- Routes testées via Postman

---

## 🛠️ Technologies utilisées

### 🎨 Front-end

- Vue.js
- HTML5
- CSS3

### 🧠 Back-end

- Python
- Flask
- API RESTful

### 🗄️ Base de données

- SQLite

### 🧪 Outils

- Postman (tests API)
- Git / GitHub
- VS Code

---

## 🏗️ Architecture du projet

L’application suit une architecture en trois couches :

Frontend (Vue.js)  
↓  
Backend API (Flask)  
↓  
Base de données (SQLite)

### Séparation des responsabilités :

- Frontend → Gestion interface utilisateur
- Backend → Logique métier + API REST
- Database → Stockage des données

---

## 🗄️ Schéma de la base de données

### 📌 Table `Questions`

| Champ | Type | Description |
|-------|------|------------|
| id | INTEGER (PK) | Identifiant unique |
| text | TEXT | Texte de la question |
| title | TEXT | Titre de la question |
| image | BLOB | Image associée |
| pos | INTEGER | Ordre d’affichage |

---

### 📌 Table `Answers`

| Champ | Type | Description |
|-------|------|------------|
| id | INTEGER (PK) | Identifiant unique |
| question_id | INTEGER (FK) | Référence à la question |
| text | TEXT | Texte de la réponse |
| isCorrect | BOOLEAN | Indique si la réponse est correcte |
| pos | INTEGER | Ordre d’affichage |

Relation :  
Une question possède plusieurs réponses.  
Une réponse appartient à une seule question.

---

### 📌 Table `Participants`

| Champ | Type | Description |
|-------|------|------------|
| id | INTEGER (PK) | Identifiant unique |
| name | TEXT | Nom du participant |
| score | INTEGER | Score obtenu |
| createdAt | DATE | Date de participation |

---

## 🚀 Installation et lancement


```bash
## 1️⃣ Cloner le projet
git clone https://github.com/ismael-ops/quiz-app.git
cd quiz-app

### 2️⃣ Installation du backend
cd quiz-api
pip install -r requirements.txt
python app.py


### 3️⃣ Installation du frontend
cd quiz-ui
npm install
npm run serve

## 📌 Améliorations possibles

- Mode chronométré
- Leaderboard global dynamique
- Mode multijoueur
- Déploiement Cloud (AWS / GCP)
- Conteneurisation Docker

## 👨‍💻 Auteur

Ismaïla Sylla
Ingénieur en informatique
