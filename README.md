# Transfer_Learning_On_Fashion_MNIST_dataset_Using_VGG16_Model
# 🚀 Fashion MNIST Classification using Transfer Learning (VGG16 + PyTorch)

A deep learning project demonstrating **Transfer Learning** using the **pretrained VGG16 architecture** to classify images from the **Fashion-MNIST** dataset.

Instead of training a CNN from scratch, this project leverages a pretrained ImageNet model and fine-tunes its classifier for Fashion-MNIST, showcasing one of the most effective techniques used in modern computer vision.

---

## 📌 Project Overview

The Fashion-MNIST dataset consists of grayscale images belonging to **10 clothing categories**.

Since VGG16 expects RGB images of size **224×224**, the dataset is preprocessed using torchvision transforms before being passed through the pretrained network.

Only the classifier layers are trained while the convolutional feature extractor remains frozen.

---

## 🖼 Dataset

**Fashion-MNIST**

Classes:

- T-shirt / Top
- Trouser
- Pullover
- Dress
- Coat
- Sandal
- Shirt
- Sneaker
- Bag
- Ankle Boot

Original Image Size:

```
28 × 28 (Grayscale)
```

Input to VGG16:

```
224 × 224 (RGB)
```

---

## 🏗 Model Architecture

### Backbone

- Pretrained **VGG16**
- Weights initialized from **ImageNet**

### Feature Extractor

- Frozen during training
- Learns generic image features

### Custom Classifier

```
Input (25088)

↓

Linear (25088 → 1024)

↓

ReLU

↓

Dropout (0.5)

↓

Linear (1024 → 512)

↓

ReLU

↓

Dropout (0.5)

↓

Linear (512 → 10)
```

---

## 🔄 Data Preprocessing

The following transformations are applied:

- Resize to 256
- Center Crop to 224×224
- Convert grayscale image to RGB
- Convert to Tensor
- Normalize using ImageNet mean and standard deviation

---

## 🛠 Technologies Used

- Python
- PyTorch
- Torchvision
- Pandas
- NumPy
- Matplotlib
- Scikit-Learn

---

## 📂 Project Structure

```
.
├── Pytorch_(Transfer_Learning_Using_VGG_16_Architecture).ipynb
├── fashion-mnist_train.csv
├── README.md
└── requirements.txt
```

---

## ⚙ Training Pipeline

1. Load Fashion-MNIST dataset
2. Split into train/test sets
3. Apply image preprocessing
4. Load pretrained VGG16
5. Freeze convolution layers
6. Replace default classifier
7. Train classifier using Adam optimizer
8. Evaluate training accuracy
9. Evaluate test accuracy

---

## 📈 Loss Function

Cross Entropy Loss

---

## ⚡ Optimizer

Adam Optimizer

---

## 🎯 Objective

Classify Fashion-MNIST images into one of ten clothing categories using transfer learning instead of building a CNN from scratch.

---

## 💡 Why Transfer Learning?

Transfer learning offers several advantages:

- Faster convergence
- Better feature extraction
- Reduced training time
- Improved accuracy with smaller datasets
- Lower computational cost

---

## 📚 Concepts Demonstrated

- Transfer Learning
- Computer Vision
- Image Classification
- Fine-Tuning
- PyTorch Dataset & DataLoader
- Data Augmentation
- GPU Training
- Model Evaluation

---

## 🚀 Future Improvements

- Fine-tune deeper VGG16 layers
- Experiment with ResNet50 and EfficientNet
- Add learning rate scheduling
- Early stopping
- Confusion matrix visualization
- Precision, Recall and F1-score
- TensorBoard integration
- Model checkpoint saving

---

## 📖 References

- PyTorch Documentation
- Torchvision Models
- Fashion-MNIST Dataset
- VGG16 Paper

---

## 👨‍💻 Author

**Sujith Pedapati**

AI & Machine Learning Enthusiast

GitHub: https://github.com/SUJITH-PEDAPATI

---

⭐ If you found this project useful, consider giving the repository a star.
