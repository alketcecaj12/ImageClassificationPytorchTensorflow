# 👗 Image Classification — PyTorch vs TensorFlow

> Classifying fashion items from the **Zalando Fashion-MNIST** dataset using neural networks built in both PyTorch and TensorFlow/Keras. A side-by-side comparison of two of the most widely used deep learning frameworks.

---

## 🧭 Project Overview

Fashion-MNIST is a drop-in replacement for the classic MNIST handwritten digits dataset, consisting of 70,000 grayscale images (28×28 pixels) across 10 clothing categories. This project implements and compares classification pipelines in both major deep learning ecosystems.

| Category | Label |
|---|---|
| T-shirt/top | 0 |
| Trouser | 1 |
| Pullover | 2 |
| Dress | 3 |
| Coat | 4 |
| Sandal | 5 |
| Shirt | 6 |
| Sneaker | 7 |
| Bag | 8 |
| Ankle boot | 9 |

---

## 🔬 Scientific Method Applied

**1. Observation** — Raw 28×28 greyscale images of fashion items are difficult to classify by hand; can a neural network learn the visual patterns that distinguish a sandal from an ankle boot?

**2. Hypothesis** — A feedforward neural network trained on pixel intensities should be able to classify Fashion-MNIST items with accuracy well above the 10% random baseline.

**3. Experimentation** — Three notebooks implement progressively more structured approaches: a simple NN baseline, a full Zalando case study, and a PyTorch-native classifier.

**4. Analysis** — Training/validation loss curves, accuracy metrics, and per-class confusion are examined to understand where models succeed and where they struggle (e.g. shirt vs pullover confusion is notoriously hard).

**5. Conclusion** — Both frameworks reach comparable accuracy on this task; the comparison illuminates the trade-offs in API design, verbosity, and flexibility between PyTorch and TensorFlow/Keras.

---

## 📓 Notebooks

### `Zalando_SimpleNN.ipynb`
Baseline feedforward neural network on the Fashion-MNIST dataset. Establishes the performance floor before any architectural tuning.

### `ZalandoCase.ipynb`
Full case study — data exploration, preprocessing, model training, evaluation, and visualisation of predictions on sample images (Coat, Bag, Sandal, Trouser, Ankle Boot).

### `PyTorch_Classifier.ipynb`
PyTorch implementation of the classifier — manual training loop, DataLoader, and `nn.Module` architecture, contrasting with the Keras high-level API approach.

---

## 🛠️ Tech Stack

```
Python 3.x
├── torch / torchvision    — PyTorch classifier + DataLoader
├── tensorflow / keras     — high-level Zalando case study
├── numpy                  — numerical operations
├── matplotlib             — loss curves and prediction visualisation
└── jupyter                — interactive notebooks
```

---

## 🚀 Getting Started

```bash
git clone https://github.com/alketcecaj12/ImageClassificationPytorchTensorflow.git
cd ImageClassificationPytorchTensorflow
jupyter notebook
```

The Fashion-MNIST dataset is downloaded automatically by both `torchvision.datasets` and `tensorflow.keras.datasets` — no manual download needed.

---

## 🖼️ Sample Images

The repo includes raw PNG samples used for manual prediction testing:

`AnkleBoot.png` · `Bag.png` · `Coat.png` · `Sandal.png` · `Trouser.png`

---

## 👤 About

Built by [Alket Cecaj](https://github.com/alketcecaj12) — data scientist and quantitative analyst with a PhD in Industrial Innovation Engineering and deep interest in applied ML across regulated and commercial domains.

---

*Fashion-MNIST was created by Zalando Research as a more challenging benchmark than the original MNIST. Details at [github.com/zalandoresearch/fashion-mnist](https://github.com/zalandoresearch/fashion-mnist).*
