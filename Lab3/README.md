# Loan Payments Data Analysis (EDA)

This project performs a comprehensive Exploratory Data Analysis (EDA) on a loan payments dataset. The goal is to understand customer demographics, loan statuses, and identify patterns that contribute to loan repayment or default.

## 🚀 Project Overview
The notebook covers the full data science lifecycle of EDA, including:
- **Data Acquisition**: Programmatic download via `kagglehub`.
- **Data Cleaning**: Handling missing values, checking for duplicates, and type conversion.
- **Descriptive Statistics**: Statistical summaries of the dataset.
- **Univariate Analysis**: Analyzing single variables like loan status and education level.
- **Bivariate Analysis**: Investigating relationships between features (e.g., Revenue by Country, Correlation Matrices).

## 📊 Dataset Information
The dataset used is the **zhijinzhai/loandata** from Kaggle.
- **Size**: 500 rows, 11 columns.
- **Key Features**: 
  - `loan_status`: Current status of the loan (PAIDOFF, COLLECTION, etc.)
  - `Principal`: The original amount of the loan.
  - `terms`: Payment schedule terms.
  - `age`, `education`, `Gender`: Demographic information of the borrower.
  - `past_due_days`: Days the loan is overdue.

## 🛠️ Requirements
To run this notebook, you will need the following Python libraries:
- `pandas`
- `seaborn`
- `matplotlib`
- `kagglehub`

## 📈 Key Insights
- **Loan Distribution**: The majority of loans in the dataset are already paid off.
- **Demographics**: Borrowers with "Master or Above" degrees are significantly less frequent in this specific loan pool compared to those with high school or college education.
- **Correlations**: The analysis explores correlations between loan amounts (`Principal`) and borrower `age`.

## 📁 Repository Structure
- `Lab3.ipynb`: The main Jupyter Notebook containing the code and visualizations.
- `Loan payments data.csv`: (Generated after running the notebook) The raw data used for analysis.

## 📝 How to Use
1. Clone this repository.
2. Ensure you have the required libraries installed.
3. Run the cells in `Lab3.ipynb` to download the dataset and generate the visualizations.

---
*Created as part of Lab 3 Assignment.*