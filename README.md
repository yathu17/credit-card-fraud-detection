# credit-card-fraud-detection
Banks face huge financial losses due to fraudulent transactions. The challenge is to detect fraudulent activity in highly imbalanced datasets while minimizing false negatives.

Dataset - https://www.kaggle.com/datasets/mlg-ulb/creditcardfraud

Process

Data Preparation:

	•	Loaded the Kaggle dataset (creditcard.csv) containing anonymized transaction features.
	•	Observed extreme imbalance: 99.8% normal transactions vs ~0.2% fraud.
	•	Applied StandardScaler to normalize numeric features.

Handling Class Imbalance:

	•	Used SMOTE (Synthetic Minority Oversampling Technique) to oversample fraud cases in the training data.
	•	Balanced dataset enabled models to learn fraud patterns better.

Model Training:

	•	Trained Logistic Regression and Random Forest classifiers.
	•	Evaluated models using precision, recall, F1-score, and ROC-AUC (since accuracy is misleading with imbalance).

Model Evaluation (Random Forest Example)

Confusion Matrix (from your output):

	•	True Negatives (TN): 56,852 legitimate transactions correctly identified
	•	False Positives (FP): 12 legitimate transactions wrongly flagged as fraud
	•	False Negatives (FN): 17 fraudulent transactions missed
	•	True Positives (TP): 81 fraudulent transactions correctly detected

Key Findings

	•	The Random Forest model achieved strong performance, with very few false positives and a good recall rate for fraud cases.
	•	Even with oversampling, the model managed to detect the majority of fraudulent cases while minimizing missed frauds.
	•	Recall (sensitivity) is the most important metric here, since missing fraud (false negatives) can lead to financial losses.

Conclusion
The Random Forest model, combined with SMOTE oversampling, proved effective at detecting credit card fraud. With only 17 missed fraud cases out of ~57k transactions, this model could significantly reduce fraud-related losses for financial institutions.
