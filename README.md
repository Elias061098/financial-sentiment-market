# Sentiment Financier vs Marchés — Prédiction à J+1

Analyse de données réelles de sentiment de presse financière (2020-2024)
croisées avec les prix de marché SPY, QQQ, VIX.

## Ce que j'ai fait

- Chargement et fusion de données réelles Kaggle (1 585 jours de marché)
- Exploration : évolution du sentiment vs prix SPY, identification des crises
- Modèle XGBoost de prédiction de la direction du marché à J+1
- Évaluation : 83,2% de précision sur 315 exemples de test

## Stack

Python (pandas, numpy, scikit-learn, xgboost, matplotlib, seaborn) · Kaggle API

## Ce que j'ai trouvé — et pourquoi ça compte

Un trader regarde les news chaque matin de façon subjective et réagit après le mouvement.
Ce modèle anticipe la direction du marché à J+1 avec 83,2% de précision
sur 1 572 jours de données réelles — sans data leakage.

Ce que l'analyse révèle :
le VIX (indice de volatilité) est la variable la plus prédictive du mouvement de marché.
Le momentum 5 jours donne un signal fort sur la tendance court terme.
Mars 2020 (Covid) et 2022 (inflation) sont clairement identifiés
comme les périodes les plus négatives dans les données de sentiment.

Ce type de modèle est utilisé dans les salles de marché de BNP, SG
et les hedge funds pour filtrer le bruit médiatique
et détecter les signaux de retournement avant qu'ils se produisent.

## Lancer le projet

```bash
pip install kagglehub pandas numpy scikit-learn xgboost matplotlib seaborn
```
