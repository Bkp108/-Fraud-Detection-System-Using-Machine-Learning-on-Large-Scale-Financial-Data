# 💼 Fraud Detection System using Machine Learning

A complete end-to-end machine learning project to detect fraudulent financial transactions using real-world data (~6.3M+ records). This project was developed as part of a Data Science Internship Assignment with XYZ.

---

## 📊 Project Objective

To build a robust and explainable fraud detection model that:

- Accurately identifies fraudulent transactions
- Provides clear business insights using EDA
- Recommends infrastructure-level fraud prevention strategies

---

## 📌 Dataset

The dataset contains 6.3 million+ financial transactions with features like:

- Transaction type (PAYMENT, TRANSFER, CASH_OUT)
- Amount, balances before/after
- Fraud label (`isFraud`)

> 🔹 `isFraud = 1` → Fraudulent transaction  
> 🔹 `isFraud = 0` → Genuine transaction

---

## ⚙️ Steps Performed

### 1. Data Cleaning & Feature Engineering

- Removed ID and redundant columns
- Engineered key features:
  - `diffOrig`, `diffDest`, zero-balance flags
- Handled class imbalance with sampling

### 2. Exploratory Data Analysis (EDA)

- Class distribution
- Transaction amount histograms
- Feature correlation heatmaps

### 3. Model Building

- **Random Forest Classifier** (tuned: 200 trees, balanced weights)
- Evaluated via:
  - Classification Report
  - Confusion Matrix
  - ROC AUC Score (~**0.999**)

---

## 📈 Results

- **ROC AUC:** 0.9992
- **Precision on Fraud Class:** 93%
- **F1 Score (Fraud):** 0.79
- Strong performance with clear separation of fraudulent behavior patterns

---

## 🔐 Key Business Insights

- Fraud occurs mainly through **TRANSFER** and **CASH_OUT** types
- Most fraudulent transactions drain accounts to **zero**
- SHAP shows **amount** and **origin balance** are crucial flags

---

## 🛡️ Fraud Prevention Recommendations

- Real-time scoring with ML API
- Alerts on zero-balance drains or high-risk transfers
- Dynamic 2FA for flagged transactions
- Monthly retraining to keep up with fraud patterns

---

## 📁 Files Included

| File                    | Description                                      |
| ----------------------- | ------------------------------------------------ |
| `fraud_detection.ipynb` | Main notebook (EDA, modeling, SHAP, LazyPredict) |
| `fraud.csv`             | Dataset (not provided here)                      |
| `README.md`             | Project documentation                            |
| `*.png`                 | Visuals: plots, confusion matrix, ROC curve      |

---

## 🧠 Tools & Libraries

- Python (Pandas, NumPy, Matplotlib, Seaborn)
- Scikit-learn

---

## 👨‍💻 Author

**Brijesh Kishore Purohit**  
📧 [brijeshkpurohit04@gmail.com]

---

## 📌 License

This project is open-source and available for educational use.
