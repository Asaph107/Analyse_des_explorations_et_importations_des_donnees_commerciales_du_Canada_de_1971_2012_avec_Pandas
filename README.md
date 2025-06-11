# 📊 Représentation des importations et des exportations du Canada (1971 - 2012)

Ce projet vise à explorer les flux commerciaux du Canada sur une période de 40 ans, en s’appuyant sur les données publiques fournies par **Statistique Canada**. Il met en œuvre un pipeline complet de traitement de données (ETL), depuis le téléchargement jusqu’à la visualisation.

## 🧱 Technologies utilisées
- Python 3.12.7
- Pandas
- Matplotlib
- SQLAlchemy
- SQL Server
- requests, zipfile, io

## 🔄 Pipeline ETL

### 1. 🔎 **Recherche et acquisition**
- Téléchargement automatique du fichier ZIP contenant le CSV
- Lecture du fichier en mémoire (`io.BytesIO`)

### 2. 🛠️ **Transformation des données**
- Décompression du fichier
- Nettoyage des colonnes inutiles
- Conservation des colonnes :
  - `PÉRIODE DE RÉFÉRENCE`
  - `VALEUR`
  - `L'importation et l'exportation, groupes principaux de marchandises et marchés principaux`
  - `UNITÉ DE`
  - `Base`

### 3. 💾 **Chargement**
- Insertion des données dans une base SQL Server via SQLAlchemy et Pandas

## 📊 Visualisations
Les données nettoyées ont été utilisées pour générer des graphiques temporels permettant d’observer les tendances des importations et des exportations par groupe de produits et partenaires commerciaux.

## ✅ Résultats
- Création d’un jeu de données propre et filtré
- Représentation claire des variations dans le temps
- Renforcement des compétences ETL et visualisation en Python

## 📌 Objectif
Utiliser des données ouvertes et fiables pour tirer des informations économiques concrètes et reproductibles, dans le cadre d’un projet d’analyse exploratoire des données publiques canadiennes.
