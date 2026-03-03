# Loan Payments Data: Quality Assessment & Preprocessing

This notebook applies a complete data preprocessing pipeline to the loan payments dataset, preparing it for use in machine learning models.

## 🚀 Project Overview

The notebook covers all major preprocessing stages required before training a model:

1. **Data Quality Assessment**: Identifying data type issues, missing values, duplicates, and anomalies.
2. **Missing Value Handling**: Applying semantically correct imputation strategies per column.
3. **Outlier Detection & Handling**: Using the IQR method to detect and cap extreme values.
4. **Normalization**: Scaling numerical features using both Min-Max and Z-Score techniques.
5. **Dimensionality Reduction (PCA)**: Applying Principal Component Analysis and interpreting explained variance.

## 📊 Dataset Information

The dataset used is the **zhijinzhai/loandata** from Kaggle.

- **Size**: 500 rows, 11 columns
- **Key Features**:
  - `Loan_ID`: Unique loan identifier (excluded from analysis)
  - `loan_status`: Current status of the loan (PAIDOFF, COLLECTION)
  - `Principal`: Original loan amount issued
  - `terms`: Loan repayment schedule (days)
  - `effective_date`, `due_date`, `paid_off_time`: Date columns (converted to datetime)
  - `past_due_days`: Days the loan is overdue (NaN = on time, filled with 0)
  - `age`, `education`, `Gender`: Borrower demographic information

## 🛠️ Requirements

```bash
pip install pandas numpy matplotlib seaborn scikit-learn kagglehub
```

## 📋 Tasks Breakdown

### Task 1 — Data Quality Assessment
- Inspects data types, missing values per column, duplicate rows, and summary statistics.
- Identifies `paid_off_time` as structurally missing (only populated for paid-off loans).
- Flags date columns stored as `object` that require type conversion.

### Task 2 — Missing Value Strategy
- `past_due_days`: Filled with **0** (NaN = no days past due, not a data error).
- `paid_off_time`: **Dropped** entirely due to structural missingness.
- `education`, `Gender`: **Mode imputation** for any missing categorical values.

### Task 3 — Outlier Detection & Handling
- Detects outliers in `Principal`, `terms`, `past_due_days`, and `age` using the IQR method.
- Handles outliers via **IQR capping (Winsorization)** — preserves all rows while neutralizing extremes.

### Task 4 — Normalization
- **Min-Max Normalization**: Scales all numerical features to the range [0, 1].
- **Z-Score Standardization**: Centers features around 0 with unit standard deviation.
- Includes histogram comparisons for each feature across both methods.

### Task 5 — PCA
- Applies PCA on Z-score standardized features.
- Reports explained variance per component and cumulative variance.
- Generates a scree plot and 2D scatter projection (PC1 vs PC2).

## 📈 Key Findings
- `past_due_days` has the most outliers, driven by a small set of severely overdue loans.
- After capping, all four numerical features show tighter, more model-friendly distributions.
- PCA reveals how much of the dataset's variance can be captured in fewer dimensions, helping assess the benefit of dimensionality reduction before model training.

## 📁 Repository Structure
- `Lab4.ipynb`: Main Jupyter Notebook with all preprocessing steps and visualizations.

## 📝 How to Use
1. Ensure the required libraries are installed.
2. Run the first cell to download the dataset via `kagglehub`.
3. Execute cells sequentially to reproduce the full preprocessing pipeline.

