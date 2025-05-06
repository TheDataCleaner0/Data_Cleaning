# 🧼 Cafe Sales Data Cleaning

This project focuses on cleaning and preprocessing a messy transactional dataset from a fictional café. The raw data contains missing values, incorrect data types, and inconsistent pricing. The goal was to transform this into a clean, analysis-ready dataset using Python and pandas.

---

## 📁 Dataset Overview

- **Source:** [dirty_cafe_sales](https://www.kaggle.com/datasets/ahmedmohamed2003/cafe-sales-dirty-data-for-cleaning-training/data)
- **Rows:** 10,000  
- **Columns:**
  - `Transaction ID`
  - `Item`
  - `Quantity`
  - `Price Per Unit`
  - `Total Spent`
  - `Payment Method`
  - `Location`
  - `Transaction Date`

---

## 🧹 Cleaning Process

1. **Data Type Conversion**
   - Converted `Quantity`, `Price Per Unit`, and `Total Spent` to numeric types.
   - Parsed `Transaction Date` into datetime format.

2. **Handling Missing & Invalid Data**
   - Replaced `"ERROR"` and `"UNKNOWN"` with `NaN`.
   - Imputed missing values:
     - Used **mode** for categorical data like `Item`, `Payment Method`, and `Location`.
     - Used **median** for `Quantity`.
     - Used a **derived column** for missing `Price Per Unit` (calculated as `Total Spent / Quantity`).
     - Created a **reference table** for average prices per item to fill in unknown prices.

3. **Derived Columns**
   - Recalculated `Total Spent` for consistency.
   - Validated calculations by cross-checking quantity * price.

---

## ✅ Final Outputs

- ✅ Cleaned dataset: `cleaned_cafe_sales.csv`
- ✅ Jupyter Notebook: `cafe_sales_cleaning.ipynb`

---

## 📊 Tools & Libraries

- Python
- pandas
- numpy
- Jupyter Notebook

---

## 📌 Key Takeaways

- Cleaned and standardized a real-world messy dataset.
- Demonstrated different techniques to impute missing values based on context.
- Built helper function for better imputation accuracy.
- Emphasized reproducibility and clarity in the data cleaning process.


