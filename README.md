# ✨ Digit Recognizer — MNIST (Handwritten Digit Recognition)

[![License: MIT](https://img.shields.io/badge/License-MIT-green.svg)](LICENSE)

Résumé
------
Projet de reconnaissance de chiffres manuscrits basé sur le dataset MNIST. Le dépôt contient des notebooks (TensorFlow / Keras) montrant l'exploration des données, la construction et l'entraînement d'un CNN, ainsi que des cellules d'évaluation et d'inférence. Objectif : classifier les images 28×28 en 10 classes (0–9).

Contenu du dépôt
----------------
- `notebooks/` — notebooks Jupyter (exploration, entraînement, évaluation, démonstration)  
- `src/` — (optionnel) scripts réutilisables (train.py, predict.py, utils.py)  
- `models/` — modèles sauvegardés (ex : `models/best_model.h5`)  
- `results/` — courbes d'entraînement, matrices de confusion, exemples de prédictions  
- `data/` — (optionnel) données locales / exemples (MNIST est téléchargé automatiquement via Keras)  
- `README.md` — ce fichier  
- `LICENSE` — MIT (si présent)

Prérequis
---------
- Python 3.8+ recommandé  
- TensorFlow 2.x  
- Bibliothèques usuelles : numpy, matplotlib, scikit-learn, pandas, jupyter, tqdm  
(versions exactes à préciser dans `requirements.txt`)

Installation rapide
------------------
1. Cloner le dépôt :
```bash
git clone https://github.com/ayounimohamedaziz/digit-recognizer-mnist.git
cd digit-recognizer-mnist
