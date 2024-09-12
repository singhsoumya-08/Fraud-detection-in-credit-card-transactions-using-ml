Credit Card Fraud Detection
This project focuses on detecting fraudulent credit card transactions using machine learning techniques. The dataset used contains transactions made by European cardholders in September 2013. The primary goal of this project is to build a model that accurately classifies transactions as fraudulent or legitimate.

Link to the dataset: https://www.kaggle.com/datasets/mlg-ulb/creditcardfraud

Credit card fraud detection is a critical application of machine learning. The dataset used in this project is highly imbalanced, with only 492 fraud cases out of 284,807 transactions. Traditional accuracy metrics are not suitable for such imbalanced datasets, so we evaluate the model using metrics like Area Under the Precision-Recall Curve (AUPRC).

Dataset
Source: The dataset consists of credit card transactions made by European cardholders.
Number of Transactions: 284,807
Fraudulent Transactions: 492 (about 0.17% of the dataset)
Features:
Time, Amount, Class
V1 to V28: Principal components obtained through PCA
LogAmount: Logarithm of transaction amount
Hour: Time of transaction in hours
Target Variable:
Class: 1 for fraud, 0 for non-fraud
Project Workflow
Data Preprocessing:

Standardization of features
Creation of additional features (LogAmount, Hour)
Handling Class Imbalance:

Used the SMOTE (Synthetic Minority Over-sampling Technique) to balance the dataset by creating synthetic samples for the minority class (fraudulent transactions).
Model Selection:

The main model used is the Random Forest Classifier, an ensemble learning method based on decision trees.
Cross-Validation:

Implemented K-Fold Cross-Validation to evaluate the model performance more robustly and ensure that the model generalizes well.
Techniques Used
Random Forest Classifier: A versatile model that fits multiple decision trees on various sub-samples of the dataset and averages the results to improve predictive accuracy.

SMOTE: A technique used to address the imbalanced nature of the dataset by oversampling the minority class (fraudulent transactions).

K-Fold Cross-Validation (KFoldCV): Used to split the dataset into training and validation sets, ensuring robust model performance and reducing overfitting.

Model Performance
Since the dataset is highly imbalanced, traditional accuracy metrics are not meaningful. Instead, we evaluate the model using:

Area Under the Precision-Recall Curve (AUPRC): To assess the trade-off between precision and recall for different thresholds.
Confusion Matrix: Provides insight into the number of true positives, false positives, true negatives, and false negatives.
