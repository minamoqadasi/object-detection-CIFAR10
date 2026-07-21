# CIFAR-10: Cats vs. Dogs Classifier

A Convolutional Neural Network (CNN) built with **Keras and TensorFlow** to classify images specifically between **Cats** and **Dogs** using a subset of the CIFAR-10 dataset.

## Dataset

This project filters the CIFAR-10 dataset down to **binary classification**:
* **Class 0:** Cat
* **Class 1:** Dog
* **Image Size:** $32 \times 32$ pixels (RGB)

## Model Architecture

The model uses a CNN with regularization to prevent overfitting:

* **Conv Block 1:** 2x Conv2D (32 filters) + BatchNormalization + MaxPooling + Dropout (0.2)
* **Conv Block 2:** 2x Conv2D (64 filters) + BatchNormalization + MaxPooling + Dropout (0.3)
* **Conv Block 3:** 2x Conv2D (128 filters) + BatchNormalization + MaxPooling + Dropout (0.4)
* **Classifier:** Flatten $\rightarrow$ Dense (128) $\rightarrow$ Dropout (0.5) $\rightarrow$ Output (2 classes)

## Key Features

* **Data Filtering:** Isolates cat and dog labels from the 10-class CIFAR-10 dataset.
* **Data Preprocessing:** Pixel scaling (0 to 1) and channel-wise standardization.
* **Data Augmentation:** Random horizontal flips and shifts to boost accuracy.
* **Training:** Optimized using Adam and Categorical Cross-Entropy loss.

## How to Run

1. Open the notebook in **Google Colab**.
2. Go to **Runtime $\rightarrow$ Change runtime type** and select **T4 GPU**.
3. Run all cells to train and evaluate.
