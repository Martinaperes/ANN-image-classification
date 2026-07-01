
# ANN Image Classification on CIFAR-10

An image classification project built using **TensorFlow** and **Keras** that trains an **Artificial Neural Network (ANN)** to classify images from the **CIFAR-10** dataset. This project also investigates the impact of hardware on deep learning by comparing model training on a **CPU** and a **GPU**.

---

##  Overview

Image classification is one of the most common applications of deep learning. Although **Convolutional Neural Networks (CNNs)** are generally the preferred choice for image classification, this project intentionally uses an **Artificial Neural Network (ANN)** to compare the computational performance of CPU and GPU hardware during model training.

The model is trained on the **CIFAR-10** dataset, which consists of 60,000 real-world color images belonging to ten different classes. The objective is to train the network to accurately classify these images while evaluating the difference in training speed between CPU and GPU execution.

---

## Objectives

- Build an Artificial Neural Network (ANN) using TensorFlow and Keras.
- Train the model using the CIFAR-10 dataset.
- Evaluate the model's classification accuracy.
- Compare the training performance of CPU and GPU.
- Visualize training metrics using TensorBoard.

---

## Dataset

The project uses the **CIFAR-10** dataset provided by TensorFlow.

```python
from tensorflow.keras.datasets import cifar10

(X_train, y_train), (X_test, y_test) = cifar10.load_data()
```

### Dataset Statistics

- **60,000** color images
- **50,000** training images
- **10,000** testing images
- Image size: **32 × 32 pixels**
- **10 image classes**

### Image Classes

- ✈️ Airplane
- 🚗 Automobile
- 🐦 Bird
- 🐱 Cat
- 🦌 Deer
- 🐶 Dog
- 🐸 Frog
- 🐴 Horse
- 🚢 Ship
- 🚚 Truck

---

## Technologies Used

- Python
- TensorFlow
- Keras
- NumPy
- Matplotlib
- TensorBoard
- Jupyter Notebook

---

## Model Architecture

The ANN consists of:

- Input layer
- Flatten layer
- Fully connected (Dense) layer(s)
- Output layer with 10 neurons for multi-class classification

Unlike CNNs, which automatically learn spatial features from images, the ANN operates on flattened image data. This architecture was selected to support the project's goal of comparing CPU and GPU training performance.

---

## Data Preprocessing

Before training, the following preprocessing steps are performed:

- Load the CIFAR-10 dataset.
- Normalize pixel values to the range **0–1**.
- Flatten each **32 × 32 × 3** image into a one-dimensional feature vector.
- Prepare labels for multi-class classification.

---

##  Model Training

The model is trained using TensorFlow/Keras and evaluated using classification accuracy.

Training includes:

- Forward propagation
- Backpropagation
- Gradient descent optimization
- Accuracy and loss monitoring

TensorBoard is used to visualize the training process.

---

##  TensorBoard

Launch TensorBoard using:

```bash
python -m tensorboard.main --logdir=logs
```

Open your browser and navigate to:

```text
http://localhost:6006
```

TensorBoard provides visualizations of:

- Training accuracy
- Training loss
- Model graph
- Weight histograms

---

##  CPU vs GPU Comparison

This project compares model training on CPU and GPU hardware.

### CPU

- Suitable for small and medium-sized machine learning tasks.
- Executes computations sequentially with limited parallel processing.
- Longer training times for deep learning models.

### GPU

- Designed for massively parallel computation.
- Significantly faster training for neural networks.
- Better suited for large datasets and deep learning applications.

Although the ANN architecture remains the same, the hardware used can significantly affect training time.

---

##  Project Structure

```text
ANN-Image-Classification/
│
├── ANN_Image_Classification.ipynb
├── README.md
├── requirements.txt
├── .gitignore
└── logs/
```

---

##  Getting Started

### 1. Clone the repository

```bash
git clone https://github.com/Martinaperes/ANN_image_classification.git
```

### 2. Navigate to the project directory

```bash
cd your-repository
```

### 3. Install dependencies

```bash
pip install tensorflow numpy matplotlib
```

### 4. Launch Jupyter Notebook

```bash
jupyter notebook
```

### 5. Open the notebook and run all cells

---

##  Future Improvements

- Implement a Convolutional Neural Network (CNN) and compare its performance with the ANN.
- Perform hyperparameter tuning.
- Experiment with different optimizers.
- Add data augmentation.
- Compare additional performance metrics such as inference time and memory usage.

---

##  Contributing

Contributions, suggestions, and improvements are welcome.

If you would like to contribute:

1. Fork the repository.
2. Create a new feature branch.
3. Commit your changes.
4. Submit a pull request.

---


