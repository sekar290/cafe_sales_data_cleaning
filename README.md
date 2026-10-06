# cafe_sales_data_cleaning
Data cleaning project on a dirty cafe sales dataset: handling missing values, duplicates, inconsistent formats, and invalid entries to produce an analysis-ready dataset.

## Dataset
- Source: https://www.kaggle.com/datasets/ahmedmohamed2003/cafe-sales-dirty-data-for-cleaning-training/data
- Rows : 10.000 rows
- Main columns: Transaction ID, Item, Quantity, Price Per Unit,
  Total Spent, Payment Method, Location, Transaction Date

## Data issues found
- Missing values (e.g. Item, Payment Method, Location)
- Placeholder values such as "ERROR" and "UNKNOWN"
- Wrong data types (numbers and dates stored as text)
- Inconsistent totals (Quantity x Price Per Unit != Total Spent)

## Cleaning steps
1. Inspect data (`df.info()`, `df.isna().sum()`)
2. Standardize placeholders to NaN
3. Fix data types
4. Handle missing values
   - Categorical columns: mode imputation or an "Unknown" category
   - Numeric columns: recompute from related columns, or median
5. Remove duplicates
6. Validate results

## Tech stack
Python (pandas), Jupyter Notebook
