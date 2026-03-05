# AGRIVISION: Plant Disease Classification Using Image-Based Deep Learning (MobileNetV2)

A deep learning computer vision project that classifies plant diseases from leaf images using **Transfer Learning with MobileNetV2**. The model is trained on the **PlantVillage dataset** and evaluated using multiple classification metrics.

---

# 📌 Project Overview

Plant diseases significantly impact agricultural productivity and global food security. Early and accurate detection of plant diseases can help farmers take timely action to reduce crop losses.

This project develops a **deep learning image classification model** capable of identifying **38 different plant disease categories** from plant leaf images.

The model leverages **transfer learning**, utilizing a pretrained convolutional neural network to extract visual features and fine-tuning it for plant disease classification.

---

# 📊 Dataset

This project uses the **PlantVillage Dataset**, a widely used dataset for plant disease recognition tasks.

Dataset characteristics:

* 38 plant disease classes
* Thousands of labeled leaf images
* Multiple crop species
* High-quality annotated dataset

Dataset source:

PlantVillage Dataset
https://www.kaggle.com/datasets/mohitsingh1804/plantvillage

---

# 🧠 Model Architecture

The model uses **MobileNetV2**, a lightweight convolutional neural network designed for efficient image classification.

### Transfer Learning Strategy

1. Load **MobileNetV2 pretrained on ImageNet**
2. Freeze the feature extraction layers
3. Replace the final classification layer
4. Fine-tune the network on the PlantVillage dataset

Architecture overview:

```
Input Image (224×224)
        ↓
MobileNetV2 Feature Extractor
        ↓
Dropout Layer
        ↓
Fully Connected Layer
        ↓
ReLU Activation
        ↓
Output Layer (38 Classes)
```

---

# 🖼️ Image Preprocessing & Data Augmentation

To improve model generalization, several preprocessing and augmentation techniques were applied.

### Image Preprocessing

* Resize images to **224 × 224**
* Convert images to **PyTorch tensors**
* Normalize using **ImageNet mean and standard deviation**

### Data Augmentation

* Random horizontal flip
* Random rotation
* Color jitter (brightness and contrast)

These techniques help the model become more robust to variations in orientation, lighting conditions, and image composition.

---

# ⚙️ Training Configuration

| Parameter     | Value            |
| ------------- | ---------------- |
| Model         | MobileNetV2      |
| Batch Size    | 32               |
| Epochs        | 10               |
| Optimizer     | Adam             |
| Learning Rate | 0.001            |
| Loss Function | CrossEntropyLoss |
| Image Size    | 224 × 224        |

The model was trained using the **PyTorch deep learning framework**.

---

# 📈 Evaluation Metrics

Model performance was evaluated using several classification metrics:

* Accuracy
* Precision
* Recall
* F1-score
* Confusion Matrix

These metrics provide a comprehensive evaluation of the model’s performance across all classes.

---

# 📊 Results

The trained model demonstrates strong performance in classifying plant diseases.

Evaluation outputs include:

* Training and validation loss curves
* Confusion matrix
* Classification report
  
---

This project was developed as part of a **computer vision course project** focusing on practical applications of convolutional neural networks for agricultural image classification.
