Aşağıda, projenizi tanıtan ve GitHub deposu için uygun bir `README.md` dosyası örneği yer almaktadır:

---

# 🏦 Polish Company Bankruptcy Prediction using Machine Learning

This project focuses on predicting the bankruptcy of Polish companies using machine learning techniques applied to historical financial data. The aim is to help investors, analysts, and policymakers detect early warning signs of financial distress.

## 📁 Dataset

* **Name**: Polish Companies Bankruptcy Data
* **Source**: [UCI Machine Learning Repository](https://archive.ics.uci.edu/dataset/365/polish+companies+bankruptcy+data)
* **Instances**: \~10,000
* **Features**: 64 numerical financial indicators
* **Target Variable**: Binary classification

  * `1`: Bankrupt
  * `0`: Not Bankrupt

## 🎯 Problem Statement

We aim to build a model that can predict whether a company will go bankrupt within 1 to 5 years based on its financial ratios from a specific year. This can be used for:

* Risk management
* Financial health assessment
* Strategic planning

## ⚙️ Preprocessing & Modeling Steps

* **Data Cleaning**: Handled missing values using mean imputation
* **Scaling**: StandardScaler (Z-score normalization)
* **Class Imbalance Handling**: SMOTE (Synthetic Minority Oversampling Technique)
* **Model Evaluation**: Stratified 5-fold Cross-Validation

## 🧠 Models Evaluated

| Model                   | F1-Score (Class 1) |
| ----------------------- | ------------------ |
| Random Forest           | 0.57               |
| XGBoost                 | 0.73               |
| LightGBM                | 0.65               |
| **CatBoost (Selected)** | **0.76**           |
| Logistic Regression     | 0.17               |
| SVM                     | 0.17               |

**Final model**: `CatBoostClassifier`
**Tuning method**: [Optuna](https://optuna.org/)
**Best F1-Score**: 0.7606 (for bankrupt class)

## 🧪 Explainability

We applied model explainability techniques to understand and verify the model’s predictions:

* **LIME** (Local Interpretable Model-Agnostic Explanations)
* **Permutation Importance**
* **Partial Dependence Plots (PDP)**

These tools help uncover which financial features most influence the prediction of bankruptcy, both globally and on individual samples.

## 📊 Key Features Influencing Bankruptcy

* A27: Accounts Receivable / Sales
* A60: Total Liabilities / Total Assets
* A61: Short-Term Liabilities / Total Assets

## 👥 Team Members

* Mert Koçoğlu (14533043564)
* Yaşar Düzgün (39599212730)

## 📚 References

* UCI ML Repository: [Polish Bankruptcy Dataset](https://archive.ics.uci.edu/dataset/365/polish+companies+bankruptcy+data)
* CatBoost Documentation: [catboost.ai](https://catboost.ai)
* Optuna: [optuna.org](https://optuna.org)

---

İsterseniz README’ye kurulum talimatları, kullanım örnekleri veya görseller de ekleyebilirim. İhtiyacınıza göre özelleştirebiliriz.
