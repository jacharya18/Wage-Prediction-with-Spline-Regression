---

# 📈 Wage Prediction Using Spline Regression
# Author: Jai Acharya
📋 **Table of Contents**

1. 🤖 Introduction
2. ⚙️ Tech Stack
3. 🔬 Methodology
4. 📊 Results
5. 💡 Key Insights
6. 🧠 Interpretation
7. 🔋 Features & Highlights
8. 🔗 Links & Resources
9. 🚀 Future Improvements
10. 🧾 Author

---

## 🤖 Introduction

**Wage Prediction Using Spline Regression** is a data science project focused on modeling the nonlinear relationship between **age** and **wage** using **spline regression techniques**.

The goal is to demonstrate how flexible regression models (linear and cubic splines) can uncover meaningful trends beyond simple linear fits — while also proving mastery of model evaluation, bias–variance trade-offs, and generalization performance.

This project forms part of a broader portfolio showcasing **machine learning applications for economic and social data**. It highlights analytical rigor, reproducible workflow, and clear business interpretation.

---

## ⚙️ Tech Stack

* 🐍 **Python 3.10+**
* 📦 **pandas** – Data handling and preprocessing
* 📉 **statsmodels** – OLS regression and statistical diagnostics
* 📊 **matplotlib** – Visualization and curve plotting
* 🔢 **NumPy** – Numerical computation
* 🧮 **Jupyter Notebook** – Interactive analysis environment

---

## 🔬 Methodology

**Objective:** Predict wages as a function of age, accounting for potential nonlinear effects.

**Workflow Overview:**

1. **Data Preparation:**

   * Loaded and cleaned wage dataset (`wages.csv`).
   * Split first 50% of rows for training and remaining 50% for testing (per assignment spec).

2. **Model Construction:**

   * Implemented **Linear** and **Cubic Spline** bases manually using truncated power functions.
   * Evaluated two knot configurations:

     * `[30, 60]`
     * `[20, 30, 40, 50, 60]`

3. **Model Fitting:**

   * Used **OLS regression** via `statsmodels`.
   * Estimated parameters, R², and computed **test MSE** for generalization.

4. **Evaluation & Visualization:**

   * Compared spline types and knot sets on both fit quality and predictive accuracy.
   * Plotted fitted curves vs. real data for interpretability.

---

## 📊 Results

| Knots            | Model Type    | Train R² | Test MSE    |
| ---------------- | ------------- | -------- | ----------- |
| [30, 60]         | Linear Spline | 0.0850   | **1553.81** |
| [30, 60]         | Cubic Spline  | 0.0933   | 1566.27     |
| [20,30,40,50,60] | Linear Spline | 0.0930   | 1557.83     |
| [20,30,40,50,60] | Cubic Spline  | 0.0944   | 1563.20     |

✅ **Best model:** Linear spline with knots at `[30, 60]` (lowest test MSE).

---

## 💡 Key Insights

* **Age explains <10% of wage variance** — clear evidence that wages depend more on experience, education, and occupation.
* **Cubic splines don’t outperform linear splines** — more flexibility increased R² but worsened test error → classic overfitting.
* **More knots ≠ better model** — finer grids added complexity with no predictive benefit.
* **Linear spline with [30,60] knots** provides smooth, interpretable wage-age trends without overfitting.

---

## 🧠 Interpretation

* Wage growth is **increasing with age** up to around 50, then plateaus — consistent with economic theory (human capital accumulation and diminishing returns).
* The **best model’s RMSE ≈ 39.5** (wage units), meaning typical prediction error is about $39 relative to true wage values — large enough to prove **age alone is insufficient**.
* The analysis reinforces that even statistically sound models can fail to explain social outcomes without richer contextual variables.

---

## 🔋 Features & Highlights

✅ Manual spline basis implementation (no prebuilt libraries)
✅ Linear vs. Cubic spline comparison
✅ Automated performance evaluation (R² & MSE)
✅ Visual inspection of fitted curves vs real data
✅ Clean separation of training and test data
✅ Fully reproducible Jupyter notebook workflow
✅ Professional README and GitHub structure
✅ Business-context interpretation of results

---

## 🔗 Links & Resources

* 📘 **Notebook:** [`Spline Regression for Wage Prediction.ipynb`](Spline%20Regression%20for%20Wage%20Prediction.ipynb)
* 📄 **Assignment Brief:** [`P2.pdf`](P2.pdf)
* 📊 **Results & Plots:** [`spline_outputs/`](spline_outputs/)
* 📚 **Key Libraries:**

  * [pandas Documentation](https://pandas.pydata.org/docs/)
  * [statsmodels Documentation](https://www.statsmodels.org/stable/index.html)
  * [Matplotlib Guide](https://matplotlib.org/stable/tutorials/index.html)

---

## 🚀 Future Improvements

* Add **education**, **experience**, and **occupation** predictors for multivariate modeling.
* Implement **B-splines** or **natural splines** for numerical stability.
* Extend evaluation with **k-fold cross-validation**.
* Benchmark against **tree-based models** (Random Forest, Gradient Boosting).
* Deploy as a small **Streamlit app** for interactive visualization.

---

## 🧾 Author

👤 **Jai Acharya**
📧 [[your.email@example.com](mailto:your.email@example.com)]
💼 [LinkedIn Profile or Portfolio URL]

---

### 🏁 Summary

A technically robust and business-aware regression project demonstrating:

* Mastery of nonlinear regression and model validation.
* Statistical reasoning tied to real-world interpretation.
* Professional-level presentation ready for hiring managers or client review.

> 🚀 *“In analytics, clarity is power — not just prediction.”*

---

