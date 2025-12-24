# Linear Regression and Regularization Techniques Project

## Project Overview

This project demonstrates the implementation of **Linear Regression**, **Ridge Regression**, **Lasso Regression**, and **ElasticNet Regression** using Python. Two datasets are used:

1. **Student Performance Dataset** - For Linear Regression.
2. **Boston Housing Dataset** - For Ridge, Lasso, and ElasticNet Regression.

The goal of this project is to:

* Understand and implement Linear Regression.
* Explore regularization techniques (Ridge, Lasso, ElasticNet) and their impact on model performance.
* Compare models using regression metrics such as **R²**, **RMSE**

---

## Project Structure

The project follows a modular structure:

```
Linear_regression/
│
├── datasets/                  # Contains datasets
│   ├── student_performance.csv
│   └── boston_housing.csv
│
├── linear_regression.ipynb
└── ridge_lasso_and_elasticnet_regresso.ipynb
```

---

## Linear Regression

Linear Regression is a fundamental supervised learning algorithm used for **predicting a continuous target variable** based on one or more features. The model assumes a linear relationship between the input variables (X) and the target variable (y):

[
y = \beta_0 + \beta_1 x_1 + \beta_2 x_2 + ... + \beta_n x_n + \epsilon
]

Key points:

* Minimized using **Mean Squared Error (MSE)**.
* Provides **coefficients** to understand feature impact.
* Implemented on the **Student Performance Dataset** to predict student scores.

**Metrics used:** R², RMSE.

---

## Ridge Regression (L2 Regularization)

Ridge Regression is a **regularized version of Linear Regression** that adds an **L2 penalty** to the loss function:

[
Loss = MSE + \alpha \sum \beta^2
]

**Purpose:**

* Reduces **overfitting** by shrinking coefficients.
* Handles **multicollinearity** in datasets.

**Hyperparameter:**

* `alpha` controls regularization strength.

**Implemented on:** Boston Housing Dataset.

---

## Lasso Regression (L1 Regularization)

Lasso Regression adds an **L1 penalty** to the loss function:

[
Loss = MSE + \alpha \sum \|beta|
]

**Purpose:**

* Performs **feature selection** by setting some coefficients to zero.
* Helps simplify models and reduce irrelevant features.

**Hyperparameter:**

* `alpha` controls regularization strength.

**Implemented on:** Boston Housing Dataset.

---

## ElasticNet Regression

ElasticNet combines **Ridge (L2)** and **Lasso (L1)** penalties:

[
Loss = MSE + \alpha (\rho \sum |\beta| + (1-\rho) \sum \beta^2)
]

**Purpose:**

* Handles **correlated features** more effectively than Lasso.
* Performs **shrinkage** (like Ridge) and **feature selection** (like Lasso).

**Hyperparameters:**

* `alpha` → overall regularization strength
* `l1_ratio` → balance between L1 and L2 penalties (0 = Ridge, 1 = Lasso)

**Implemented on:** Boston Housing Dataset.

---

## Key Takeaways

* Linear Regression works well for simple datasets but can **overfit** with correlated or high-dimensional features.
* Ridge Regression reduces overfitting and handles multicollinearity.
* Lasso Regression performs feature selection by eliminating irrelevant features.
* ElasticNet balances Ridge and Lasso, providing **shrinkage and sparsity** simultaneously.

---

## Author

**Nishant Chandra Verma**
