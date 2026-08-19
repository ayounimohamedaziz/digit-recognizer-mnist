# ✈️ PlanesNet — Détection d'avions dans des images satellite

[![License: MIT](https://img.shields.io/badge/License-MIT-green.svg)](LICENSE)

Résumé
------
PlanesNet est un projet de classification binaire qui détecte la présence d'avions dans de petites vignettes extraites d'images satellite. Le modèle est implémenté avec TensorFlow/Keras.  
Résultat clé reproduit dans ce dépôt : **val_accuracy = 97.4%** sur le jeu de validation.

Contenu du dépôt
----------------
- data/ — jeux de données (ou scripts de téléchargement). Exemple attendu : `data/planesnet.json`  
- src/ — code réutilisable (train.py, predict.py, utils.py)  
- notebooks/ — notebooks d’exploration et démonstration (ex. analyses, visualisations)  
- models/ — modèles / poids sauvegardés (ex. `models/best.h5`)  
- results/ — courbes d'entraînement, matrices de confusion, exemples d'images  
- README.md — ce fichier  
- LICENSE — MIT

Prérequis
---------
- Python 3.8+ recommandé  
- TensorFlow 2.x  
- Bibliothèques usuelles : numpy, scikit-learn, matplotlib, pandas, tqdm  
(versions exactes à figer dans `requirements.txt`)

Installation rapide
------------------
1. Cloner le dépôt :
