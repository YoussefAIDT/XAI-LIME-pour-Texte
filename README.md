# 🔍 Explicabilité de l'IA (XAI) : Analyse de Sentiment avec LIME

![Python](https://img.shields.io/badge/Python-3.8%2B-blue?style=for-the-badge&logo=python&logoColor=white)
![Hugging Face](https://img.shields.io/badge/Transformers-DistilBERT-yellow?style=for-the-badge&logo=huggingface&logoColor=white)
![LIME](https://img.shields.io/badge/XAI-LIME-green?style=for-the-badge)
![License](https://img.shields.io/badge/License-Academic-lightgrey?style=for-the-badge)

> **Mini-projet académique sur l'interprétabilité des modèles de Deep Learning (NLP).**

---

## 👥 Auteurs
Ce projet a été réalisé par :
* **ES-SAAIDI Youssef**
* **ZEMMAHI Zakariae**
* *Date : Décembre 2025*

---

## 📝 Description du Projet

L'objectif de ce projet est d'ouvrir la "boîte noire" des modèles de traitement du langage naturel (NLP). Nous utilisons la méthode **LIME (Local Interpretable Model-agnostic Explanations)** pour comprendre pourquoi un modèle de Deep Learning classe une critique de film comme **Positive** ou **Négative**.

Nous avons implémenté un pipeline complet qui :
1.  Utilise un modèle **DistilBERT** pré-entraîné (`distilbert-base-uncased-finetuned-sst-2-english`).
2.  Effectue des prédictions sur le dataset de critiques de films **IMDb**.
3.  Génère des explications visuelles montrant l'impact de chaque mot sur la décision finale.

---

## 🧠 Concepts Clés

| Concept | Description |
| :--- | :--- |
| **Black Box** | Modèles complexes (Réseaux de neurones) dont le processus de décision interne est opaque. |
| **LIME** | Technique qui approxime le modèle complexe par un modèle linéaire simple localement pour expliquer une prédiction unique. |
| **Perturbation** | Génération de variantes de la phrase en masquant des mots pour tester la sensibilité du modèle. |

---

## 🛠️ Stack Technique

* **Langage :** Python 3
* **Modèle :** Hugging Face Transformers
* **Bibliothèques Principales :**
    * `lime` : Algorithme d'explicabilité.
    * `transformers` : Chargement du modèle BERT.
    * `datasets` : Chargement des données IMDb.
    * `torch` : Backend Deep Learning.
    * `matplotlib` / `numpy` : Visualisation et calculs matriciels.

---

## 🚀 Installation et Utilisation

### 1. Cloner le projet
```bash
git clone [[https://github.com/VOTRE_NOM_UTILISATEUR/NOM_DU_REPO.git](https://github.com/YoussefAIDT/XAI-LIME-pour-Texte)]
cd XAI-LIME-pour-Texte
````

### 2\. Installer les dépendances

Il est recommandé d'utiliser un environnement virtuel. Installez les paquets nécessaires avec :

```bash
pip install -q transformers datasets lime torch scikit-learn matplotlib
```

### 3\. Exécuter le Notebook

Le cœur du projet se trouve dans le fichier Jupyter Notebook. Lancez-le via :

```bash
jupyter notebook mini_projet_lime_texte.ipynb
```

*Note : Ce projet est également optimisé pour s'exécuter directement sur Google Colab.*

-----

## 📊 Visualisation des Résultats

Le projet produit des visualisations intuitives pour expliquer les prédictions.

### Exemple d'analyse

**Phrase d'entrée :** *"The movie was good but the ending was boring"*

**Interprétation LIME :**

  * 🟩 **Mots Verts (Positifs) :** `good` (Score: +0.32)
  * 🟥 **Mots Rouges (Négatifs) :** `boring` (Score: -0.45)

Cela confirme que le modèle détecte correctement les adjectifs porteurs de sentiment.

-----

## 🔮 Limitations et Perspectives

  * **Instabilité :** Les explications peuvent varier légèrement entre deux exécutions dues à l'échantillonnage aléatoire de LIME.
  * **Performance :** Le processus de perturbation nécessite plusieurs secondes par phrase.
  * **Piste future :** Comparer les résultats avec la méthode **SHAP** (Shapley Additive Explanations) pour valider la robustesse.

-----

## 📜 Licence

Ce projet est réalisé dans un cadre académique (Master/Ingénierie) et est ouvert à toute utilisation pédagogique.

```
