#  Analyse de la consommation énergétique résidentielle (2006–2010)

##  Contexte
Ce projet a été réalisé dans le cadre du **projet PACTE**, en travail d’équipe.  
Il porte sur l’analyse de **données réelles de consommation électrique résidentielle** collectées sur une période de près de 4 ans dans un foyer situé à Sceaux (France).

L’objectif principal est de comprendre les **habitudes énergétiques**, identifier des **tendances de consommation** et proposer des **pistes d’optimisation énergétique**.

---

##  Objectifs du projet
- Nettoyer et préparer un dataset réel de grande taille
- Analyser les comportements de consommation électrique
- Identifier les tendances journalières, mensuelles et saisonnières
- Détecter les pics de consommation et les anomalies
- Étudier la répartition de la consommation par usage
- Proposer des recommandations simples et exploitables

---

##  Données utilisées
- **Dataset** : Individual Household Electric Power Consumption (UCI Machine Learning Repository)
- **Période** : Décembre 2006 – Novembre 2010
- **Fréquence** : 1 mesure par minute
- **Nombre de lignes** : 2 075 259
- **Nombre de variables** : 9

 Le dataset étant volumineux, il n’est pas directement inclus dans le dépôt.  
Lien vers les données : https://archive.ics.uci.edu/ml/datasets/individual+household+electric+power+consumption

---

##  Nettoyage et préparation des données
- Analyse des valeurs manquantes (~1,25 % des données)
- Identification de blocs de valeurs manquantes :
  - blocs courts (≤10 minutes)
  - blocs longs (>10 minutes)
- Interpolation des blocs courts
- Suppression des blocs longs (périodes d’absence ou de panne)
- Fusion des variables **Date** et **Time** en une variable **Datetime**
- Création de variables dérivées pour faciliter l’analyse

---

## 🔧 Variables principales
- `Global_active_power` : consommation totale du foyer
- `Sub_metering_1` : cuisine
- `Sub_metering_2` : buanderie
- `Sub_metering_3` : chauffe-eau
- `Autre_consommation` : consommation non mesurée par les sous-compteurs

---

## 📈 Analyses réalisées
- Consommation horaire moyenne
- Consommation mensuelle et saisonnière
- Comparaison entre les années
- Répartition de la consommation par zone
- Identification des pics de consommation
- Analyse des comportements énergétiques

---

## 🔍 Résultats clés
- Pics de consommation le matin (7h–8h) et le soir (19h–21h)
- Consommation plus élevée en hiver, plus faible en été
- Le chauffe-eau et les usages de confort sont dominants
- Une part importante de la consommation provient des usages non mesurés

---

##  Recommandations
- Optimiser la programmation des équipements de confort
- Réduire les consommations inutiles (appareils en veille)
- Améliorer l’efficacité énergétique des équipements
- Mettre en place un suivi régulier de la consommation

---

##  Technologies utilisées
- Python
- Pandas
- NumPy
- Matplotlib
- Jupyter Notebook



##  Perspectives
- Intégration de données externes (température)
- Modélisation prédictive de la consommation
- Mise en place d’un système de suivi intelligent
