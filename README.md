# 📈 Wage Prediction Using Spline Regression
**Author:** Jai Acharya  

---

## 📋 Table of Contents
- 🤖 [Introduction](#-introduction)  
- ⚙️ [Tech Stack](#-tech-stack)  
- 🔬 [Methodology](#-methodology)  
- 📊 [Results](#-results)  
- 💡 [Key Insights](#-key-insights)  
- 🧠 [Interpretation](#-interpretation)  
- 🔋 [Features & Highlights](#-features--highlights)  
- 🔗 [Links & Resources](#-links--resources)  
- 🚀 [Future Improvements](#-future-improvements)  
- 🧾 [Author](#-author)  
- 🏁 [Summary](#-summary)  

---

## 🤖 Introduction

**Wage Prediction Using Spline Regression** is a data science project that models the **nonlinear relationship between age and wage** using spline regression techniques.  

The goal is to demonstrate how **flexible regression models** (linear and cubic splines) can uncover trends missed by standard linear models — while showcasing strong understanding of **bias–variance trade-offs**, **generalization**, and **statistical interpretation**.

This work is part of a broader portfolio in **Data Science for Business Decision Making**, highlighting analytical rigor, reproducibility, and business-focused storytelling.

---

## ⚙️ Tech Stack

- 🐍 **Python 3.10+**
- 📦 **pandas** – Data handling & preprocessing  
- 📉 **statsmodels** – OLS regression & statistical diagnostics  
- 📊 **matplotlib** – Visualization & curve plotting  
- 🔢 **NumPy** – Numerical computation  
- 🧮 **Jupyter Notebook** – Interactive analysis environment  

---

## 🔬 Methodology

### 🎯 Objective  
Predict individual wages as a function of **age**, capturing nonlinearities in the wage-age curve using **spline regression**.

### 🧩 Workflow Overview

#### 1. Data Preparation
- Loaded dataset: `wages.csv`
- Split evenly into training (estimation) and testing (validation) subsets.

#### 2. Model Construction
- Implemented **Linear** and **Cubic Splines** manually using truncated power basis functions.
- Evaluated two knot configurations:
  - `[30, 60]`
  - `[20, 30, 40, 50, 60]`

#### 3. Model Fitting
- Fitted all models using **OLS regression** (`statsmodels`).
- Computed **R²**, **Adjusted R²**, and **Test MSE** to assess accuracy and generalization.

#### 4. Evaluation & Visualization
- Compared model performance and stability.
- Plotted fitted spline curves against real wage data.

---

## 📊 Results

| Knots | Model Type | Train R² | Test MSE |
|--------|-------------|-----------|-----------|
| [30, 60] | Linear Spline | 0.0850 | **1553.81** |
| [30, 60] | Cubic Spline | 0.0933 | 1566.27 |
| [20, 30, 40, 50, 60] | Linear Spline | 0.0930 | 1557.83 |
| [20, 30, 40, 50, 60] | Cubic Spline | 0.0944 | 1563.20 |

✅ **Best Model:** *Linear spline with knots at [30, 60]* — lowest test MSE and most stable performance.

---

## 💡 Key Insights

- Age explains **less than 10%** of wage variance → other socioeconomic factors dominate.
- **Cubic splines** add flexibility but yield **no test improvement** → mild overfitting.
- **More knots ≠ better accuracy** — unnecessary complexity increased instability.
- **Linear spline (30, 60)** delivers the best trade-off between interpretability and fit.

---

## 🧠 Interpretation

- Wages **increase steadily** with age up to ~50, then **plateau**, consistent with labor economics (experience accumulation, diminishing returns).  
- The model’s **RMSE ≈ 39.5** indicates that **age alone** cannot fully predict wage levels — additional variables like **education** and **job class** are crucial.  
- The results show that even statistically robust methods can fail without **contextual, domain-relevant variables**.

---

## 🔋 Features & Highlights

✅ Manual spline basis implementation (no auto libraries)  
✅ Comparison of Linear vs. Cubic spline models  
✅ Automated performance evaluation (R², MSE)  
✅ Clean training/testing split for fair validation  
✅ High-quality data visualizations with `matplotlib`  
✅ Reproducible Jupyter Notebook workflow  
✅ Professional documentation and structure  
✅ Clear business interpretation of model behavior  

---

## 🔗 Links & Resources

📘 **Notebook:** `Spline Regression for Wage Prediction.ipynb`  
📄 **Assignment Brief:** `P2.pdf`  
📊 **Results & Plots:** `/spline_outputs/`  

**Key References:**
- [pandas Documentation](https://pandas.pydata.org/docs/)  
- [statsmodels Documentation](https://www.statsmodels.org/stable/index.html)  
- [Matplotlib User Guide](https://matplotlib.org/stable/users/index.html)  

---

## 🚀 Future Improvements

- Add **education**, **experience**, and **occupation** variables for multivariate modeling.  
- Explore **B-splines** or **natural splines** for numerical stability.  
- Integrate **k-fold cross-validation** to validate generalization robustness.  
- Benchmark against **tree-based regressors** (Random Forest, Gradient Boosting).  
- Build an **interactive Streamlit app** for visual model exploration.  

---

## 🧾 Author

👤 **Jai Acharya**  
📧 [jacharya@email.sc.edu]  
💼 [https://www.linkedin.com/in/jai-acharya/]  

---

## 🏁 Summary

A technically rigorous and business-aware regression analysis demonstrating:

- Mastery of nonlinear regression (splines) and model validation.  
- Strong statistical reasoning and interpretable modeling.  
- Professional communication and reproducible workflow.  

> 🚀 *“In analytics, clarity is power — not just prediction.”*
