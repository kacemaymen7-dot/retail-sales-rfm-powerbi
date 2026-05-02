# Analyse des ventes retail et segmentation client RFM avec Power BI

## Présentation du projet

Ce projet analyse les ventes retail et le comportement client à l’aide de Power BI.

L’objectif est de construire un dashboard interactif permettant de suivre la performance commerciale, d’identifier les clients à forte valeur et de prioriser les actions marketing grâce à la segmentation RFM.

RFM signifie :

- Recency : date du dernier achat ;
- Frequency : fréquence d’achat ;
- Monetary : montant total dépensé.

## Objectif business

L’objectif principal est d’aider une entreprise retail à :

- comprendre la performance des ventes et du profit ;
- identifier les segments clients les plus importants ;
- détecter les clients à risque ;
- prioriser les campagnes marketing ;
- prendre des décisions basées sur les données.

## Dataset

Le projet utilise le dataset Superstore Sales de Kaggle.

Colonnes principales utilisées :

- Order ID
- Order Date
- Customer ID
- Customer Name
- Segment
- Region
- Category
- Sub-Category
- Sales
- Quantity
- Discount
- Profit

## Outils utilisés

- Power BI Desktop
- Power Query
- DAX
- Excel
- GitHub

## Étapes du projet

1. Import du fichier CSV dans Power BI.
2. Nettoyage des données avec Power Query.
3. Correction des types de données.
4. Création des mesures DAX.
5. Création d’une table client RFM.
6. Calcul de la récence, fréquence et valeur monétaire.
7. Création des scores R, F et M.
8. Segmentation des clients.
9. Construction du dashboard Power BI.
10. Analyse des insights et recommandations business.

## Mesures DAX principales

```DAX
Total Sales = SUM(Orders[Sales])

Total Profit = SUM(Orders[Profit])

Total Orders = DISTINCTCOUNT(Orders[Order ID])

Total Customers = DISTINCTCOUNT(Orders[Customer ID])

Total Quantity = SUM(Orders[Quantity])

Profit Margin = DIVIDE([Total Profit], [Total Sales])

Average Order Value = DIVIDE([Total Sales], [Total Orders])
