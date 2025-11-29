# 🚢 Titanic Survival Prediction — Logistic Regression

This project builds an interpretable **Logistic Regression** model to predict which passengers survived the Titanic disaster.  
Using demographic, socio-economic, and travel-related features, the model uncovers survival determinants while providing strong predictive performance.

---

## 📌 Project Objective
The primary goal is to predict passenger survival (`Survived = 1 or 0`) using features such as:

- Sex  
- Age  
- Passenger Class (Pclass)  
- Fare  
- Siblings/Spouses aboard (SibSp)  
- Parents/Children aboard (Parch)  
- Embarkation Port  
- Family size & socio-economic indicators  

Logistic Regression is chosen for its transparency, interpretability, and suitability for binary classification.

---

## 📁 Dataset Details

- **Source:** Titanic Dataset (Kaggle)  
- **Samples:** 891 rows  
- **Features:** 11 usable predictors after cleaning  
- **Target:** `Survived` (0 = No, 1 = Yes)

### Key Predictors
- Sex  
- Pclass  
- Age  
- Fare  
- SibSp  
- Parch  
- Embarked  

### Preprocessing Performed
- Missing values handled (Age median imputation, Embarked mode fill)  
- Dropped non-informative fields: PassengerId, Name, Ticket, Cabin  
- One-hot encoding for categorical variables  
- StandardScaler on Age and Fare  
- Train-test split (80/20)  

---

## 🔍 Exploratory Data Analysis — Summary

### **Class Distribution**
- ~38% survived → moderate imbalance  

### **Major Patterns**
- **Sex:** Females had significantly higher survival probability  
- **Pclass:** First-class > Second-class > Third-class  
- **Fare:** Higher fare → higher survival odds  
- **Age:** Younger passengers survived at higher rates  
- **Family Features:** Small family groups slightly improved survival chances  

### **Core Insights**
- Social and economic factors strongly influenced outcomes  
- Wealthier and female passengers had clear advantages  
- Fare correlates positively with survival while Pclass correlates negatively  

---

## 🧠 Model Summary

### Algorithm Used:
- **Logistic Regression** with scaled features  
- **Solver:** lbfgs  
- **Regularization:** default  
- **One-hot encoded categorical fields**

---

## 🎯 Model Performance

| Metric | Score |
|--------|--------|
| **Accuracy** | 0.80 |
| **Precision (Survived)** | 0.76 |
| **Recall (Survived)** | 0.71 |
| **F1-score (Survived)** | 0.74 |
| **ROC-AUC** | 0.86 |
| **PR-AUC** | 0.85 |

### Interpretation
- Strong ability to distinguish survivors from non-survivors  
- Good balance between precision & recall  
- ROC-AUC 0.86 indicates reliable generalization  

---

## 🧪 Learning & Validation Curves
- Training and validation accuracy converge around 0.80  
- Low variance, minimal overfitting  
- Model generalizes well without excessive complexity  

---

## ⭐ Feature Importance (Coefficients & Analysis)

Most influential predictors:

1. **Sex (female)** → strongest positive effect on survival  
2. **Fare** → higher fare passengers survived more  
3. **Pclass** → lower class passengers had lower odds  
4. **Age** → younger passengers slightly more likely to survive  

Embarked and family-related features showed moderate or subtle influence.

---

## 💡 Key Insights

- Survival followed stark socio-economic and gender patterns  
- Females and first-class passengers had the highest survival chances  
- Higher fare values reflected priority access to rescue  
- Simple linear models can still capture real-world behavioral patterns effectively  

---

## 📦 Summary Table

| Item | Value |
|------|--------|
| Dataset | Titanic Passenger Dataset |
| Target | Survived |
| Best Model | Logistic Regression |
| Accuracy | 0.80 |
| ROC-AUC | 0.86 |
| PR-AUC | 0.85 |
| Dominant Features | Sex, Fare, Pclass, Age |
| Data Size | 891 records |

---

## 🧱 Tech Stack
- Python  
- Pandas, NumPy  
- Matplotlib, Seaborn  
- Scikit-learn  
- Statsmodels  
- Jupyter / Google Colab  
