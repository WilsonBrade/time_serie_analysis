# Time series analysis

Projet d'analyse de série temporelle appliqué à l'action Apple (AAPL).
Le cœur du travail se trouve dans le notebook [time_serie_analys.ipynb](time_serie_analys.ipynb), qui charge les données, visualise la série, teste la présence de tendance et de saisonnalité, puis applique un lissage de Holt-Winters.

## Objectif

L'objectif du projet est d'étudier le comportement temporel du cours de clôture de AAPL et de construire une première modélisation de type série temporelle.

Le notebook couvre notamment:

- le chargement et le nettoyage des données historiques,
- la visualisation de la série brute,
- la décomposition de la série en tendance, saisonnalité et résidu,
- une analyse de saisonnalité via moyennes mensuelles et test de Fisher,
- l'identification d'un schéma additif ou multiplicatif,
- un lissage exponentiel de Holt-Winters,
- l'évaluation du modèle avec MAE et RMSE.

## Structure du dépôt

- [time_serie_analys.ipynb](time_serie_analys.ipynb) : notebook principal d'analyse.
- [data/raw_AAPL.csv](data/raw_AAPL.csv) : jeu de données historique utilisé par le notebook.
- [requirements.txt](requirements.txt) : dépendances Python nécessaires.

## Prérequis

Utilise Python 3.10+ de préférence, avec les bibliothèques suivantes:

- pandas
- numpy
- matplotlib
- statsmodels
- yfinance
- scikit-learn

## Installation

Créer un environnement virtuel puis installer les dépendances:

```bash
python -m venv .venv
.venv\\Scripts\\activate
pip install -r requirements.txt
```

Si tu travailles déjà dans un environnement Python configuré, la simple installation des dépendances suffit.

## Utilisation

1. Ouvre [time_serie_analys.ipynb](time_serie_analys.ipynb) dans VS Code ou Jupyter.
2. Vérifie que le fichier [data/raw_AAPL.csv](data/raw_AAPL.csv) est bien présent.
3. Exécute les cellules dans l'ordre pour reproduire l'analyse.

Le notebook produit:

- des graphiques de la série de clôture,
- des décompositions additive et multiplicative,
- des indicateurs de tendance et de saisonnalité,
- un forecast Holt-Winters sur 12 mois,
- des métriques de performance.

## Données

Le fichier `data/raw_AAPL.csv` contient les observations historiques utilisées pour l'analyse. Le notebook lit ce fichier directement, donc il n'est pas nécessaire de télécharger les données à chaque exécution.

## Résultats attendus

L'analyse conclut que la série présente une tendance et une saisonnalité mensuelle significatives, avec un modèle additif retenu pour le lissage Holt-Winters.

## Remarques

- Le notebook est en français et mélange analyse visuelle, justification statistique et modélisation.
