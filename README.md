# Semiconductor Defect Prediction

This repository presents a complete machine learning and deep learning pipeline for analyzing the **UCI SECOM Dataset**, a real-world dataset from semiconductor manufacturing.  
The objective is to predict whether a chip passes or fails quality control, enabling **predictive quality assurance** in manufacturing processes.

---

## 📊 Dataset Overview
- **Source:** [Kaggle – UCI SECOM Dataset](https://www.kaggle.com/datasets/paresh2047/uci-semcom)  
- **Samples:** 1,567  
- **Features:** 591 sensor readings  
- **Target:** Binary classification → `Pass (1)` / `Fail (0)`  
- **Challenges:** High dimensionality, missing values, outliers  

---

## ⚙️ Methodology

### Data Preprocessing
- Removed non-informative features (`Time`)
- Imputed missing values with column means
- Detected and capped outliers using **IQR method**
- Applied **StandardScaler** for normalization

### Dimensionality Reduction
- **PCA** (Kaiser’s Rule) → 115 components retained  
- **Kernel PCA** (RBF, Polynomial, Linear) → captured non-linear feature interactions  

### Machine Learning Models
- **Decision Tree** → Accuracy: **86.9%**  
- **Logistic Regression** → Accuracy: **88.9%**  
- **Logistic Regression + PCA** → Accuracy: **92.0%**

### Deep Learning Models
- **Convolutional Neural Network (CNN)** → Accuracy: **92.4%**  
- **Artificial Neural Network (ANN)** → Accuracy: **93.3%** ✅ *Best performance*  

---

## 📈 Results

| Model                       | Accuracy |
|-----------------------------|----------|
| Decision Tree               | 86.9%    |
| Logistic Regression         | 88.9%    |
| Logistic Regression + PCA   | 92.0%    |
| CNN                         | 92.4%    |
| **ANN (Best Model)**        | **93.3%** |

- **Dimensionality reduction (PCA)** improved model performance significantly  
- **ANN outperformed all traditional models** by learning complex feature interactions  
- CNN also achieved strong results despite non-image data  

---

## 📂 Repository Contents
- `UCI_SECOM_DATASET.ipynb` → End-to-end notebook (preprocessing, PCA, ML/DL models)  
- `secom_model_report.docx` → Detailed technical report  
- `requirements.txt` → Python dependencies  
- `models/` → Saved trained models (optional)  
- `images/` → Plots and visualizations (ROC curves, scree plots, etc.)  

---

## 🚀 Usage

1. Clone the repository:
   ```bash
   git clone https://github.com/your-username/SECOM-Quality-Prediction.git
   cd SECOM-Quality-Prediction
