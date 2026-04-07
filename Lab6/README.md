# Lab 6 — Ecommerce Customers (Summary)

Things I learned while completing Lab 6.

- **Data loading & exploration:** practice with `pandas` (head, info, describe). Good reminder to always inspect shapes and types first.
- **Basic cleaning:** check for missing values and confirm the dataset is clean before modeling.
- **Feature selection:** choose meaningful numeric features (`Avg. Session Length`, `Time on App`, `Time on Website`, `Length of Membership`) and the target (`Yearly Amount Spent`).
- **Train/test split:** use `train_test_split` to evaluate model generalization (I used `test_size=0.3, random_state=101`).
- **Modeling:** trained a `LinearRegression` model and inspected coefficients to understand feature impact.
- **Evaluation metrics:** compute MAE, MSE, and RMSE to quantify prediction error.
- **New and useful plot — Actual vs Predicted (`y` vs `y_hat`):**
  - This scatter plot of actual target values versus predicted values helps quickly assess how well predictions match truth.
  - Points tightly clustered around the diagonal line indicate good predictions; systematic deviations reveal bias or poor fit.
  - I found this visualization especially helpful for spotting heteroscedasticity and large outliers.
- **Residuals distribution:** plot residuals to check for normality and patterns (another quick sanity check).
