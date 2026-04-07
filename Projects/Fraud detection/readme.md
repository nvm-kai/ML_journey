📌 Overview

Financial fraud is a major challenge in digital transactions. This project builds a robust fraud detection system using XGBoost and engineered features to identify suspicious activities with high precision and recall.

📊 Dataset
Link : https://drive.google.com/file/d/11J7s35t1ei7wTgQiby09XrqqCOtZJSFG/view?usp=sharing
Size: 6,362,620 transactions
Features: 11 original columns
Target Variable: isFraud
Key Columns:
step – Time step
type – Transaction type (PAYMENT, TRANSFER, CASH_OUT, etc.)
amount – Transaction amount
oldbalanceOrg, newbalanceOrig – Sender balance
oldbalanceDest, newbalanceDest – Receiver balance
isFraud – Fraud label (0 = No, 1 = Yes)

🔍 Exploratory Data Analysis (EDA)
Key Insights:
Fraud cases are extremely imbalanced (~0.13%)
Fraud occurs only in:
TRANSFER
CASH_OUT
Large transactions and balance inconsistencies are strong fraud indicators

🧹 Data Cleaning
No missing values
Outliers detected using IQR (~5.31%)
Outliers retained (important fraud signals)

⚙️ Feature Engineering

Created meaningful features to capture fraud patterns:

errorBalanceOrig → Balance mismatch (sender)
errorBalanceDest → Balance mismatch (receiver)
balanceOrigRatio → Amount vs original balance
isHighAmount → High-value transaction flag
type_encoded → Encoded transaction type
isTransferOrCashOut → Fraud-prone transaction types

🤖 Model
Algorithm Used:
XGBoost Classifier
Train-Test Split:
80% Training
20% Testing (Stratified)

📈 Model Performance
Metric	Score
Accuracy	99.99%
ROC-AUC	0.9886
Precision	0.95
Recall	0.95
F1-score	0.95

⚠️ Reality Check
Accuracy is misleading due to class imbalance — focus on:
Recall (Fraud Detection Rate)
Precision (False Alarm Control)

🔑 Feature Importance
Top predictors:
oldbalanceOrg
newbalanceOrig
errorBalanceDest
balanceOrigRatio
errorBalanceOrig
isTransferOrCashOut
Interpretation:
Fraud often involves balance inconsistencies
Fraudsters tend to drain accounts completely
Suspicious activity mostly occurs in TRANSFER & CASH_OUT

🛡️ Fraud Prevention Strategies
Recommended Actions:
Require OTP/Biometric for high-value transactions
Limit multiple large transactions in short time
Real-time customer alerts
Monitor unusual balance behavior

📊 Evaluation Strategy

To measure real-world effectiveness:

Track fraud count before vs after deployment
Monitor False Positives (FP)
Maintain Recall > 90%
Analyze customer complaints

🧠 Key Learnings
Feature engineering matters more than model choice
Imbalanced data requires careful evaluation
Domain understanding is critical in fraud detection
High accuracy ≠ good model

🚀 Tech Stack
Python
Pandas, NumPy
Matplotlib, Seaborn
Scikit-learn
XGBoost

📂 Project Structure
├── Fraud.csv
├── fraud_detection.ipynb
├── README.md
📌 Conclusion

This model successfully captures real-world fraud patterns and achieves strong performance using engineered features and XGBoost. However, production systems should further focus on reducing false positives and improving real-time detection.