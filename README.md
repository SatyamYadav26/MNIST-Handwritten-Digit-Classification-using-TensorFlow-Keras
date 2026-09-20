# MNIST Handwritten Digit Classification using TensorFlow/Keras

## 📌 Overview

This project implements a simple neural network using **TensorFlow/Keras** to classify handwritten digits from **0 to 9** using the MNIST dataset.

The project covers dataset exploration, preprocessing, neural network training, model evaluation, visualization of training performance, and comparison of the original model with a Dropout-based model.

## 🎯 Objectives

* Load and explore the MNIST dataset.
* Display sample handwritten digit images.
* Normalize and preprocess the image data.
* Build and train a neural network using TensorFlow/Keras.
* Evaluate the model using test accuracy.
* Visualize training and validation accuracy and loss.
* Test the model on five handwritten images.
* Compare the original model with a modified model using Dropout.

## 📊 Dataset

The **MNIST dataset** contains:

* 60,000 training images
* 10,000 testing images
* Image size: 28 × 28 pixels
* Grayscale images
* 10 classes: digits 0–9

The dataset is loaded directly using TensorFlow/Keras.

```python
from tensorflow.keras.datasets import mnist

(x_train, y_train), (x_test, y_test) = mnist.load_data()
```

## 🧠 Model Architecture

The basic neural network consists of:

```text
Input Image (28 × 28)
        ↓
     Flatten
        ↓
Dense Layer (128 neurons, ReLU)
        ↓
Dense Layer (64 neurons, ReLU)
        ↓
Dense Layer (10 neurons, Softmax)
        ↓
Predicted Digit (0–9)
```

## ⚙️ Preprocessing

The pixel values are normalized from the range **0–255** to **0–1**.

```python
x_train = x_train.astype("float32") / 255.0
x_test = x_test.astype("float32") / 255.0
```

## 🏋️ Training

The model is trained using:

* **Optimizer:** Adam
* **Loss Function:** Sparse Categorical Cross-Entropy
* **Metric:** Accuracy
* **Epochs:** 10
* **Batch Size:** 32

A portion of the training data is used for validation.

## 📈 Evaluation

The trained model is evaluated on the test dataset using classification accuracy.

The project also includes:

* Training vs. validation accuracy graph
* Training vs. validation loss graph
* Actual vs. predicted labels for five test images

## 🧪 Experiment

An additional experiment is performed by adding **Dropout layers with a rate of 0.2** to the neural network.

### Original Model

```text
Flatten → Dense(128) → Dense(64) → Dense(10)
```

### Modified Model

```text
Flatten → Dense(128) → Dropout(0.2)
        → Dense(64) → Dropout(0.2)
        → Dense(10)
```

The test accuracy of both models is compared to observe the effect of Dropout.

## 📁 Project Structure

```text
MNIST-Handwritten-Digit-Classification/
│
├── MNIST_Digit_Classification.ipynb
├── MNIST_Digit_Classification_Report.pdf
├── requirements.txt
├── README.md
│
└── images/
    ├── sample_digits.png
    ├── accuracy_plot.png
    ├── loss_plot.png
    └── predictions.png
```

## 🛠️ Technologies Used

* Python
* TensorFlow
* Keras
* NumPy
* Pandas
* Matplotlib
* Jupyter Notebook

## 🚀 How to Run

### 1. Clone the repository

```bash
git clone https://github.com/YourUsername/MNIST-Handwritten-Digit-Classification.git
```

### 2. Navigate to the project folder

```bash
cd MNIST-Handwritten-Digit-Classification
```

### 3. Install the required libraries

```bash
pip install -r requirements.txt
```

### 4. Open the Jupyter Notebook

```bash
jupyter notebook
```

Open:

```text
MNIST_Digit_Classification.ipynb
```

Run the cells sequentially to train and evaluate the model.

## 📌 Results

The model achieves high accuracy on the MNIST test dataset.

| Model                   |   Test Accuracy |
| ----------------------- | --------------: |
| Original Neural Network | Add your result |
| Dropout Model           | Add your result |

> Replace the values above with the actual accuracy obtained after running the notebook.

## 📚 Conclusion

This project demonstrates the implementation of a basic neural network for handwritten digit classification using TensorFlow/Keras. The experiment also shows how modifying the network architecture with Dropout can affect model performance and generalization.


