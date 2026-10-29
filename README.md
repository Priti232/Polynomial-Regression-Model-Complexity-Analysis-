# Polynomial Regression & Model Complexity Analysis

## Overview

This project demonstrates how polynomial degree affects a regression model's fit and how Ridge regularization can be explored to help control overfitting. The notebook creates a noisy sine-wave dataset, trains polynomial regression models, compares training and testing Mean Squared Error (MSE), and plots each fitted model.

## Objectives

- Explore Polynomial Regression using different polynomial degrees.
- Compare a simple model with more complex models.
- Observe training and testing errors.
- Explore Ridge regularization on a high-degree polynomial model.
- Visualize the fitted regression curves.

## Technologies Used

- Python
- NumPy
- Matplotlib
- scikit-learn
- Google Colab / Jupyter Notebook

## Dataset

The notebook generates a synthetic dataset with 100 points:

- **Input (`X`):** Values evenly spaced between -3 and 3.
- **Target (`y`):** `sin(X)` with added random noise.

The data is split into training and testing sets, with 30% reserved for testing.

## Experiments

The notebook runs these experiments:

1. **Degree 1:** A simple model, used to illustrate underfitting.
2. **Degree 4:** A more flexible model intended to fit the underlying pattern.
3. **Degree 15:** A highly complex model used to illustrate potential overfitting.
4. **Degree 15 with Ridge:** Applies Ridge regularization (`alpha=1.0`) to the degree-15 model.

For each experiment, the notebook prints training and testing Mean Squared Error (MSE) and plots the fitted curve alongside the dataset.

> Note: Actual error values and how clearly each model demonstrates underfitting or overfitting depend on the train-test split and execution. Run the notebook to see the results.

## How to Run

### Option 1: Google Colab

1. Open the `.ipynb` notebook in Google Colab.
2. Run the cells from top to bottom, or select **Runtime → Run all**.
3. Review the printed training/testing errors and plots.

### Option 2: Run locally

Install the required packages:

```bash
pip install numpy matplotlib scikit-learn jupyter
```

Then open the notebook in Jupyter Notebook or JupyterLab and run all cells.

## Project Structure

```text
Polynomial-Regression-Model-Complexity-Analysis/
├── Polynomial_Regression_&_Model_Complexity_Analysis.ipynb
└── README.md
```

## Key Concepts

- **Polynomial Regression:** Adds polynomial features so a linear regression model can represent curved relationships.
- **Model Complexity:** Describes how flexible a model is in fitting patterns in data.
- **Underfitting:** When a model is too simple to capture the pattern well.
- **Overfitting:** When a model fits the training data too closely and generalizes poorly to unseen data.
- **Ridge Regression:** Adds an L2 penalty to the regression objective to discourage excessively large coefficients.
- **Mean Squared Error (MSE):** Measures the average squared difference between actual and predicted values; lower values indicate smaller errors on that dataset.

## Future Improvements

- Set a fixed `random_state` in `train_test_split` for reproducible results.
- Compare more polynomial degrees and Ridge `alpha` values.
- Add a summary table comparing training and testing MSE.
- Improve plot labels and include a legend.

## Project Status

Educational machine learning project for exploring polynomial regression, model complexity, and regularization.
