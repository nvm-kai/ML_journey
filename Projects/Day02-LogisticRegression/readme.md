# 🚢 Titanic Survival Prediction (Machine Learning Project)

## 📌 Overview

This project predicts whether a passenger survived the Titanic disaster using machine learning.
It uses the famous Titanic dataset and applies data preprocessing, feature engineering, and a Logistic Regression model to make predictions.

---

## 🎯 Objective

To build a classification model that can predict passenger survival based on features like:

* Age
* Sex
* Passenger Class
* Fare
* Embarked location

---

## 📊 Dataset

* Source: Seaborn built-in Titanic dataset
* Total samples: 891
* Target variable: `survived` (0 = Died, 1 = Survived)

---

## 🛠️ Technologies Used

* Python
* NumPy
* Pandas
* Seaborn
* Matplotlib
* Scikit-learn

---

## ⚙️ Data Preprocessing

* Filled missing values:

  * `age` → median
  * `embarked` → mode
* Dropped irrelevant columns:

  * `deck`, `embark_town`, `alive`, `who`, `class`, `adult_male`, `alone`
* Encoding:

  * One-hot encoding for `sex`
  * Manual mapping for `embarked`
* Feature scaling using `StandardScaler`

---

## 🤖 Model

* Algorithm: Logistic Regression
* Train-Test Split: 80% training / 20% testing

---

## 📈 Evaluation Metrics

The model was evaluated using:

* Accuracy
* Precision
* Recall
* F1 Score
* Confusion Matrix


---

## 📊 Visualizations

### 1. Survival Distribution

* Comparison of total passengers who survived vs died

### 2. Gender-Based Survival Analysis

* Male vs Female survival comparison
* Key insight:

  * Females had significantly higher survival rates than males

---

## 🔍 Key Insights

* Gender is a strong predictor of survival
* Passengers in higher classes had better survival chances
* Younger passengers had slightly higher survival rates

---

## 🚀 Tools used for this :

```
pip install numpy pandas seaborn matplotlib scikit-learn

```


## 🧠 Future Improvements

* Try advanced models (Random Forest, XGBoost)
* Perform hyperparameter tuning
* Add cross-validation
* Deploy as a web app

---

## 🙌 Author

**Satya**

* Linked in : https://www.linkedin.com/in/psatyashry24
* GitHub : https://github.com/nvm-kai

---

## ⭐ If you found this useful, give it a star!
