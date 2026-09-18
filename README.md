# Retail Store Sales Data Cleaning

## Project Overview

This project focuses on cleaning and preprocessing a retail store sales dataset using Python and Pandas.

The objective is to identify and fix common data quality issues such as missing values, duplicate records, incorrect data types, and inconsistent values.

## Dataset

The dataset contains retail transaction information including:

- Transaction ID
- Customer ID
- Category
- Item
- Price Per Unit
- Quantity
- Total Spent
- Payment Method
- Location
- Transaction Date
- Discount Applied

## Tools Used

- Python
- Pandas
- Jupyter Notebook

## Data Cleaning Performed

### Missing Values

The following missing values were identified and handled:

| Column | Issue | Treatment |
|---|---|---|
| Item | Missing values | Recovered using Category and Price Per Unit |
| Price Per Unit | Missing values | Calculated using Total Spent / Quantity where possible |
| Quantity | Missing values | Filled using category-wise median |
| Total Spent | Missing values | Calculated using Price Per Unit × Quantity |
| Discount Applied | Missing values | Filled with `Unknown` because it could not be reliably derived |

### Duplicate Records

- Checked for duplicate rows
- Checked for duplicate Transaction IDs
- No duplicate records were found

### Data Types

- Transaction Date was converted from object/string to datetime
- Quantity was converted to integer
- Numerical columns were checked for appropriate data types

### Inconsistent Values

Categorical columns were checked for:

- Extra whitespace
- Inconsistent category names
- Inconsistent payment methods
- Inconsistent location values

No significant formatting inconsistencies were found.

## Validation

The cleaned dataset was validated for:

- Missing values
- Duplicate records
- Duplicate Transaction IDs
- Negative numerical values
- Incorrect Total Spent calculations
- Correct data types

## Files

- `cleaned_retail_store_sales.csv` — Cleaned dataset
- `Data_Cleaning.ipynb` — Complete data cleaning process

## Dataset Source

Kaggle — Retail Store Sales: Dirty for Data Cleaning

## Project Objective

The goal of this project is to transform a raw and inconsistent dataset into a clean, reliable dataset suitable for further analysis and visualization.
