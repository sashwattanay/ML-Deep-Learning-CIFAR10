# CIFAR-10 Image Classification with Deep Neural Networks

## Overview
This project focuses on classifying images from the **CIFAR-10 dataset** using a **deep fully connected neural network**. The model is implemented using **Keras with TensorFlow backend** and incorporates **Batch Normalization, L2 Regularization, and Learning Rate Scheduling** to optimize performance.

The objective is to build and train a deep neural network while addressing overfitting and ensuring efficient convergence.

## Skills Demonstrated
This project showcases the following key concepts:
1. **Data Preprocessing**:
   - Normalization of pixel values to the range `[0, 1]` for stable training.
   - Splitting the dataset into **training (80%)**, **validation (20%)**, and **test sets**.

2. **Deep Neural Network Architecture**:
   - Input layer for `32x32x3` RGB images.
   - **20 hidden layers** with:
     - `100 neurons per layer`
     - `Swish` activation function.
     - `He initialization` for weight distribution.
     - **Batch Normalization** for stable training.
   - Output layer with `10 neurons` (softmax activation for classification).

3. **Optimization Techniques**:
   - **Nadam optimizer** for adaptive learning.
   - **Early stopping** to prevent overfitting.
   - **Learning Rate Scheduling** (decays by 2% after every epoch).
   - **L2 Regularization** (`λ=0.0001`) to control model complexity.

4. **Model Evaluation**:
   - Achieved **test accuracy: ~50%**.
   - Validation and learning curves analyzed for diagnosing overfitting.
   - Comparison of training loss and validation loss for model tuning.

## Dataset
The **CIFAR-10 dataset** consists of `60,000` images across `10` classes:
- **Training Samples**: 40,000
- **Validation Samples**: 10,000
- **Test Samples**: 10,000
- **Image Size**: `32x32x3` (RGB)

## Results
- **Best Configuration**:
  - **Batch Size**: `16`
  - **Initial Learning Rate**: `0.00025`
  - **Regularization**: L2 (`λ=0.0001`)
- **Final Test Performance**:
  - **Test Accuracy**: `~50%`
  - **Test Loss**: `~1.63`

## Key Features
- **Batch Normalization**: Stabilizes training and accelerates convergence.
- **Early Stopping**: Automatically stops training when validation loss ceases to improve.
- **Learning Rate Decay**: Ensures smooth convergence over epochs.
- **Proper Data Splitting**: Independent validation set for unbiased hyperparameter tuning.

## Requirements
This project requires:
- Python 3.7 or higher
- Libraries:
  - `tensorflow`
  - `keras`
  - `numpy`
  - `matplotlib`
  - `sklearn`
