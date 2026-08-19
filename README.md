# 🔢 Handwritten Digit Recognizer (MNIST)

Ce projet implémente un réseau de neurones convolutif (**CNN**) sous TensorFlow/Keras pour la reconnaissance de chiffres manuscrits (de 0 à 9) à partir du jeu de données **Kaggle Digit Recognizer (MNIST)**.

---

## 📌 Présentation du Projet
* **Objectif** : Classification d'images multi-classes (10 classes : chiffres 0 à 9).
* **Dataset** : Kaggle Digit Recognizer — 42 000 images d'entraînement en niveaux de gris de dimensions $28 \times 28$ pixels.
* **Résultat Clé** : Précision supérieur à **99 %** (`val_accuracy`) sur le jeu de validation.

---

## ⚙️ Traitement des Données & Pipeline

1. **Reconstruction des Images** :
   * Transformation du vecteur aplati de 784 pixels en matrice 3D : `(28, 28, 1)`.
2. **Normalisation** :
   * Conversion des valeurs de pixels de l'intervalle $[0, 255]$ vers $[0.0, 1.0]$.
3. **Data Augmentation** :
   * Application de légères rotations, zooms et décalages (width/height shift) pour améliorer la généralisation du modèle face à différentes écritures manuscrites.
4. **Découpage des Données** :
   * Séparation en jeux d'entraînement et de validation (ex. 90% Train / 10% Validation).

---

## 🧠 Architecture du Modèle

```text
Input (28x28x1)
  │
  ├── Conv2D (32 filtres, 3x3) + ReLU
  ├── Conv2D (32 filtres, 3x3) + ReLU
  ├── MaxPool2D (2x2) + Dropout (0.25)
  │
  ├── Conv2D (64 filtres, 3x3) + ReLU
  ├── Conv2D (64 filtres, 3x3) + ReLU
  ├── MaxPool2D (2x2) + Dropout (0.25)
  │
  ├── Flatten
  ├── Dense (256 neurones) + ReLU + Dropout (0.5)
  └── Output: Dense (10 neurones) + Softmax
