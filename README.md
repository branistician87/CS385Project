# Predicting MLB Player ROTO Scores Using Statistical Analysis & Machine Learning  
**CS385 — Baseball Data Modeling Project**

## 📌 Overview
This project provides a comprehensive analysis of Major League Baseball (MLB) player performance using a combination of exploratory statistics and machine learning. Using the **bat2022** dataset—containing detailed player performance metrics—we developed predictive models to estimate a player's **ROTO score**, a key fantasy baseball performance indicator.

We focused on performance metrics such as **stolen bases (SB), at-bats (AB), home runs (HR),** and **hits (H)** to identify their predictive power and evaluate players across positions.

---

## 📊 Dataset
The analysis utilized the **bat2022** dataset, containing diverse performance metrics for MLB players.  
Initial exploration revealed:

- **Average games played:** 72.55  
- **MLB qualification rules applied:**  
  - Using MLB Rules **9.22** and **10.22**, a minimum of **223 at-bats** was required to qualify.
- A filtered dataset, **`minatbats`**, was created to ensure all players met official MLB batting qualifications.

---

## 🔍 Exploratory Data Analysis (EDA)

### ✔ Correlation Analysis  
A correlation matrix and heatmap revealed strong relationships between:
- **ROTO ↔ RBI**
- **ROTO ↔ Hits (H)**  

These insights helped identify which metrics carry the strongest predictive signal.

### ✔ Positional Performance Patterns  
A scatterplot matrix was used to compare performance metrics across player positions.  
This visualization helped us understand how positional roles influence:

- Power metrics  
- Contact rates  
- Speed/stolen base contributions  

---

## 🤖 Machine Learning Models

### **1️⃣ Linear Regression (Baseline Model)**
- Train/test split used for initial evaluation  
- **R² = 0.987**  
- Excellent predictive capability on test data  

### **2️⃣ Cross-Validation**
- 5-fold cross-validation confirmed model generalizability  
- Mean CV score closely matched original R² value  

### **3️⃣ Ridge Regression**
- Tested to reduce potential multicollinearity effects  
- Performance nearly identical to baseline linear regression  

---

## 🏆 Key Findings
- Stolen bases (SB), at-bats (AB), home runs (HR), and hits (H) are **strong predictors of ROTO score**.
- Linear regression performed exceptionally well with:
  - **High accuracy**
  - **Strong generalization**
  - **Minimal overfitting**
- Ridge regression did not significantly improve accuracy, suggesting simple linear relationships capture most variance.

---

## 🚀 Future Work
Potential enhancements include:
- Incorporating advanced sabermetrics (e.g., wOBA, OPS+, WAR)  
- Evaluating non-linear models (Random Forest, XGBoost)  
- Integrating injury history or team-level context  
- Deploying as an interactive dashboard (Tableau/Streamlit)

---

## 🛠 Tools & Technologies
- Python  
- pandas, NumPy  
- Matplotlib / Seaborn  
- Scikit-learn  
- Jupyter Notebook  
- Statistical modeling & regression analysis  

---

## 📁 Repository Structure
