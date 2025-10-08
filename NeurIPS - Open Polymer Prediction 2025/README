# NeurIPS - Open Polymer Prediction 2025

## Note
En cours de developpement

## Description

Ce projet vise à développer un pipeline de machine learning pour la prédiction automatisée des propriétés physico-chimiques de polymères à partir de leur structure moléculaire (SMILES). Ce travail s'inscrit dans le cadre du challenge NeurIPS 2025 - Open Polymer Prediction.

## Fonctionnalités principales

- Extraction des descripteurs moléculaires et empreintes (fingerprints) à l'aide de RDKit
- Prétraitement et normalisation des données
- Construction de modèles de régression pour la prédiction de propriétés
- Optimisation des hyperparamètres via GridSearchCV
- Évaluation à l'aide d'une métrique personnalisée (Weighted Mean Absolute Error - wMAE)
- Génération de prédictions et préparation d'un fichier de soumission pour la compétition

## Propriétés prédites

Le pipeline est conçu pour prédire les propriétés suivantes des polymères :
- Tg (Température de transition vitreuse)
- FFV (Fractional Free Volume)
- Tc (Température de cristallisation)
- Density (Densité)
- Rg (Rayon de giration)

## Données

- **train.csv** : Fichier d'entraînement contenant les SMILES et les propriétés cibles
- **test.csv** : Fichier de test contenant les SMILES des polymères à prédire

## Pipeline

1. **Chargement des données**  
   - Lecture des fichiers CSV contenant les SMILES et propriétés
   - Construction de jeux de données spécialisés pour chaque propriété

2. **Ingénierie des caractéristiques**  
   - Extraction des descripteurs physico-chimiques (RDKit)
   - Calcul des Morgan Fingerprints (empreintes circulaires)
   - Prétraitement des chaînes SMILES pour générer les features

3. **Normalisation et split**  
   - Standardisation des features
   - Séparation entraînement/validation pour chaque propriété

4. **Modélisation et optimisation**  
   - Régression avec différents modèles (RandomForest, LightGBM, Ridge, SVR, KNN, MLP)
   - Optimisation des hyperparamètres via GridSearchCV
   - Sélection du meilleur modèle pour chaque propriété selon le wMAE

5. **Évaluation**  
   - Calcul du score wMAE global à partir des prédictions Out-of-Fold
   - Affichage des performances pour chaque propriété

6. **Génération des prédictions sur le test set**  
   - Extraction et standardisation des features du jeu de test
   - Prédiction des propriétés avec les modèles optimisés
   - Génération d’un fichier de soumission pour la compétition

## Technologies utilisées

- Python
- Pandas, NumPy, tqdm
- RDKit (chimie computationnelle)
- scikit-learn (modèles et optimisation)
- LightGBM (gradient boosting)
- Matplotlib, Seaborn (visualisation)

## Utilisation

1. Placez les fichiers `train.csv` et `test.csv` dans le dossier `datasets/`.
2. Lancez le notebook ou le script principal.
3. Les résultats et le fichier de soumission seront générés automatiquement à la fin de l’exécution.

## Structure du dossier

```
NeurIPS - Open Polymer Prediction 2025/
├── datasets/
│   ├── train.csv
│   └── test.csv
├── pipeline_1.ipynb
└── README.md
```

## Contact

Pour toute question ou suggestion, veuillez ouvrir une issue sur le repository principal ou contacter les auteurs du projet.

---

Ce projet est développé pour le challenge NeurIPS 2025 et représente une base solide pour la prédiction de propriétés de polymères à partir de leur structure moléculaire.
