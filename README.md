
# 🚀 Machine Learning Model Selection & Hyperparameter Tuning

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

## 📊 Output File

### ✔ `model_performance_results.csv`

This file contains **one row per model**, including:

| Model | Train Accuracy | Test Accuracy | Train F1 | Test F1 | Precision | Recall | ROC-AUC | Best Params |
|-------|----------------|--------------|---------|--------|----------|--------|--------|-----------|

The **Best Params** column stores the tuned hyperparameters for each model.

---

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

## 📝 License

This project is licensed under the MIT License. Feel free to modify and reuse.
