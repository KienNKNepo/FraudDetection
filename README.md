# Financial Statement Fraud Detection

A machine learning-based system to detect fraudulent financial statements using multi-metric voting, data preprocessing, feature engineering, and various supervised learning models.

---

## 📂 Project Structure

| File/Folder     | Description                                      |
|-----------------|--------------------------------------------------|
| `code.ipynb`    | Full Jupyter Notebook with data processing, modeling, and evaluation |
| `raw_data_101/`         | Raw datasets                       |
| `README.md`     | Project overview and usage instructions          |
| `report.pdf`    | Full written report with analysis, insights, and results |

---

## **Problem Statement**
The goal is to build a classifier that can distinguish between fraudulent and non-fraudulent financial statements based on both financial ratios and statistical indicators, combining multiple fraud detection metrics with machine learning techniques.

---

## **Dataset Overview**
- **Columns:** Various financial ratios and key metrics extracted from financial statements.  
- **Target:** Fraudulent (1) or Non-Fraudulent (0).  
- **Fraud Labels:** Assigned using a voting mechanism of:
  1. Net Income Difference (pre- vs. post-audit),
  2. Auditor's Opinion,
  3. Mahalanobis Distance.

---

## **Data Cleaning & Preprocessing**
- Remove irrelevant features and handle missing values.
- Calculate Mahalanobis distance for outlier detection.
- Generate fraud labels based on metric voting.
- Standardize features using `StandardScaler`.

---

## **Exploratory Data Analysis (EDA)**
**Key Insights:**
- Fraudulent companies tend to show abnormal financial ratios and greater discrepancies between pre- and post-audit profits.
- Some features like **Profit_diff, ROA, Cash Flow** have significant separation between fraud and non-fraud classes.

---

## **Models Implemented**
Several supervised learning models were trained and evaluated:
- Logistic Regression
- Decision Tree
- Random Forest
- Naive Bayes
- K-Nearest Neighbors (KNN)
- SVM - Linear Kernel
- SVM - Sigmoid Kernel
- Neural Network (ANN)
- XGBoost

---

## **Model Performance**
| Classifier            | Accuracy | Precision | Recall  | F1-Score |
|-----------------------|----------|-----------|---------|----------|
| Logistic Regression   | 0.7642   | 0.7734    | 0.7642  | 0.6979   |
| k-Nearest Neighbors   | 0.7968   | 0.7843    | 0.7968  | 0.7772   |
| Naive Bayes           | 0.7895   | 0.8143    | 0.7895  | 0.7393   |
| SVM - Linear Kernel   | 0.7463   | 0.8114    | 0.7463  | 0.6488   |
| SVM - Sigmoid Kernel  | 0.6358   | 0.6225    | 0.6358  | 0.6287   |
| Decision Tree         | 0.8474   | 0.8472    | 0.8474  | 0.8473   |
| Random Forest         | 0.9084   | 0.9103    | 0.9084  | 0.9040   |
| Neural Network (ANN)  | 0.8726   | 0.8696    | 0.8726  | 0.8702   |
| XGBoost               | 0.9011   | 0.8996    | 0.9011  | 0.8980   |

**Best performer:** Random Forest – strong balance of precision and recall.

---

## **Evaluation Metrics**
- **Accuracy:** Overall correctness of predictions.
- **Precision:** How many predicted frauds were actually fraud.
- **Recall:** How many real fraud cases were detected.
- **F1-score:** Balance between precision and recall.

---

## **Practical Applications**
- Deploy Random Forest or XGBoost as real-time fraud detection tools for auditors and regulators.
- Integrate the model into financial monitoring systems (e.g., FiinPro-X) for continuous anomaly detection.
- Use feature importance to guide audit focus (e.g., profit difference, ROA, leverage).
- Extend the framework to other markets with retraining and threshold adjustments.
---

## **License**
Distributed under the MIT License.
