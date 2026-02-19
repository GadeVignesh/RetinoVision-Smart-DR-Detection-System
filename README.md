# 🩺 RetinoVision - Smart DR Detection System

An end-to-end deep learning system for automated detection and multi-stage classification of Diabetic Retinopathy (DR) from retinal fundus images using Convolutional Neural Networks (CNN).

---

## 📌 Project Overview

Diabetic Retinopathy (DR) is a diabetes-related eye disease and one of the leading causes of blindness worldwide. Early detection is crucial but manual screening requires expert ophthalmologists and is time-consuming.

This project proposes an AI-based automated screening system that:

- Detects DR from retinal fundus images  
- Classifies images into five severity stages  
- Enhances feature extraction using segmentation  
- Handles dataset imbalance effectively  
- Achieves high classification accuracy  

---

## 🧠 Methodology

### 🔹 Image Preprocessing
- Cropping and resizing images  
- Normalization and brightness adjustment  
- Non-Local Means Denoising (NLMD)  

### 🔹 Data Augmentation
- Rotation (90°, 180°)  
- Brightness scaling  
- Class balancing for underrepresented categories  

### 🔹 Retinal Segmentation
- U-Net based vessel segmentation  
- Region merging to preserve important pathological features  
- Improved detection of retinal abnormalities  

### 🔹 CNN Architecture
The classification model consists of:
- Convolutional layers  
- Max-pooling layers  
- Leaky ReLU activation  
- Dropout (0.5) for regularization  
- Fully connected layers  
- Softmax output layer  

### 🔹 Training Strategy
- Xavier weight initialization  
- Nesterov momentum optimizer  
- 250 training epochs  
- GPU-accelerated training  
- Implemented using **Theano**

---

## 📊 Dataset

- Source: **Kaggle EyePACS Diabetic Retinopathy Dataset**  
- 30,000+ high-resolution retinal fundus images  
- 5 severity classes:
  - 0 – No DR  
  - 1 – Mild  
  - 2 – Moderate  
  - 3 – Severe  
  - 4 – Proliferative DR  

The dataset was highly imbalanced and addressed using augmentation and balanced training.

---

## 📈 Results

- **~95% accuracy** – Binary classification (DR vs No DR)  
- **~85% accuracy** – Five-class severity classification  
- ~93% accuracy after segmentation enhancement  

Model evaluation performed using accuracy metrics and confusion matrix analysis.

---

## 🛠 Tech Stack

- Python  
- Theano  
- NumPy  
- OpenCV  
- GPU Acceleration  
- Kaggle Dataset (EyePACS)  
