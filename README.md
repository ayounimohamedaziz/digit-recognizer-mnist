# 🔢 Digit Recognizer - MNIST Handwritten Digit Classification

[![Python](https://img.shields.io/badge/Python-3.10%2B-blue?logo=python)](https://www.python.org/)
[![TensorFlow](https://img.shields.io/badge/TensorFlow-2.x-orange?logo=tensorflow)](https://www.tensorflow.org/)
[![Keras](https://img.shields.io/badge/Keras-Deep%20Learning-red?logo=keras)](https://keras.io/)
[![Kaggle](https://img.shields.io/badge/Kaggle-Competition-blue?logo=kaggle)](https://www.kaggle.com/competitions/digit-recognizer)
[![License](https://img.shields.io/badge/License-MIT-green.svg)](LICENSE)

An end-to-end Computer Vision project implementing a Convolutional Neural Network (CNN) in **TensorFlow/Keras** to classify 28x28 grayscale images of handwritten digits (0 through 9) from the famous **MNIST benchmark**.

---

## 📌 Project Overview

This project addresses the classic multi-class handwritten digit recognition challenge hosted on Kaggle. By designing a deep convolutional neural network, the model automatically learns spatial feature hierarchies (edges, curves, loops) directly from raw pixel intensity values.

### Key Highlights
- **Multi-Class Classification**: Softmax activation across 10 output classes (digits 0–9) using `CategoricalCrossentropy` loss.
- **Data Preprocessing & Reshaping**: Normalized pixel values from `[0, 255]` to `[0.0, 1.0]` and transformed flattened 784-feature CSV vectors into `(28, 28, 1)` tensor representations.
- **CNN Architecture**: Stack of Convolutional (`Conv2D`), Pooling (`MaxPooling2D`), Batch Normalization, and Dense layers with `ReLU` activations.

---

## 📊 Model & Performance

| Parameter / Metric | Description / Value |
| :--- | :--- |
| **Input Shape** | `(28, 28, 1)` |
| **Num Classes** | `10` (Digits 0–9) |
| **Optimizer** | `Adam` |
| **Loss Function** | `CategoricalCrossentropy` |
| **Regularization** | `BatchNormalization` + `Dropout` |

---

## 📁 Repository Structure

```text
.
├── digit_recognizer.ipynb  # Full notebook containing EDA, data preprocessing, CNN training & evaluations
├── submission.csv          # Formatted test set predictions ready for Kaggle evaluation
├── .gitignore              # Ignores large raw dataset CSVs (train.csv, test.csv)
└── README.md               # Project documentation
