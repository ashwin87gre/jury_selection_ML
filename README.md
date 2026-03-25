# Human vs Machine Prediction Analysis

This repository contains the supporting code and analysis for the paper:

**_Predicting Juror Predisposition Using Machine Learning: A Comparative Study of Human and Algorithmic Jury Selection_**

---

## 📌 Overview

This project investigates how machine learning models compare against human experts in predicting juror decisions. We evaluate:

- **Human consultants (majority vote)**
- **Random Forest**
- **K-Nearest Neighbors (KNN)**

The goal is to understand:
- Where models outperform humans
- Where humans outperform models
- How their errors overlap
- Whether observed differences are statistically significant

---

## ⚙️ What This Repository Provides

The main notebook:

👉 **`human_vs_ml_evaluation.ipynb`**

It performs:

### 1. Model Evaluation
- Accuracy
- Precision
- Recall
- F1 score

### 2. Statistical Comparison
- **Paired bootstrap** confidence intervals for accuracy differences
- **McNemar’s test** for significance on paired predictions

### 3. Error Analysis
- Fine-grained **error overlap patterns** between humans and models
- Identification of agreement vs disagreement regions

### 4. Visualization
- Error overlap bar plots  
- Row-normalized confusion matrices  
- Accuracy comparison with confidence intervals  

All figures are **publication-ready** and saved as `.png` and `.pdf`.

---

## 📂 Repository Structure
```text
.
├── human_vs_ml_evaluation.ipynb
├── outputs/
│   ├── error_overlap_human_vs_models.png
│   ├── confusion_matrices_human_rf_knn.png
│   ├── teaser_human_vs_ml_accuracy.png
│   └── model_vs_human_evaluation_summary.csv
├── requirements.txt
└── README.md

---

## 📊 Dataset

The dataset contains:

- Ground truth labels (`y_true`)
- Predictions from:
  - Random Forest (`y_pred_rf`)
  - KNN (`y_pred_knn`)
- Labels from three human experts:
  - `human_expert_1`
  - `human_expert_2`
  - `human_expert_3`

A **majority vote** is used to construct the human baseline.

---

## 🚀 Getting Started

### 1. Clone the repository
git clone <your-repo-link>
cd <repo-name>

### 2. Install dependencies
pip install -r requirements.txt

### 3. Run the notebook
Open:
human_vs_ml_evaluation.ipynb
and execute all cells.

---

## 📈 Key Methodological Details

### 🔹 Paired Bootstrap
We estimate confidence intervals for the difference in accuracy between models and humans using paired resampling.

### 🔹 McNemar’s Test
We test statistical significance using McNemar’s test, focusing on discordant predictions.

### 🔹 Error Pattern Analysis
We encode joint error patterns across human and models to analyze disagreement regions.

---

## 📌 Reproducibility

- Fixed random seeds are used
- No hardcoded results
- Outputs are automatically saved

---

## 📄 Citation

@article{juror_prediction_2026,
  title={Predicting Juror Predisposition Using Machine Learning: A Comparative Study of Human and Algorithmic Jury Selection},
  author={Ashwin Murthy; Ramesh Krishnamaneni; Sean Chacon; Kelsey Carlson; Ranjita Naik},
  year={2026}
}

---

## 📬 Contact

For questions or collaborations, feel free to reach out.
