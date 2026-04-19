# 🍛 Indian Food Classification using Deep Learning

A deep learning project for **multi-class Indian food image classification (89 classes)** using transfer learning with **MobileNetV2, EfficientNet-B0, and ResNet50**.

---

## 📌 Overview

This project investigates the performance of modern CNN architectures on a **fine-grained food classification task**.  
Unlike standard datasets, this one combines multiple sources, increasing **class diversity, imbalance, and visual similarity**, making the task more challenging.

---

## 🎯 Objectives

- Compare performance of different deep learning architectures  
- Analyze the impact of transfer learning and fine-tuning  
- Study challenges like class imbalance and inter-class similarity  
- Evaluate models using accuracy, precision, recall, and F1-score  

---

## 🧠 Models Used

- **MobileNetV2** — Lightweight, fast, and efficient  
- **EfficientNet-B0** — Well-balanced and stable  
- **ResNet50** — Deep architecture with strong feature extraction  

All models use **ImageNet pretrained weights** with progressive fine-tuning.

---

## ⚙️ Experimental Setup

- **Dataset Split**: 70% Train / 15% Validation / 15% Test  
- **Optimizer**: Adam  
- **Loss Function**: Categorical Crossentropy  
- **Batch Size**: 32 / 64  

### 🔄 Training Strategy

1. Feature extraction (frozen backbone)  
2. Partial fine-tuning  
3. Full fine-tuning  

### 🎨 Data Augmentation

- Color jitter (MobileNetV2)  
- Dropout regularization  
- Learning rate scheduling  

---

## 📊 Results

| Model            | Accuracy | Precision | Recall | F1 Score |
|------------------|----------|-----------|--------|----------|
| MobileNetV2      | 82.38%   | 0.824     | 0.823  | 0.813    |
| EfficientNet-B0  | 82.23%   | **0.836** | 0.822  | 0.823    |
| ResNet50         | **82.81%** | 0.830   | 0.820  | 0.770    |

---

## 📈 Key Observations

- **ResNet50 achieved the highest accuracy (~82.8%)**
- **EfficientNet-B0 delivered the most stable and precise performance**
- **MobileNetV2 achieved competitive results with faster convergence**

### 🟢 High-performing Classes
`biryani`, `jalebi`, `gulab_jamun`, `dal_makhani`

### 🔴 Low-performing Classes
`chicken_tikka`, `rabri`, `chhena_kheeri`

---

## 🔍 Insights

- Class imbalance significantly impacts performance  
- Visually similar dishes often lead to misclassification  
- **Macro F1 (~0.66)** is much lower than **Weighted F1 (~0.82)**  
  → Indicates poor performance on minority classes  

---

## ⚠️ Limitations

- Imbalanced dataset distribution  
- High visual similarity across classes  
- Limited hyperparameter tuning  
- No cross-dataset evaluation  

---

## 🚀 Future Work

- Apply data balancing techniques (oversampling, class weights)  
- Use advanced augmentation (Mixup, CutMix)  
- Experiment with Vision Transformers (ViT)  
- Incorporate attention mechanisms  
- Perform cross-dataset evaluation  

---

## 🧾 Conclusion

This project demonstrates that deep learning models can effectively tackle large-scale food classification tasks.

- **ResNet50** → Best accuracy  
- **EfficientNet-B0** → Best stability & precision  
- **MobileNetV2** → Most efficient  

Performance is heavily influenced by **dataset quality, class balance, and visual similarity**.

---


