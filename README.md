# CSET485 – AI and Society | Assignment #1

## Predictive Modeling, Stress Testing and Fairness Analysis on German Credit Data

**Student:** Yash Agarwal  
**Enrolment Number:** S24CSEU0244  
**Course:** CSET485 – AI and Society  
**Dataset:** German Credit Data (UCI Statlog)  
**Random State:** 244

## 1. Project Purpose

This project builds and compares two predictive models using the German Credit dataset: an Ordinary Least Squares (OLS) linear probability model and a logistic regression model.

The analysis compares their classification rules (OLS median threshold versus logistic regression threshold of 0.5) and investigates the reliability, limitations, and fairness of the logistic model through four stress tests.

The objective is to understand how model choices, omitted variables, subgroup differences, confident prediction errors, and decision thresholds affect credit-risk decisions.

## 2. Dataset

The project uses the German Credit dataset from the UCI Machine Learning Repository.

**Dataset source:** https://archive.ics.uci.edu/dataset/144/statlog+german+credit+data

The dataset contains 1,000 credit applicants, 20 input attributes, and a class label. The documented class distribution is 700 good-credit cases and 300 bad-credit cases.

The notebook checks the dataset shape and class distribution before performing the analysis.

## 3. Data Preprocessing

The notebook documents the following preprocessing steps:

- Missing-value inspection.
- Categorical feature encoding using one-hot encoding.
- Feature scaling using `StandardScaler`, fitted on the training data only.
- Outlier inspection and the documented transformation of the loan amount.
- Target encoding, with 1 representing good credit/approval and 0 representing bad credit/rejection.
- Train–test splitting using `test_size=0.30` and `random_state=244`.

These steps prepare the data for model fitting and evaluation.

## 4. Part 1 — Model Comparison

The notebook compares:

- **Model A:** Ordinary Least Squares (OLS) linear probability model.
- **Model B:** Logistic regression.

The comparison includes model coefficients, statistical results, test-set performance, prediction thresholds, an agreement matrix, and mismatch analysis.

## 5. Part 2 — Four Stress Tests

### 5.1 Subgroup Analysis

Investigates differences in the relationship between age and credit outcomes across sex-based subgroups, including statistical tests and robustness analysis.

### 5.2 Omitted-Variable Bias

Compares the full logistic regression model with a reduced model that excludes checking-account status. The analysis examines coefficient changes and differences in model performance.

### 5.3 Confident Classification Errors

Identifies confidently incorrect predictions using the documented probability thresholds. It examines the characteristics of these cases and compares them with the test dataset.

### 5.4 Fairness Analysis

Evaluates demographic parity, equalized odds, and predictive parity across ten classification thresholds, using age groups of 25 years or younger versus older than 25 years.

Tables, charts, and numerical comparisons are used to examine the trade-offs between fairness measures and predictive performance.

## 6. Part 3 — Descriptive Analysis

The assignment includes eight descriptive questions addressing model disagreement, subgroup differences, omitted-variable bias, confounding, confident errors, fairness trade-offs, threshold selection, and demographic parity versus equalized odds.

## 7. Part 4 — Reflection

The reflection discusses the implications of the analysis for model deployment, predictive accuracy, fairness, limitations, and responsible credit decision-making.

## 8. Notebook and Reproduction Instructions

The Jupyter Notebook in this repository is named:

`CSET485_German_Credit_Analysis.ipynb`

To inspect or run the analysis:

1. Open the notebook from this GitHub repository.
2. Select **Open in Colab** if available, or download it and open it in Jupyter Notebook.
3. Install any missing dependencies required by the notebook.
4. Run all cells sequentially from the beginning.
5. Review the generated outputs, tables, charts, and model evaluation results.

The notebook should be executed from a fresh runtime to check that the results can be reproduced.

## 9. Software and Dependencies

The analysis uses Python and may require the following libraries, depending on the notebook implementation:

- pandas
- NumPy
- SciPy
- statsmodels
- scikit-learn
- Matplotlib
- seaborn
- openpyxl
- Jupyter Notebook

Install the dependencies required by the actual notebook before execution.

## 10. Assumptions and Limitations

- The train–test split uses `random_state=244`.
- The interpretation of class labels follows the dataset encoding used in the analysis.
- Subgroup estimates may be less precise because of smaller subgroup sample sizes.
- The dataset does not include income or debt-to-income information, limiting the assessment of repayment capacity.
- Statistical associations do not necessarily establish causation.
- Fairness metrics capture different aspects of model performance and must be interpreted in context.

## 11. Repository Contents

- `README.md` — project description, methodology, and instructions.
- `CSET485_German_Credit_Analysis.ipynb` — Jupyter Notebook containing the analysis and computations.

Additional dependency or output files should be included when they are required to run the notebook or reproduce the submitted report.

---

**Author:** Yash Agarwal  
**Enrolment Number:** S24CSEU0244

