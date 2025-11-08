# data_challenge_M2MIA

Objectif général
----------------
Ce projet s’inscrit dans le cadre d’un data challenge portant sur deux problématiques distinctes :
1. Un problème de classification multiclasse.
2. Un problème de régression.

L’objectif est de concevoir, évaluer et comparer plusieurs modèles d’apprentissage supervisé sur des jeux de données tabulaires.
Chaque tâche est accompagnée d’une analyse exploratoire approfondie et d’une justification méthodologique complète.

------------------------------------------------------
Organisation des notebooks
------------------------------------------------------

1. analyse_exploratoire_classification_data_challenge.ipynb
   --------------------------------------------------
   - Étude du jeu de données de classification (environ 60 000 observations).
   - Analyse des distributions des variables quantitatives et qualitatives.
   - Étude des corrélations et réalisation d’une Analyse en Composantes Principales (ACP).
   - Visualisations : histogrammes, boxplots, matrice de corrélation, cercle des corrélations, éboulis des valeurs propres.
   - Identification des variables les plus discriminantes pour la tâche de classification.

2. analyse_exploratoire_regression_data_challenge.ipynb
   --------------------------------------------------
   - Exploration statistique du jeu de données de régression.
   - Analyse univariée et bivariée des covariables.
   - Étude des relations linéaires et non linéaires avec la variable cible.
   - ACP et visualisations pour détecter la multicolinéarité et les variables influentes.
   - Préparation des données pour la phase de modélisation.

3. modeles_predictifs_classification_data_challenge.ipynb
   --------------------------------------------------
   - Implémentation et comparaison de trois modèles :
       * Régression logistique multinomiale
       * Forêt aléatoire (Random Forest)
       * SVM à noyau RBF (extension One-vs-One)
   - Optimisation des hyperparamètres via validation croisée (GridSearchCV, RandomizedSearchCV).
   - Évaluation selon le F1-score pondéré (métrique du challenge Kaggle).
   - Visualisation des matrices de confusion et rapports de classification.
   - Sélection du modèle final et export du fichier de soumission Kaggle.

4. modeles_predictifs_regression_data_challenge.ipynb
   --------------------------------------------------
   - Implémentation et comparaison de trois modèles de régression :
       * Régression linéaire multiple
       * Forêt aléatoire régressive
       * XGBoost regressor
   - Évaluation selon le R^2 .
   - Validation croisée et analyse des erreurs résiduelles.
   - Visualisation des performances comparées.
   - Choix du modèle final et export du fichier de prédictions.

------------------------------------------------------
Résultats synthétiques
------------------------------------------------------
- En classification : la Forêt Aléatoire s’est révélée être le meilleur compromis entre performance (F1-score élevé), robustesse et capacité de généralisation.
- En régression : le modèle XGBoost a offert le R^2 le plus grand, surpassant les modèles linéaires et à base d’arbres standards.

------------------------------------------------------
Auteur
------------------------------------------------------
Projet réalisé par : [LARIBI Yanis, KTAIB Achraf]
Encadrant : [COUDRAY Olivier]
Date : [année 2025-2026]
