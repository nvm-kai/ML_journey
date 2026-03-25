## Day 2 — Logistic Regression

### Dataset
- **Breast Cancer Dataset** (built into sklearn)
- 569 patients, 30 features
- Task: predict malignant vs benign (yes/no)

- **Titanic Dataset** (seaborn)
- 891 passengers, 8 features (after cleaning)
- Task: predict survival (survived=1, died=0)

### Model
- Logistic Regression (sklearn)

### Metrics
| Metric    | Breast Cancer | Titanic |
|-----------|--------------|---------|
| Accuracy  | 97.37%       | 79.89%  |
| Precision | 97.22%       | 77.14%  |
| Recall    | 98.59%       | 72.97%  |
| F1 Score  | 97.90%       | 75.00%  |

### What I Learned
- Logistic regression predicts yes/no (classification)
- Sigmoid function squeezes output between 0 and 1
- Decision boundary — probability > 0.5 = YES, < 0.5 = NO
- Confusion matrix — TP, TN, FP, FN
- Accuracy is misleading on imbalanced datasets
- Precision = when I say YES how often am I right?
- Recall = out of all actual YES how many did I catch?
- F1 = balance between precision and recall
- OneHotEncoding with ColumnTransformer
- Handling missing values
- Feature selection
- Data visualization with matplotlib

---

## Key Takeaways So Far
```
Regression  → predict a number  → use MAE, MSE, R²
Classification → predict yes/no → use Accuracy, Precision, Recall, F1
```

---

## Tech Stack
- Python 3
- scikit-learn
- pandas
- numpy
- matplotlib
- seaborn!

