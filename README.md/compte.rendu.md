# 📊 Compte rendu Machine Learning & Analyse Statistique

**Projet :** Analyse de l’impact de l’IA sur les emplois à l’horizon 2030
**Dataset :** *AI_Impact_on_Jobs_2030.csv*
**Auteur :** Douaa El Khayari
**Contexte académique :** Analyse de données & Machine Learning

---

## 1. Introduction

Ce projet vise à analyser l’impact potentiel de l’intelligence artificielle sur les emplois à l’horizon 2030 à partir d’un jeu de données structuré. L’objectif est double :

* Réaliser une **analyse statistique descriptive** afin de comprendre la structure et les caractéristiques des données.
* Mettre en place des **modèles de régression / classification** pour prédire et expliquer certains niveaux de compétences liés aux métiers.

---

## 2. Présentation du dataset

Le dataset contient **3000 observations** et **18 variables**, composées de :

* Variables numériques : indicateurs de compétences, scores, niveaux d’exposition à l’IA.
* Variables catégorielles : secteurs, types de métiers, classifications professionnelles.

La variable principale étudiée dans la modélisation est **Skill_10**, transformée en variable binaire afin de permettre une approche en classification.

---

## 3. Analyse statistique descriptive

### 3.1 Tableau des statistiques descriptives

Un tableau de statistiques descriptives a été généré pour l’ensemble des variables numériques du dataset. Ce tableau présente :

* La moyenne
* La médiane
* L’écart-type
* Les valeurs minimale et maximale

📊 **Tableau 1 – Statistiques descriptives des variables numériques**
(Ce tableau est issu de la fonction `describe()` de *pandas* et est affiché dans le notebook.)

Ces indicateurs permettent d’évaluer la dispersion des données, leur homogénéité et d’identifier d’éventuelles anomalies.

---

### 3.2 Graphiques de distribution

Des graphiques de distribution (histogrammes) ont été générés pour les principales variables numériques afin d’analyser leur forme (symétrie, concentration, dispersion).

📈 **Figure 1 – Histogrammes des variables de compétences**

L’analyse graphique montre que la majorité des variables présentent des distributions relativement équilibrées, ce qui est favorable à l’application de modèles statistiques et de Machine Learning.

---

### 3.2 Analyse de la distribution

Les distributions des variables numériques montrent une relative homogénéité des scores de compétences, avec quelques variations selon les dimensions analysées. Cette étape est essentielle pour justifier l’utilisation de modèles statistiques et de Machine Learning.

---

## 4. Matrice de corrélation

Une matrice de corrélation a été construite à partir des variables numériques afin d’identifier les relations linéaires entre les différentes compétences.

📊 **Tableau 2 – Matrice de corrélation (coefficients de Pearson)**

En complément, une visualisation graphique sous forme de heatmap a été réalisée.

📉 **Figure 2 – Heatmap de la matrice de corrélation**

### Interprétation :

* Certaines variables de compétences présentent une corrélation positive modérée à forte, indiquant des évolutions conjointes.
* Aucune corrélation extrême n’a été observée, ce qui limite le risque de multicolinéarité dans les modèles de régression.

La matrice de corrélation constitue un outil fondamental pour orienter la sélection des variables explicatives.

---

## 5. Modélisation et régressions

### 5.1 Prétraitement des données

Avant la modélisation, plusieurs étapes de prétraitement ont été appliquées :

* Imputation des valeurs manquantes (médiane / valeur la plus fréquente)
* Standardisation des variables numériques
* Encodage des variables catégorielles (One-Hot Encoding)
* Séparation des données en **jeu d’entraînement (80%)** et **jeu de test (20%)**

---

### 5.2 Algorithmes utilisés

Deux algorithmes de Machine Learning ont été implémentés :

* **Logistic Regression** : modèle linéaire utilisé comme référence pour la classification binaire.
* **Random Forest Classifier** : algorithme d’ensemble basé sur des arbres de décision, capable de capturer des relations non linéaires.

---

### 5.3 Résultats des modèles

Les performances des modèles ont été comparées à l’aide d’un tableau récapitulatif.

📊 **Tableau 3 – Comparaison des performances des modèles**

| Modèle              | Accuracy    |
| ------------------- | ----------- |
| Logistic Regression | Élevée      |
| Random Forest       | Très élevée |

Ces résultats montrent la supériorité du modèle Random Forest sur ce jeu de données.

---

## 6. Matrice de confusion

La matrice de confusion du meilleur modèle (Random Forest) a été représentée graphiquement afin d’évaluer la qualité des prédictions.

📉 **Figure 3 – Matrice de confusion (Random Forest)**

Cette visualisation met en évidence :

* Un nombre très élevé de prédictions correctes
* Un taux d’erreur extrêmement faible

Elle confirme ainsi la robustesse et la fiabilité du modèle sélectionné.

---

## 7. Conclusion

Ce projet a permis de :

* Comprendre la structure et les relations internes du dataset grâce à l’analyse statistique descriptive
* Identifier les liens entre les compétences via la matrice de corrélation
* Mettre en œuvre des modèles de Machine Learning performants

Le **Random Forest Classifier** s’est révélé être le modèle le plus adapté pour ce problème, offrant des résultats très satisfaisants.

---

## 8. Perspectives

Pour aller plus loin, plusieurs pistes peuvent être envisagées :

* Utiliser des modèles de régression avancés (XGBoost, Gradient Boosting)
* Effectuer une sélection automatique des variables
* Étudier l’importance des variables pour interpréter l’impact de l’IA sur les compétences

---

📌 *Ce dépôt GitHub contient le dataset, les notebooks de traitement, les modèles entraînés ainsi que ce compte rendu analytique.*
