

# 🧠 CIFAR-10 Image Classification using CNN (PyTorch)

##  Overview

This project implements a **Convolutional Neural Network (CNN)** using PyTorch to classify images from the CIFAR-10 dataset into 10 different classes.

The model is trained using data augmentation techniques and achieves strong performance on both training and testing data.

---

##  Dataset

* **Dataset:** CIFAR-10
* **Classes (10):**
  Airplane, Automobile, Bird, Cat, Deer, Dog, Frog, Horse, Ship, Truck
* **Image Size:** 32 × 32 (RGB)

---

##  Data Preprocessing

### Training Transformations:

* Random Crop (32×32 with padding)
* Random Horizontal Flip
* Normalization (mean = 0.5, std = 0.5)

### Testing Transformations:

* Random Crop
* Normalization

---

##  Model Architecture

The CNN consists of:

###  Convolution Blocks:

* Conv2D → BatchNorm → ReLU → MaxPooling
* 3 such blocks with increasing channels:

  * 3 → 32
  * 32 → 64
  * 64 → 128

###  Fully Connected Layers:

* Flatten layer
* Dense (128×4×4 → 512)
* Dropout (0.5)
* Output Layer (512 → 10)

### 📊 Total Parameters:

**~1.14 Million**

---

##  Training Details

* **Optimizer:** Adam
* **Learning Rate:** 0.001
* **Loss Function:** CrossEntropyLoss
* **Epochs:** 50
* **Batch Size:** 32
* **Device:** GPU (CUDA)

---

## 📈 Results

| Metric            | Value   |
| ----------------- | ------- |
| Training Accuracy | **87%** |
| Testing Accuracy  | **90%** |

 The model generalizes well and avoids overfitting.

---

##  Visualization

* Training Loss vs Epochs
* Training vs Testing Accuracy

---

##  Notes

* Image normalization causes pixel values to range between **[-1, 1]**, which may trigger visualization warnings — this is expected.
* Data augmentation helps improve generalization.

---

##  Future Improvements

* Use deeper architectures (ResNet, EfficientNet)
* Implement learning rate scheduling
* Train on CIFAR-100
* Add confusion matrix & class-wise accuracy

---

##  Tech Stack

* Python
* PyTorch
* Torchvision
* NumPy
* Matplotlib

---

##  Author

Aman Shaikh

---

##  Acknowledgment

This project is part of my journey in **Deep Learning and Computer Vision**.

---
