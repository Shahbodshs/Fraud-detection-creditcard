# Fraud Detection with Weighted Random Forest

This project aims to implement a machine learning model to detect fraudulent credit card transactions using the [Credit Card Fraud Detection Dataset](https://www.kaggle.com/datasets/mlg-ulb/creditcardfraud).
The key challenge here is dealing with the highly imbalanced nature of the dataset, where fraudulent transactions account for less than 1% of the data.
Handling imbalanced datasets is crucial because traditional accuracy metrics can be misleading.
Instead, we focus on more informative metrics such as Precision, Recall, F1-Score, and AUC-ROC.

## Motivation

The primary goal of this project is to learn how to handle imbalanced datasets, especially in scenarios where data augmentation isn't a suitable option.
This project addresses the issues of detecting minority class samples (fraud cases) and tuning the model for both precision and recall.

### Why Standard Accuracy Doesn't Work:
In imbalanced datasets, even if the model predicts all transactions as non-fraudulent, it could achieve high accuracy without correctly identifying any fraudulent cases.
That's why evaluation metrics like Precision, Recall, and F1-Score are more meaningful for fraud detection.

### Evaluation Metrics:
- **Precision**: Measures how many of the predicted frauds are actually frauds.
- **Recall**: Measures how many of the actual frauds were identified.
- **F1-Score**: A balance between Precision and Recall.
- **AUC-ROC**: Evaluates the trade-off between true positives and false positives at different thresholds.

## Key Insights
When working with imbalanced data and scaling feature ranges:
- **Min-Max Scaling** is effective without outliers.
- **Z-Score Normalization** works best when the data is normally distributed.
- **Robust Scaling** handles outliers effectively.

Additionally, understanding the nature of outliers and distribution of your data is crucial to select the right scaling technique and improve model performance.

### Results:
```plaintext
- AUC Score: 0.96
- Precision: High Precision, focusing on minimizing false positives.
- Recall: High Recall, ensuring the detection of most fraudulent transactions.
