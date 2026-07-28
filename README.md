# Predicting Heart Disease Using SMOTE-Based Data Balancing and Ensemble Learning

This repository contains the source code, experimental materials, figures, and published paper associated with our research:

> **Predicting Heart Disease Using SMOTE-Based Data Balancing and Ensemble Learning**

The study was published in the **2026 International Conference on Artificial Intelligence for Sustainable Engineering and Innovation (AISEI)**. It presents a machine learning framework for binary heart disease prediction using systematic data preprocessing, SMOTE-based class balancing, hyperparameter optimization, multiple supervised classifiers, and ensemble learning.

---

## 📌 Overview

Heart disease remains a major global health concern, while timely diagnosis can be challenging in resource-constrained healthcare environments. This research investigates whether conventional machine learning models combined with appropriate preprocessing, class balancing, and ensemble learning can provide accurate heart disease predictions using commonly available clinical attributes.

Eight individual machine learning algorithms were evaluated. Selected classifiers were subsequently combined using **Soft Voting** and **Stacking Ensemble** techniques to improve predictive performance and generalization.

---

## 📊 Dataset

The study uses the **Heart Disease dataset from the UCI Machine Learning Repository**.

- **Total Records:** 303
- **Total Attributes:** 14
- **Input Features:** 13
- **Target Variable:** 1
- **Task:** Binary Classification
- **Class 0:** No Heart Disease
- **Class 1:** Heart Disease

The dataset contains clinical attributes related to age, sex, chest pain, resting blood pressure, cholesterol, electrocardiographic results, maximum heart rate, exercise-related indicators, and thalassemia.

### Dataset Source

