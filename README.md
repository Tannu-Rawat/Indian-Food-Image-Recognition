```markdown
# 🍛 Indian Food Classification using Deep Learning

A deep learning project for **multi-class Indian food image classification (89 classes)** using transfer learning with **MobileNetV2, EfficientNet-B0, and ResNet50**.

---

## 📌 Overview

This project explores how different CNN architectures perform on a **fine-grained food classification task**.  
The dataset combines multiple sources, making it more challenging than typical benchmarks with fewer classes.

---

## 🎯 Objectives

- Compare deep learning architectures  
- Analyze impact of transfer learning and fine-tuning  
- Study effects of class imbalance and visual similarity  
- Evaluate performance using accuracy, precision, recall, and F1-score  

---

## 🧠 Models Used

- **MobileNetV2** – lightweight and efficient  
- **EfficientNet-B0** – stable and well-balanced  
- **ResNet50** – deeper architecture with strong feature learning  

All models use **ImageNet pretrained weights** with progressive fine-tuning.

---

## ⚙️ Experimental Setup

- **Dataset split**: 70% Train / 15% Validation / 15% Test  
- **Optimizer**: Adam  
- **Loss Function**: Categorical Crossentropy  
- **Batch Size**: 32 / 64  

### Training Strategy
- Feature extraction (frozen backbone)  
- Partial fine-tuning  
- Full fine-tuning  

### Augmentation
- Color jitter (MobileNetV2)  
- Dropout and learning rate scheduling  

---

## 📊 Results

| Model            | Accuracy | Precision | Recall | F1 Score |
|------------------|----------|-----------|--------|----------|
| MobileNetV2      | 82.38%   | 0.824     | 0.823  | 0.813    |
| EfficientNet-B0  | 82.23%   | **0.836** | 0.822  | 0.823    |
| ResNet50         | **82.81%** | 0.83    | 0.82   | 0.77     |

---

## 📈 Key Observations

- **ResNet50 achieved the highest accuracy (~82.8%)**  
- **EfficientNet-B0 showed the most stable and precise performance**  
- **MobileNetV2 provided competitive results with faster learning**  

- High-performing classes:  
  `biryani`, `jalebi`, `gulab_jamun`, `dal_makhani`  

- Low-performing classes:  
  `chicken_tikka`, `rabri`, `chhena_kheeri`  

---

## 🔍 Insights

- Class imbalance significantly affects performance  
- Visually similar dishes lead to misclassification  
- Macro F1 (~0.66) is much lower than weighted F1 (~0.82), showing poor performance on minority classes  

---

## ⚠️ Limitations

- Imbalanced dataset  
- High inter-class similarity  
- Limited hyperparameter tuning  
- No cross-dataset evaluation  

---

## 🚀 Future Work

- Data balancing (oversampling, class weighting)  
- Advanced augmentation (Mixup, CutMix)  
- Use of Vision Transformers (ViT)  
- Fine-grained feature learning (attention mechanisms)  
- Cross-dataset evaluation  

---

## 🧾 Conclusion

This project shows that deep learning models can effectively handle large-scale food classification tasks.  
**ResNet50 performs best in terms of accuracy**, while **EfficientNet provides better stability and precision**, and **MobileNetV2 offers an efficient alternative**.  

Performance is strongly influenced by dataset characteristics such as class imbalance and visual similarity.

---

## 📂 Project Structure

```

├── data/
├── models/
├── notebooks/
├── results/
├── utils/
├── README.md

````

---

## ▶️ How to Run

```bash
git clone <repo-link>
cd project-folder
pip install -r requirements.txt
python train.py
````

---

## ⭐ Acknowledgment

* ImageNet pretrained models
* Multiple Indian food datasets used for training

---

⭐ If you found this useful, consider giving it a star!

```
```
