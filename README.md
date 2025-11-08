# data_challenge_M2MIA

Objectif
---------
Ce notebook met en œuvre différentes approches d’apprentissage supervisé pour résoudre un problème de classification multiclasse à partir d’un jeu de données tabulaire. 
L’objectif est de prédire la variable cible 'reservation_status' ∈ {0,1,2} à partir d’un ensemble mixte de variables numériques et catégorielles.

Organisation du notebook
------------------------
1. Chargement et préparation des données :
   - Importation du jeu d’entraînement et du jeu de test.
   - Séparation des covariables (X_train, X_test) et de la cible (Y_train).
   - Identification des colonnes numériques et catégorielles.

2. Prétraitement :
   - Utilisation d’un ColumnTransformer pour appliquer :
       * StandardScaler sur les variables numériques (si nécessaire).
       * OneHotEncoder sur les variables catégorielles.
   - Intégration du prétraitement dans un Pipeline unique par modèle.

3. Modèles testés :
   a) Régression logistique multinomiale :
      - Modèle linéaire de référence.
      - Hyperparamètre principal : coefficient de régularisation C.
      - Optimisation par validation croisée (GridSearchCV).

   b) Forêt aléatoire (Random Forest) :
      - Modèle non linéaire basé sur un ensemble d’arbres de décision.
      - Recherche d’hyperparamètres par RandomizedSearchCV avec validation croisée.
      - Analyse des importances de Gini pour interpréter les résultats.

   c) SVM à noyau RBF (One-vs-One) :
      - Modèle à marges maximales adapté à la classification multiclasse.
      - Optimisation des hyperparamètres C et gamma via RandomizedSearchCV.
      - Évaluation par validation croisée et matrice de confusion OOF.

4. Évaluation des modèles :
   - Calcul du F1-score pondéré, de la précision et du rappel.
   - Validation croisée (k=5) pour évaluer la performance généralisée.
   - Visualisation des matrices de confusion et des rapports de classification.

5. Soumission finale :
   - Génération des prédictions sur la base de test (X_test).
   - Export des résultats au format CSV pour soumission sur Kaggle.
