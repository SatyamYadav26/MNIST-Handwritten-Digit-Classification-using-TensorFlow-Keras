# MNIST Handwritten Digit Classification

## Overview

This project implements handwritten digit classification using the MNIST dataset and a neural network built with TensorFlow/Keras.

The model classifies handwritten images into one of ten classes: 0 to 9.

## Dataset

MNIST contains:
- 60,000 training images
- 10,000 testing images
- 28 × 28 grayscale images
- 10 digit classes

## Technologies Used

- Python
- TensorFlow
- Keras
- NumPy
- Pandas
- Matplotlib
- Jupyter Notebook

## Model Architecture

Original Model:

Input (28 × 28)
↓
Flatten
↓
Dense (128, ReLU)
↓
Dense (64, ReLU)
↓
Dense (10, Softmax)

## Experiment

A second model was created by adding Dropout layers with a rate of 0.2.

The performance of both models was compared using test accuracy and validation accuracy.

## Results

| Model | Test Accuracy |
|---|---|
| Original Model | XX.XX% |
| Dropout Model | YY.YY% |

## Files

- `MNIST_Digit_Classification.ipynb` - Jupyter Notebook
- `MNIST_Digit_Classification_Report.pdf` - Project report
- `requirements.txt` - Required Python packages

## How to Run

1. Clone the repository.
2. Install dependencies:

```bash
pip install -r requirements.txt
