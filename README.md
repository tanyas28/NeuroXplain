# 🧠 NeuroXplain: Explainable Brain Tumor Detection using Deep Learning

NeuroXplain is an Explainable AI (XAI) system designed to detect brain tumors from MRI scans using deep learning. The project performs a **comparative study between VGG16 and DenseNet121** architectures with transfer learning and fine-tuning. It also incorporates **Grad-CAM** to provide visual explanations, helping to highlight the regions responsible for predictions, thus improving interpretability and trust in medical AI applications.

---

## 📌 Features

- Classification of brain MRI scans into tumor or non-tumor categories
- Comparative performance analysis of **VGG16** and **DenseNet121**
- Grad-CAM visualizations for **model explainability**
- Preprocessing pipeline for MRI data
- Achieved up to **99.81% accuracy on training** and **98% on testing** using VGG16

---

## 🧪 Model Architecture

- **Transfer Learning Models Used:**
  - VGG16
  - DenseNet121
- **Techniques:**
  - Data Augmentation (Rotation, Shift, Flip)
  - Fine-tuning
  - Batch Normalization & Dropout
  - Grad-CAM (Gradient-weighted Class Activation Mapping)

---

## 🗃️ Dataset

- **Source:** Publicly available brain MRI datasets (e.g., Kaggle)
- **Classes:** Tumor, No Tumor
- **Preprocessing:**
  - Resized images to 224x224
  - RGB conversion
  - Normalized using `preprocess_input` from Keras
  - Data augmentation applied to training set

---

## 📊 Results

| Model       | Train Accuracy | Test Accuracy |
|-------------|----------------|---------------|
| VGG16       | 99.81%         | 98.00%        |
| DenseNet121 | ~97.00%        | ~95.00%       |

Grad-CAM heatmaps visually confirmed that the models learned to focus on tumor regions.

---

## 🛠️ Tech Stack

- Python
- TensorFlow / Keras
- NumPy, Pandas, Matplotlib
- Grad-CAM (via `tf.GradientTape`)
- Scikit-learn (for evaluation metrics)

---
## 📈 Future Work
Incorporate multi-class tumor classification (e.g., glioma, meningioma)

Add other explainability methods like LIME or SHAP

Deploy the model using a web framework