[UCI Machine Learning Repository – Heart Disease Dataset](https://archive.ics.uci.edu/dataset/45/heart+disease)

---

## ⚙️ Proposed Methodology

The experimental pipeline includes:

1. Dataset acquisition
2. Missing-value identification and median imputation
3. Numerical data conversion
4. Duplicate record removal
5. Binary target transformation
6. IQR-based outlier handling
7. One-hot encoding
8. Min-Max feature scaling
9. Train-test splitting
10. SMOTE-based class balancing
11. Hyperparameter optimization
12. Individual model training
13. Soft Voting and Stacking Ensemble construction
14. Performance evaluation

SMOTE was used to address class imbalance by generating synthetic minority-class samples, helping reduce prediction bias without simply duplicating existing observations.

---

## 🤖 Machine Learning Models

The following eight individual classifiers were evaluated:

- Logistic Regression (LR)
- Decision Tree (DT)
- Random Forest (RF)
- K-Nearest Neighbors (KNN)
- Support Vector Machine (SVM)
- Gradient Boosting (GB)
- AdaBoost
- Naive Bayes (NB)

### Ensemble Learning

Three ensemble configurations were evaluated:

- **Stacking Ensemble (SVM + GB + RF)**
- **Stacking Ensemble (KNN + GB + RF)**
- **Soft Voting Ensemble**

The stacking approach combines multiple base classifiers through a meta-learning strategy, while soft voting combines predicted class probabilities from multiple classifiers.

---

## 📈 Experimental Results

### Individual Classifier Performance

| Model | Accuracy | Precision | Recall | F1-Score |
|---|---:|---:|---:|---:|
| KNN | **91.80%** | 0.9305 | 0.9180 | 0.9180 |
| Gradient Boosting | 90.16% | 0.9096 | 0.9016 | 0.9017 |
| Random Forest | 88.52% | 0.8860 | 0.8852 | 0.8854 |
| Logistic Regression | 88.52% | 0.8900 | 0.8852 | 0.8854 |
| AdaBoost | 85.25% | 0.8640 | 0.8525 | 0.8525 |
| SVM | 85.25% | 0.8532 | 0.8525 | 0.8526 |
| Decision Tree | 77.05% | 0.7948 | 0.7705 | 0.7690 |
| Naive Bayes | 62.30% | 0.6946 | 0.6230 | 0.6014 |

**KNN achieved the highest individual classification accuracy of 91.80%.**

### Ensemble Performance

| Ensemble Model | Accuracy |
|---|---:|
| **Stacking Ensemble (SVM + GB + RF)** | **93.44%** |
| **Soft Voting Ensemble** | **93.44%** |
| Stacking Ensemble (KNN + GB + RF) | 91.80% |

The **Stacking Ensemble (SVM + GB + RF)** and **Soft Voting Ensemble** achieved the highest accuracy of **93.44%**, outperforming all evaluated individual classifiers.

The best ensemble models also achieved an overall **F1-score of 0.93**.

---

## 📏 Evaluation Metrics

The models were evaluated using:

- Accuracy
- Precision
- Recall
- F1-Score
- ROC-AUC
- Confusion Matrix
- Classification Report

These metrics were used to assess both overall predictive performance and the ability of the models to distinguish heart disease from non-heart-disease cases.

---

## 📁 Repository Structure

```text
Heart-Disease-Prediction-SMOTE-Ensemble-Learning/
│
├── README.md
├── LICENSE
├── .gitignore
├── .gitattributes
│
├── notebooks/
│   └── Heart-Disease-Prediction.ipynb
│
├── figures/
│   ├── workflow.png
│   ├── stacking-ensemble-confusion-matrix.png
│   ├── knn-stacking-confusion-matrix.png
│   └── soft-voting-confusion-matrix.png
│
└── Paper/
    └── Published-Paper.pdf
```

---

## 📄 Published Paper

The published conference paper is available in the [`Paper`](./Paper/) directory of this repository.

**Title:** Predicting Heart Disease Using SMOTE-Based Data Balancing and Ensemble Learning

**Conference:** 2026 International Conference on Artificial Intelligence for Sustainable Engineering and Innovation (AISEI)

**Publisher:** IEEE

**Year:** 2026

**Pages:** 416–421

### Authors

- Md Sifatuzzaman Mia
- Nabid Rezuan
- Jahid Shikder
- Hejbulla Asad Shehab
- Anik Biswas
- Md Sadekur Rahman

---

## 🚀 Running the Project

### 1. Clone the Repository

```bash
git clone https://github.com/YOUR-USERNAME/Heart-Disease-Prediction-SMOTE-Ensemble-Learning.git
```

### 2. Open the Project

```bash
cd Heart-Disease-Prediction-SMOTE-Ensemble-Learning
```

### 3. Install Required Libraries

The implementation uses common Python machine learning and data-analysis libraries, including:

```bash
pip install numpy pandas matplotlib seaborn scikit-learn imbalanced-learn jupyter
```

### 4. Run the Notebook

Open the `.ipynb` file located inside the `notebooks/` directory using Jupyter Notebook, JupyterLab, VS Code, or another compatible environment.

---

## 🛠️ Technologies

- Python
- Jupyter Notebook
- Scikit-learn
- Imbalanced-learn
- Pandas
- NumPy
- Matplotlib
- Seaborn
- SMOTE
- Ensemble Learning

---

## 🔑 Key Findings

The experiments demonstrate that ensemble learning can improve heart disease classification over individual classifiers. KNN achieved the highest individual accuracy of **91.80%**, whereas the best stacking and soft voting approaches achieved **93.44% accuracy**.

The results demonstrate the effectiveness of combining systematic preprocessing, SMOTE-based class balancing, hyperparameter optimization, and ensemble learning for heart disease prediction.

---

## 🔮 Future Work

Future work will focus on evaluating the framework using larger, multi-site clinical datasets and investigating advanced approaches such as deep learning, hybrid ensemble models, and Explainable Artificial Intelligence (XAI). Integration with Electronic Health Record (EHR) systems may also be explored to improve the practical usability of the framework.

---

## 📚 Citation

If this repository or research contributes to your work, please cite the associated publication:

```bibtex
@inproceedings{mia2026heart,
  title     = {Predicting Heart Disease Using SMOTE-Based Data Balancing and Ensemble Learning},
  author    = {Mia, Md Sifatuzzaman and Rezuan, Nabid and Shikder, Jahid and Shehab, Hejbulla Asad and Biswas, Anik and Rahman, Md Sadekur},
  booktitle = {2026 International Conference on Artificial Intelligence for Sustainable Engineering and Innovation (AISEI)},
  pages     = {416--421},
  year      = {2026},
  publisher = {IEEE}
}
```

> The citation should be updated with the official DOI and IEEE Xplore bibliographic metadata when available.

---

## ⚠️ Disclaimer

This repository and its associated machine learning models are intended solely for **research and educational purposes**. They are not intended to replace professional medical diagnosis, clinical judgment, or treatment decisions.

---

## 📜 License

The source code in this repository is distributed under the **MIT License**. See the `LICENSE` file for details.

The published paper may be subject to separate IEEE copyright and licensing terms.

---

## ⭐ Acknowledgment

If you find this work useful, please consider citing the published paper and starring this repository.