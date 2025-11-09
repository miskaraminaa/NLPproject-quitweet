# Qui Tweet ? Trump ou Trudeau ?  
**Classifieur NLP d’attribution d’auteur sur tweets**  
[![Python](https://img.shields.io/badge/Python-3.10-blue)](https://www.python.org/)  
[![HuggingFace](https://img.shields.io/badge/🤗%20HuggingFace-Transformers-yellow)](https://huggingface.co/)  
[![Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/drive/1ABC123...)  
[![License](https://img.shields.io/badge/License-MIT-green)](LICENSE)

---

## Description du projet

Développement d’un **classifieur binaire** capable de déterminer si un tweet a été écrit par **Donald Trump** ou **Justin Trudeau**, en se basant uniquement sur le **style linguistique**.

- **Scraping** en temps réel via l’API Twitter (Tweepy v4)  
- **Fine-tuning** du modèle **BERT** (`bert-base-uncased`) sur GPU T4  
- **Prétraitement** complet : nettoyage regex profonds, tokenisation subword, padding/truncation  
- **Représentation** : embeddings contextuels 768 dims + pooling `[CLS]`  
- **Évaluation** : Accuracy, Precision, Recall, F1-score, matrice de confusion  
- **Améliorations** :  
  - Augmentation de données (EDA + back-translation EN↔FR)  
  - Régularisation renforcée (dropout 0.3, weight decay 1e-2, cosine scheduler)

**Résultat** : **Accuracy 76.9 %** → cible **F1 macro > 0.8** après améliorations.

---

## Aperçu visuel

| Présentation | Rapport |
|--------------|--------|
| ![Présentation](https://github.com/ton-pseudo/QuiTweet-Trump-Trudeau/raw/main/assets/presentation_cover.png) | ![Rapport](https://github.com/ton-pseudo/QuiTweet-Trump-Trudeau/raw/main/assets/rapport_cover.png) |

---

## Structure du dépôt
