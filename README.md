# Analyse du coût de la vie mondial

Analyse exploratoire et segmentation du coût de la vie dans plusieurs centaines de villes à partir de 55 indicateurs économiques exprimés en dollars : loyers, salaires, alimentation, transports, services.

L'objectif est de mesurer les écarts de niveau de vie entre villes, d'identifier des profils de villes homogènes et de construire des indicateurs de pouvoir d'achat.

## Méthodologie

| Étape | Contenu |
|---|---|
| Exploration | Dimensions, types de variables, couverture géographique |
| Valeurs manquantes | Analyse du mécanisme (MCAR, MAR, MNAR) |
| Nettoyage | Règles métier, valeurs aberrantes remplacées par NaN |
| Imputation | Comparaison médiane globale, médiane par pays et MICE |
| Statistiques descriptives | Asymétrie, aplatissement, coefficient de variation |
| Transformation | `log(1 + x)` pour réduire l'asymétrie des distributions |
| Réduction de dimension | Analyse en composantes principales (ACP) |
| Segmentation | K-Means, nombre de groupes choisi par la méthode du coude et le score de silhouette |

## Résultats

La première composante principale explique 52,4 % de la variance : un seul facteur, assimilable au niveau de vie global, structure l'essentiel des indicateurs.

Le K-Means fait ressortir quatre profils de villes :

| Groupe | Profil | Salaire net médian | Loyer médian (centre-ville) |
|---|---|---|---|
| 0 | Villes à revenus très élevés | 3 690 $ | 1 600 $ |
| 1 | Villes intermédiaires | 1 454 $ | 519 $ |
| 2 | Villes émergentes | 1 832 $ | 718 $ |
| 3 | Villes à revenus modestes | 599 $ | 307 $ |

Les écarts extrêmes sont marqués : à Cuba, le loyer représente environ 11 fois le salaire médian, et le pouvoir d'achat est 96 fois plus élevé au Qatar.

## Exécution

Le notebook est conçu pour Google Colab : il utilise `google.colab.files` pour charger le jeu de données.

1. Ouvrir [le notebook dans Colab](https://colab.research.google.com/github/eyazouch/global-cost-of-living-analysis/blob/main/Projet_Analyse_de_Donn%C3%A9es.ipynb).
2. Télécharger le jeu de données [Global Cost of Living](https://www.kaggle.com/datasets/mvieira101/global-cost-of-living/data) (Miguel Vieira, Kaggle). Il n'est pas inclus dans ce dépôt.
3. Charger le fichier CSV lorsque le notebook le demande, puis exécuter les cellules dans l'ordre.

## Outils

Python, Pandas, NumPy, Matplotlib, Seaborn, Plotly, Scikit-learn (IterativeImputer, PCA, KMeans), Missingno.

## Contexte

Projet académique réalisé par Eya Zouch en 2025.
