# Logistic Regression Assignment

This repository contains a Jupyter notebook that implements a Logistic Regression assignment using the `advertising.csv` dataset.

What the notebook does
- Loads and inspects the dataset (`advertising.csv`) and performs basic exploratory data analysis (EDA).
- Preprocesses features and splits the data into training and test sets.
- Implements logistic regression from scratch (sigmoid function, cost/loss, gradient descent) and trains the model.
- Trains and evaluates scikit-learn's `LogisticRegression` for comparison.
- Evaluates models using `sklearn.metrics.classification_report`

How to use
- Open the notebook [02-Logistic Regression Assignment.ipynb](02-Logistic%20Regression%20Assignment.ipynb) and run the cells sequentially.
- Install dependencies if needed:

```bash
pip install pandas numpy matplotlib seaborn scikit-learn
```

Notes
- The notebook is intended for learning: it shows both a manual implementation and a library-based approach, with visualizations to help understand model behavior.
