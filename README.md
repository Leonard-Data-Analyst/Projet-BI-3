
# Projet-BI-3: Analyse-Risque-Credit-Bancaire

## 1. Contexte du Projet

Ce projet porte sur l'analyse du risque de credit bancaire, menée auprès d'une institution. Il concerne les données clients d'une banque. 
Le type de crédit concerné est celui d’un crédit revolving. L'objectif est d'identifier les dentances du secteur, le niveau de risqe de remboursement, 
le défaut de remboursement.

## 2. Objectifs

- **Analyser les comportements de paiement des clients** 
- **Étudier l'impact des variables sociodémographiques** sur le **les paiements**
- **Étudier l'impact des variables métiers ** sur le **les paiements**.
- **Créer des visualisations interactives** avec **Power BI**.

## 3. Étapes de la conception du Dashboard

### a. Préparation des Données

- **Renommage des variables** pour une meilleure lisibilité.
- **Suppression des colonnes inutiles** (par exemple, celles avec 100% de valeurs manquantes).
- **Catégorisation des variables** sociodémographiques et métiers pour simplifier l’analyse :
  - **Âge** : Jeunes, Adultes, Moyenne âge, Seniors, Plus âgés.
  - **Sexe** : Homme, Femme.
  - **Niveau d’éducation** : École supérieure, Université, Collège, Autres formations.
  - **Statut marital** : Marié, Célibataire, Autre.
- **Transformation des variables** (par exemple, catégorisation des paiements et des factures) pour mieux comprendre les comportements financiers.

### b. Création des KPI et Visualisations

#### KPI 1 : Taux de défaut global
- **Variables utilisées** : `default.payment.next.month` (variable cible)
- **Visualisation** : Carte KPI affichant le **taux de défaut global**.

#### KPI 2 : Montant total des crédits accordés
- **Variables utilisées** : `LIMIT_BAL`
- **Visualisation** : Carte KPI montrant le **total du crédit accordé**.

#### KPI 3 : Taux d’utilisation moyen du crédit
- **Variables utilisées** : `BILL_AMT6` / `LIMIT_BAL`
- **Visualisation** : Carte KPI montrant le **taux d’utilisation moyen du crédit**.

#### KPI 4 : Montant total en défaut
- **Variables utilisées** : `LIMIT_BAL` des clients en défaut.
- **Visualisation** : Carte KPI montrant le **montant total en défaut**.

#### Graphiques :
- **Barres empilées** pour la répartition des défauts de paiement par **sexe**, **âge**, **niveau d’éducation**, **statut marital**.
- **Graphiques en secteurs** pour analyser la **répartition des défauts de paiement** selon **la catégorie de paiement** et la **catégorie de facture** (dettes, surplus, à jour).

## 4. Résultats et Insights Clés

- **Analyse des comportements de paiement** : Les clients ayant un **taux d'utilisation élevé du crédit** et des **retards de paiement fréquents** ont une probabilité plus élevée de faire défaut.
- **Impact des variables sociodémographiques** : Les **jeunes adultes** ont tendance à faire plus de défauts que les **adultes plus âgés**.
- **Comportement de remboursement** : Les clients ayant un **surplus de paiement** sont moins susceptibles de faire défaut, tandis que ceux avec des **dettes** ont un risque plus élevé.

## 5. Structure du Projet

```
Projet3.pbix/        # Fichier Power BI
│
├── data/                         # Données sources (si disponible)
│
├── screenshots/                  # Captures d'écran du tableau de bord
│
└── README.md                     # Documentation du projet
```

## 6. Perspectives

- **Amélioration des visualisations** et **ajout d'indicateurs avancés**.
- **Comparaison** avec les années précédentes pour détecter les **tendances évolutives** des paiements et des défauts
- **Exploration de nouvelles sources de données** pour enrichir l'analyse

---
