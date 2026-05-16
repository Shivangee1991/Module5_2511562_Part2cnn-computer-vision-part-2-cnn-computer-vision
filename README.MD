# CNN Computer Vision – Manufacturing Defect Classification

## Project Overview

This project builds a basic Convolutional Neural Network (CNN) model to classify manufacturing product images into different defect categories.

The goal is to understand how CNNs learn image patterns using:
- Convolution layers
- Activation functions
- Pooling layers
- Flattening
- Dense layers

The model classifies product surface images into:
- Normal
- Scratch
- Dent
- Stain

---

# Dataset Information

## Dataset Name
Synthetic Manufacturing Defect Image Dataset

## Classes
- normal
- scratch
- dent
- stain

## Goal
Predict the type of defect present in a product image.

---

# Task 1 – Problem Identification

## Selected Problem Type
Image Classification

## Reason

This dataset represents an image classification problem because:
- Each image belongs to only one category
- The task is to assign a label to the entire image
- No bounding boxes or pixel-level masks are provided

The CNN model predicts which defect class the image belongs to.

---

# Task 2 – Dataset Exploration

Performed:
- Counted number of classes
- Counted images per class
- Displayed sample images
- Checked image dimensions
- Analyzed class imbalance

Observations:
- Dataset contains 4 classes
- Most images have similar dimensions
- Dataset is mostly balanced across classes

---

# Task 3 – Image Preprocessing

The following preprocessing steps were applied:

## Resizing
All images resized to:
- 128 x 128

## Normalization
Pixel values scaled between:
- 0 and 1

## Train-Test Split
Dataset split into:
- 80% training
- 20% testing

## Data Augmentation
Applied:
- Rotation
- Zoom
- Horizontal flip

This helps reduce overfitting.

---

# Task 4 – CNN Model Creation

## CNN Architecture

The CNN model contains:
- Convolution layers
- ReLU activation
- MaxPooling layers
- Flatten layer
- Dense layers
- Softmax output layer

## Loss Function
- Categorical Crossentropy

## Optimizer
- Adam Optimizer

---

# Task 5 – Model Training and Evaluation

Evaluation included:
- Training accuracy
- Validation accuracy
- Loss curves
- Confusion matrix
- Sample predictions

Observations:
- Accuracy improved steadily during training
- CNN successfully identified defect patterns
- Some confusion occurred between scratch and stain classes

---

# Task 6 – CNN Concept Explanation

## What is convolution?

Convolution is a process where small filters scan across the image to detect important patterns like edges, textures, and shapes.

## Why is pooling used?

Pooling reduces image size while keeping important information. It helps reduce computation and prevents overfitting.

## Why is ReLU commonly used in CNNs?

ReLU helps the network learn non-linear patterns and speeds up training.

## Why are CNNs better than regular feed-forward networks for images?

CNNs automatically learn image features using filters and preserve spatial relationships between pixels. Regular neural networks treat all pixels independently and become inefficient for images.

---

# Task 7 – Business Use Case Mapping

## Manufacturing Quality Inspection

This solution can be used in manufacturing industries for automatic defect detection.

Example uses:
- Detect scratches on metal surfaces
- Identify dents in products
- Find stains or surface damage
- Reduce manual inspection effort
- Improve production quality

CNN-based inspection systems can work in real-time and help companies reduce defective product delivery.

---

# Repository Structure

part-2-cnn-computer-vision/
│
├── README.md
├── notebook.ipynb
├── requirements.txt
├── sample_predictions/
│   └── prediction_outputs.png
└── results/
    ├── accuracy_loss_curves.png
    └── confusion_matrix.png

---

# Libraries Used
- pandas
- numpy
- matplotlib
- seaborn
- tensorflow
- scikit-learn
- opencv-python

---

# How to Run

Install dependencies:

```bash id="vgtn7v"
pip install -r requirements.txt