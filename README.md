
# 🚀 Falcon 9 Data Analysis

This project performs model comparison and hyperparameter tuning using **RandomizedSearchCV** across multiple machine-learning models. Each model is evaluated on the training and test datasets, and both the **model performance metrics and the best hyperparameters** are stored together in a single results file.

---


## 🎯 Objective

- Train and compare multiple ML models  
- Perform **hyperparameter tuning** using RandomizedSearchCV  
- Evaluate each model using:
  - Accuracy
  - F1-Score
  - Precision
  - Recall
  - ROC-AUC
- Save **both**
  - Training & test performance metrics
  - Best hyperparameters found during tuning  
  → into **one consolidated results file**

---

## 🧠 Models Used

(Examples — update based on your project)

- Logistic Regression  
- Random Forest  
- Gradient Boosting  
- Support Vector Machine  
- Gaussian Naive Bayes  
- K-Nearest Neighbors  
- (Add or remove models as required)

---

### ✔ `model_performance_results.csv`

This file contains **one row per model** with the following columns:

| Column | Description |
|--------|------------|
| **Model** | Name of the machine-learning model |
| **Model Parameters** | Best hyperparameters selected by RandomizedSearchCV |
| **Train Accuracy** | Accuracy score on the training dataset |
| **Test Accuracy** | Accuracy score on the test dataset |
| **Train F1 Score** | Weighted F1-score on training data |
| **Test F1 Score** | Weighted F1-score on test data |
| **Train Precision** | Precision score on training data |
| **Test Precision** | Precision score on test data |
| **Train Recall** | Recall score on training data |
| **Test Recall** | Recall score on test data |
| **Train Roc Auc Score** | ROC-AUC score on training data |
| **Test Roc Auc Score** | ROC-AUC score on test data |

> ✅ This single file contains **both performance metrics and tuned hyperparameters** for every model.

## ⚙️ Workflow

1. Define models and their hyperparameter search spaces  
2. Run **RandomizedSearchCV**  
3. Train the best configuration for each model  
4. Generate predictions on train & test sets  
5. Calculate evaluation metrics  
6. Store **metrics + best parameters together** in a single CSV file

---

## 🛠️ Tech Stack

- Python
- Scikit-Learn
- Pandas / NumPy


---




## 👤 Author

- Heet Dave  
- heetmdave@gmail.com

---


