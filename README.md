# Energy Efficiency Modeling with Linear Regression and Lasso

This project models **building energy efficiency** based on building parameters, using statistical learning techniques to model heating and cooling loads. The notebook demonstrates the construction and implementation of models that balance computational efficiency with strong predictive performance through **linear regression and Lasso**.

---

## Overview

- **Objective**: Predict energy efficiency (heating and cooling loads) from building features.
- **Approach**: Statistical learning techniques using a complete machine learning pipeline.
- **Key Features**:
  - Linear regression (baseline modeling)
  - Polynomial feature interaction modeling
  - Lasso (L1) regularization
  - Cross-validated model selection
  - Exploratory data visualization and residual analysis

---

## Dataset

The dataset used includes:
- Physical properties: wall area, roof area, glazing, etc.
- Target variables:
  - `Heating Load`
  - `Cooling Load`

---

## Methods

- **Data Preprocessing**
  - Standard scaling of numeric variables
  - Use of one-hot encoded categorical variables
- **Feature Engineering**
  - Interaction-only polynomial expansion
  - Post-expansion scaling to stabilize regularization
- **Modeling**
  - `LinearRegression` (as baseline)
  - `ElasticNetCV` with `l1_ratio=1` (equivalent to Lasso)
- **Evaluation**
  - Residual plots to assess model fit
  - R² and cross-validated MSE
  - Interpretation of Lasso coefficients

---

## Results

- **Heating Load R²**: ~0.96  
- **Cooling Load R²**: ~0.93  
- Residuals resemble noise, indicating good model fit  
- Lasso successfully reduced model complexity by zeroing out many coefficients

---

## Requirements

Install the required libraries with:

```bash
pip install pandas numpy scikit-learn matplotlib seaborn
```

---

## Running the Notebook

1. Clone or download this repository.
2. Open the notebook `energy_efficency_modeling_linear_regression_lasso.ipynb`.
3. Run all cells in order to reproduce the analysis.

---

## File Structure

.
├── energy_efficency_modeling_linear_regression_lasso.ipynb # Main analysis notebook
└── README.md # Project overview and instructions

---

## Skills Demonstrated

✅ Data preprocessing  
✅ Regularization techniques  
✅ Pipeline construction  
✅ Model tuning and validation  
✅ Statistical interpretation of coefficients

---

## Notes

This project was designed for clarity, computational efficiency, and strong predictive performance.

While simple models performed well, future work could explore non-linear or ensemble methods to further improve performance and model flexibility.
