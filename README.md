# CIFAR-10 Image Classifier

A Convolutional Neural Network (CNN) built with **Keras and TensorFlow** that classifies images from the CIFAR-10 dataset into 10 categories with **80%+ accuracy**.

---

## Dataset

**CIFAR-10** contains 60,000 $32 \times 32$ color images divided into 10 classes:
* Airplane, Automobile, Bird, Cat, Deer, Dog, Frog, Horse, Ship, Truck

---

## Model Architecture

The model uses a **VGG-style CNN** with 3 blocks to prevent overfitting:

* **Conv Block 1:** 2x Conv2D (32 filters) + BatchNormalization + MaxPooling + Dropout (0.2)
* **Conv Block 2:** 2x Conv2D (64 filters) + BatchNormalization + MaxPooling + Dropout (0.3)
* **Conv Block 3:** 2x Conv2D (128 filters) + BatchNormalization + MaxPooling + Dropout (0.4)
* **Classifier:** Flatten $\rightarrow$ Dense (128) $\rightarrow$ Dropout (0.5) $\rightarrow$ Output (10 classes, Softmax)

---

## Key Features

* **Data Preprocessing:** Pixel scaling (0 to 1) and channel-wise standardization.
* **Data Augmentation:** Random flips and shifts to improve model generalization.
* **Training:** Optimized using Adam with Categorical Cross-Entropy loss.

---

## How to Run

1. Open the notebook in **Google Colab**.
2. Go to **Runtime $\rightarrow$ Change runtime type** and select **T4 GPU**.
3. Run all cells.
