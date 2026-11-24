# Fraud Detection in Financial Transactions (synthetic data demo)

A learning project that walks through a fraud-detection workflow on **synthetic** transaction data.

## What I did
- **Generated data** with scikit-learn `make_classification` plus Faker: 1,000 transactions with amount, merchant, user, location and timestamp, about 5% labelled as fraud, with fraud patterns such as unusually large amounts added on top.
- **Feature engineering:** extracted hour of day and day of week from timestamps.
- **Model:** Random Forest classifier with an 80/20 train/test split, evaluated with a classification report and confusion matrix.

## Note on results
The model scores perfectly on the test set because the synthetic fraud cases follow simple rules that the model learns easily. Real transaction data would need class-imbalance handling, time-based validation and precision/recall trade-offs. This repo shows the workflow, not production-level performance.

**Tools:** Python, Pandas, NumPy, Faker, scikit-learn (Random Forest)
