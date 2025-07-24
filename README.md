# Credit-Card-Fraud-Detection

📌 Project Overview
This project focuses on detecting fraudulent credit card transactions using machine learning techniques. Fraudulent transactions are extremely rare compared to non-fraudulent transactions, making this an imbalanced classification problem.
We use Logistic Regression and Random Forest models to predict fraud, applying SMOTE to handle class imbalance.

## 📊 Dataset
Source: Kaggle - Credit Card Fraud Detection

Total Transactions: 284,807

Fraudulent Transactions: 492 (~0.172%)

Features: 30 (V1–V28, Time, Amount)

Target: Class (0 = Not Fraud, 1 = Fraud)

## 🛠 Technologies & Libraries
Language: Python 3

Libraries:

pandas, numpy → Data manipulation

matplotlib, seaborn → Data visualization

scikit-learn → ML models & metrics

imbalanced-learn → SMOTE for class imbalance

joblib → Model persistence

## 🔍 Methodology
1. Data Cleaning & Preprocessing
Remove null values and duplicates

Standardize Time and Amount using StandardScaler

2. Handling Class Imbalance
Applied SMOTE (Synthetic Minority Oversampling Technique) to balance the dataset

3. Model Training
Logistic Regression: Baseline model

Random Forest: Ensemble model with hyperparameter tuning

4. Hyperparameter Tuning
Used RandomizedSearchCV for Random Forest:

n_estimators, max_depth, min_samples_split, max_features

## 📊 Results (Sample)
| Model              | Precision | Recall | F1-Score | ROC-AUC |
|--------------------|-----------|--------|----------|---------|
| Logistic Regression|   0.82    |  0.65  |  0.73    |  0.94   |
| Random Forest      |   0.97    |  0.91  |  0.94    |  0.99   |

---

## ▶ How to Run
```bash
# Clone the repo
git clone https://github.com/yourusername/credit-card-fraud-detection.git
cd credit-card-fraud-detection

# Install dependencies
pip install -r requirements.txt

# Run the Jupyter Notebook
jupyter notebook CreditCardFraudDetection.ipynb
