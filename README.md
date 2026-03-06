# TP — Volumes & Persistance Docker

## Prérequis
- Docker installé et fonctionnel
- Connaissances de base : `docker run`, `docker rm`, `docker ps`

---


---

## Exercice 3 — La surprise du VOLUME

### 📋 Contexte
Vous devez construire une image qui prépare un dossier avec des fichiers, puis déclare ce dossier comme volume.

### 🎯 Objectif
Comprendre ce qu'il reste dans le dossier après avoir lancé le conteneur.

### 📝 Consignes

Créez un fichier `Dockerfile` avec les instructions suivantes, **dans cet ordre exact** :

1. Partez de l'image `alpine`
2. Créez le dossier `/data`
3. Ajoutez-y les fichiers `fichier1.txt` et `fichier2.txt`
4. Déclarez `/data` comme **volume**
5. Ajoutez ensuite les fichiers `fichier3.txt` et `fichier4.txt` dans le même dossier

Construisez l'image, lancez un conteneur, puis affichez le contenu de `/data`.

### ❓ Questions

1. Quels fichiers voyez-vous dans `/data` ?
2. Pourquoi `fichier3.txt` et `fichier4.txt` ne sont pas présents ?
3. Que se passe-t-il si vous lancez le conteneur **sans** monter de volume avec `-v` ?
4. Quel est l'intérêt de l'instruction `VOLUME` dans un Dockerfile ?