# AI and Regression Refresher

A hands-on refresher on linear and polynomial regression, implemented **from scratch** using only **NumPy** and **Matplotlib**. No machine-learning libraries are used for the models: prediction, cost, gradients, and gradient descent are all written by hand.

The goal is to understand *how a regression model actually learns from data* — not just how to call a library.

## Main project

**`stellar_luminosity_hands_on.ipynb`** — Linear and polynomial regression applied to stellar **mass vs luminosity**.

The notebook walks through the full process:

1. Load and explore the data (mass vs luminosity).
2. Implement the learning algorithm from first principles (vectorized, works for one or more features).
3. Train a **linear model** and show that it underfits the curvature of the data.
4. Train a **polynomial model** (adding a `mass²` feature) and compare the fit.
5. Compare both models through their residuals and final cost.
6. Test the models inside and outside the training range to see where they can and cannot be trusted (interpolation vs extrapolation).
7. A short reflection on what this experiment does and does not reveal about how modern AI learns.

Key idea: polynomial regression is just linear regression on engineered features — the learning algorithm stays exactly the same, only the representation changes.



## Concepts covered

- Linear regression model: `ŷ = Xw + b`
- Mean squared error cost function: `J(w,b) = (1/2m) · Σ (ŷ − y)²`
- Gradient descent (batch)
- Vectorization with NumPy
- Feature scaling / standardization
- Feature engineering and polynomial features
- Underfitting, residual analysis, and the limits of extrapolation

## Requirements

- Python 3.12+
- NumPy
- Matplotlib
- Jupyter (Notebook or Lab)

Install the dependencies with:

```bash
pip install numpy matplotlib jupyter
```

## How to run

Open the notebooks with Jupyter:

```bash
jupyter notebook
```

Then open `stellar_luminosity_hands_on.ipynb` and run the cells in order.

## Project structure

```
.
├── README.md
├── stellar_luminosity_hands_on.ipynb                         # Main project
├── 01-week1_lab_notebook_1_one_feature_linear_regression_no_vectorization.ipynb
├── 02-week1_vectorization.ipynb
├── 03-week1_lab_notebook_1_one_feature_linear_regression_with_vectorization.ipynb
└── 04-week1_lab_notebook_2_multifeature_house_prices.ipynb
```
