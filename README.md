Overview:

This project focused on building an effective machine learning model to detect credit card fraud, a critical issue for banks and financial institutions. The goal was to use supervised learning methods to develop a model that identifies fraudulent transactions quickly and accurately, reducing financial losses.

Dataset & EDA:

Sourced from Kaggle, the dataset includes 284,807 transactions over two days, with only 492 (0.172%) labeled as fraud — making it highly imbalanced.
All features are anonymized PCA components (V1 to V28), except for Time and Amount.
Fraud was more frequent during late-night and early morning hours.
PCA visualization showed a linear separability between fraud and non-fraud classes.

Methodology:

Models Used: Logistic Regression, Decision Trees, Random Forest, BernoulliNB, LDA, CatBoost, and XGBoost.
Balancing Techniques: SMOTE and undersampling were applied to address data imbalance.
valuation Metrics: Focused on precision and recall for the fraud class, rather than accuracy, due to class imbalance.
Validation: Stratified 5-fold cross-validation was used for traditional models, with test set evaluations for boosting models.

Key Findings:

SMOTE and undersampling improved recall but drastically lowered precision, making them less suitable for this dataset.
The best performance was achieved without balancing the dataset.
CatBoost delivered the top results with a recall of 0.96 and precision of 0.83, effectively detecting most fraudulent transactions while minimizing false positives.

High-Risk Goals:

Identified key features (V4, V14, V26) that were most influential in detecting fraud.
Recommended financial institutions monitor these variables (though their exact nature is unknown) as part of preventative strategies.
