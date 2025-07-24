# Credit-Card-Fraud-Detection

````markdown
# 💳 Credit Card Fraud Detection  
[![Python](https://img.shields.io/badge/Python-3.8%2B-blue.svg)](https://www.python.org/)  
[![Scikit-learn](https://img.shields.io/badge/ML-ScikitLearn-orange)](https://scikit-learn.org/)  
[![Imbalanced-learn](https://img.shields.io/badge/ImbalancedLearn-SMOTE-green)](https://imbalanced-learn.org/)  

---

## 📌 Project Overview
Credit card fraud detection is a **highly imbalanced classification problem**. The goal of this project is to detect fraudulent transactions using machine learning techniques.  
We implemented **Logistic Regression** and **Random Forest** models, handled class imbalance using **SMOTE**, and evaluated performance using metrics suitable for imbalanced data.

---

## ✅ Dataset
- **Source:** [Kaggle - Credit Card Fraud Detection](https://www.kaggle.com/datasets/mlg-ulb/creditcardfraud)
- **Size:** 284,807 transactions  
- **Fraud cases:** 492 (~0.17%)  
- **Features:** V1–V28 (PCA components), Time, Amount  
- **Target:** `Class` (0 = Non-Fraud, 1 = Fraud)

---

## 🛠 Technologies Used
- **Python 3.8+**
- **Libraries:**
  - `pandas`, `numpy`
  - `matplotlib`, `seaborn`
  - `scikit-learn`
  - `imbalanced-learn` (SMOTE)
  - `joblib`

---

## 🔍 Methodology
1. **Data Cleaning & Scaling**
   - Remove nulls, scale `Time` and `Amount`
2. **Handling Imbalance**
   - Apply **SMOTE** to oversample minority class
3. **Model Training**
   - Logistic Regression (baseline)
   - Random Forest (tuned)
4. **Hyperparameter Tuning**
   - Used **RandomizedSearchCV** for Random Forest
5. **Evaluation**
   - Metrics: Precision, Recall, F1-score, ROC-AUC
   - Visuals: Confusion Matrix, ROC Curve, PR Curve

---

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
````

---

## 🌐 Deployment (Optional)

You can deploy this as a **Streamlit app** for real-time predictions:

```bash
streamlit run fraud_app.py
```

---

## 📂 Project Structure

```
├── creditcard.csv                # Dataset
├── CreditCardFraudDetection.ipynb# Main Notebook
├── fraud_detection_model.pkl      # Trained Model
├── scaler.pkl                     # Saved Scaler
├── fraud_app.py                   # Streamlit App
├── requirements.txt               # Dependencies
└── README.md                      # Documentation
```

---

![Preview Image](preview.png)
*(Add a screenshot of your notebook or Streamlit app here)*

---

```

---

### ✅ 2. **requirements.txt**
Save this as `requirements.txt`:

```

pandas
numpy
scikit-learn
imbalanced-learn
matplotlib
seaborn
joblib
streamlit

```
