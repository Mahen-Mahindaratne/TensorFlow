# Image Classifier: Cats vs. Dogs 🐶🐱

This repository contains a Convolutional Neural Network (CNN) model built with TensorFlow and Keras to perform binary classification on images of cats and dogs.

## 🚀 Project Overview

The goal of this project is to train a deep learning model to accurately identify whether an input image contains a cat or a dog. The model is configured to achieve an accuracy of at least **63%** on a provided test set.

***

## 📁 Files

* `image_classifier.py`: The main script containing the model definition, data loading, training process, and evaluation logic.

***

## ⚙️ Model Architecture

The model uses a Sequential CNN architecture with the following layers:

* **Convolutional Block 1:** `Conv2D` (32 filters) followed by `MaxPooling2D`.
* **Convolutional Block 2:** `Conv2D` (64 filters) followed by `MaxPooling2D`.
* **Convolutional Block 3:** `Conv2D` (128 filters) followed by `MaxPooling2D`.
* **Classifier Head:** `Flatten` layer, a `Dense` layer (512 units with `relu` activation), and a final `Dense` output layer (1 unit with `sigmoid` activation for binary classification).

### Training Configuration

* **Image Size**: 150x150 pixels
* **Batch Size**: 128
* **Epochs**: 15
* **Optimizer**: `adam`
* **Loss Function**: `binary_crossentropy`
* **Metrics**: `accuracy`

***

## 💻 How to Run

This code is best executed in a **Google Colaboratory** environment due to its use of Colab-specific shell commands for data fetching and environment setup (`!wget`, `!unzip`, etc.).

1.  **Open in Colab:** Upload the `image_classifier.py` file to your Google Drive and open it with Google Colaboratory.
2.  **Install Libraries (if needed):** The notebook automatically attempts to use TensorFlow 2.x.
3.  **Run Cells:** Run all the cells in the notebook. This will automatically:
    * Download and unzip the `cats_and_dogs.zip` dataset.
    * Define the image data generators.
    * Build and compile the CNN model.
    * Train the model for 15 epochs.
    * Display the training/validation accuracy and loss plots.
    * Evaluate the model against the test set and print the final percentage of correctly identified images.

***

## 📊 Data Source

The dataset is a collection of cat and dog images provided by freeCodeCamp and is downloaded directly within the script from the following URL: https://cdn.freecodecamp.org/project-data/cats-and-dogs/cats_and_dogs.zip

The dataset is structured into `train`, `validation`, and `test` directories.