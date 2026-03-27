# Loan Prediction System – Decision Tree

## Project Overview
This project predicts whether a person is eligible for a loan based on their personal and financial information. The goal is to minimize risky loan approvals (False Positives), ensuring banks approve loans responsibly.

---

## Dataset
- **Source:** Kaggle – Debetta Chatterage
- **Features:** Gender, Married, Dependents, Education, Self_Employed, ApplicantIncome, CoapplicantIncome, LoanAmount, Loan_Amount_Term, Credit_History, Property_Area, Loan_Status

---

## Steps Taken

### 1. Data Cleaning & Preprocessing
- Filled missing categorical features with mode
- Filled missing numerical features with median
- Dropped `Loan_ID` (non-predictive)

### 2. Feature Encoding
- One-Hot Encoding for multi-category features
- Label Encoding for binary features and target

### 3. Train/Test Split
- 80% train / 20% test
- Maintained class distribution with `stratify=y`

### 4. Model Building
- Trained Decision Tree Classifier
- Tuned `max_depth` for performance
- Experimented with `class_weight` and thresholds for reducing False Positives

### 5. Evaluation
- Metrics: Accuracy, Precision, Recall, F1-Score
- Focused on recall for risky applicants (class 0)
- Feature importance highlighted `Credit_History`, `CoapplicantIncome`, and `LoanAmount` as key predictors

---

## Key Insights
- Decision Tree can identify risky applicants effectively, though trade-offs exist between precision and recall.
- `Credit_History` is the most critical factor in loan approval.
- Business objective (minimizing false approvals) influenced model tuning decisions.

---

## Next Steps
- Explore Random Forest / Ensemble models for improved recall and stability
- Optimize thresholds to further reduce risky loan approvals
- Add cross-validation for more robust evaluation

---

## How to Run
1. Clone the repository
2. Install dependencies: `pip install pandas numpy scikit-learn matplotlib`
3. Open `Loan_Prediction_DecisionTree.ipynb`
4. Run cells sequentially