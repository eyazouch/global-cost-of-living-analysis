# 🌍 Analyse du Coût de la Vie Mondial
> *Comprendre les disparités économiques mondiales à travers les données*

**Réalisé par Eya ZOUCH**

---

## 📋 Description

Ce projet propose une analyse approfondie du coût de la vie dans des centaines de villes à travers le monde. À partir d'un dataset de 55 indicateurs économiques en USD, il explore les inégalités mondiales, identifie des profils de villes cohérents et construit des indicateurs originaux de pouvoir d'achat.

---

## ⚠️ Important — Google Colab uniquement

Le notebook est conçu pour fonctionner **exclusivement sur Google Colab**.

Il ne fonctionnera pas en local car il utilise :
- `from google.colab import files` pour l'upload du dataset
- Des dépendances pré-installées sur l'environnement Colab

**Pour l'exécuter :**

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/)

1. Ouvrir le notebook dans Google Colab
2. Télécharger le dataset depuis [Kaggle](https://www.kaggle.com/datasets/mvieira101/global-cost-of-living/data)
3. Uploader le fichier CSV quand demandé
4. Exécuter les cellules dans l'ordre

---

## 🔬 Méthodologie

```
Chargement → EDA → Prétraitement → Analyse Statistique → ACP → Clustering
```

| Étape | Détail |
|---|---|
| **Exploration initiale** | Dimensions, types, couverture géographique |
| **Valeurs manquantes** | Classification MCAR / MAR / MNAR |
| **Nettoyage** | Règles métier, remplacement par NaN |
| **Imputation** | Comparaison médiane globale vs médiane pays vs **MICE** |
| **Analyse statistique** | Skewness, Kurtosis, Coefficient de variation |
| **Log-transformation** | `log(1+x)` pour réduire l'asymétrie |
| **ACP** | PC1 = 52.4% de variance — niveau de vie global |
| **K-Means** | k=4 validé par méthode du coude + Silhouette |

---

## 📊 Résultats clés

- **PC1 capture 52.4%** de la variance → un seul facteur latent structure tout
- **4 profils de villes** identifiés :

| Cluster | Profil | Salaire médian | Loyer centre |
|---|---|---|---|
| 0 | Très riches | 3 690 $ | 1 600 $ |
| 1 | Intermédiaires | 1 454 $ | 519 $ |
| 2 | Émergentes | 1 832 $ | 718 $ |
| 3 | Modestes | 599 $ | 307 $ |

- **Cuba** : ratio loyer/salaire = **1 100%**
- **Qatar vs Cuba** : facteur **×96** de pouvoir d'achat

---

## 🛠️ Stack technique

| Outil | Usage |
|---|---|
| Python | Analyse, prétraitement, modélisation |
| Pandas / NumPy | Manipulation des données |
| Matplotlib / Seaborn / Plotly | Visualisations |
| Scikit-learn | MICE, ACP, K-Means |
| Missingno | Analyse des valeurs manquantes |

---

## 📦 Dataset

**Source :** [Kaggle — Global Cost of Living](https://www.kaggle.com/datasets/mvieira101/global-cost-of-living/data)

**Auteur :** Miguel Vieira

> ⚠️ Le dataset n'est pas inclus dans ce repo. Téléchargez-le directement depuis Kaggle avant d'exécuter le notebook.

---

## 📄 Licence

Ce projet est à des fins académiques uniquement.

---

*Eya ZOUCH — 2025*# 🌍 Analyse du Coût de la Vie Mondial
> *Comprendre les disparités économiques mondiales à travers les données*

**Réalisé par Eya ZOUCH**

---

## 📋 Description

Ce projet propose une analyse approfondie du coût de la vie dans des centaines de villes à travers le monde. À partir d'un dataset de 55 indicateurs économiques en USD, il explore les inégalités mondiales, identifie des profils de villes cohérents et construit des indicateurs originaux de pouvoir d'achat.

---

## ⚠️ Important — Google Colab uniquement

Le notebook est conçu pour fonctionner **exclusivement sur Google Colab**.

Il ne fonctionnera pas en local car il utilise :
- `from google.colab import files` pour l'upload du dataset
- Des dépendances pré-installées sur l'environnement Colab

**Pour l'exécuter :**

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/)

1. Ouvrir le notebook dans Google Colab
2. Télécharger le dataset depuis [Kaggle](https://www.kaggle.com/datasets/mvieira101/global-cost-of-living/data)
3. Uploader le fichier CSV quand demandé
4. Exécuter les cellules dans l'ordre

---

## 🔬 Méthodologie

```
Chargement → EDA → Prétraitement → Analyse Statistique → ACP → Clustering
```

| Étape | Détail |
|---|---|
| **Exploration initiale** | Dimensions, types, couverture géographique |
| **Valeurs manquantes** | Classification MCAR / MAR / MNAR |
| **Nettoyage** | Règles métier, remplacement par NaN |
| **Imputation** | Comparaison médiane globale vs médiane pays vs **MICE** |
| **Analyse statistique** | Skewness, Kurtosis, Coefficient de variation |
| **Log-transformation** | `log(1+x)` pour réduire l'asymétrie |
| **ACP** | PC1 = 52.4% de variance — niveau de vie global |
| **K-Means** | k=4 validé par méthode du coude + Silhouette |

---

## 📊 Résultats clés

- **PC1 capture 52.4%** de la variance → un seul facteur latent structure tout
- **4 profils de villes** identifiés :

| Cluster | Profil | Salaire médian | Loyer centre |
|---|---|---|---|
| 0 | Très riches | 3 690 $ | 1 600 $ |
| 1 | Intermédiaires | 1 454 $ | 519 $ |
| 2 | Émergentes | 1 832 $ | 718 $ |
| 3 | Modestes | 599 $ | 307 $ |

- **Cuba** : ratio loyer/salaire = **1 100%**
- **Qatar vs Cuba** : facteur **×96** de pouvoir d'achat

---

## 🛠️ Stack technique

| Outil | Usage |
|---|---|
| Python | Analyse, prétraitement, modélisation |
| Pandas / NumPy | Manipulation des données |
| Matplotlib / Seaborn / Plotly | Visualisations |
| Scikit-learn | MICE, ACP, K-Means |
| Missingno | Analyse des valeurs manquantes |

---

## 📦 Dataset

**Source :** [Kaggle — Global Cost of Living](https://www.kaggle.com/datasets/mvieira101/global-cost-of-living/data)

**Auteur :** Miguel Vieira

> ⚠️ Le dataset n'est pas inclus dans ce repo. Téléchargez-le directement depuis Kaggle avant d'exécuter le notebook.

---

## 📄 Licence

Ce projet est à des fins académiques uniquement.

---

*Eya ZOUCH — 2025*
