# bank_marketing_prediction
Bank Marketing Prediction

a. Problem statement 
  The objective of this project is to predict whether a client will subscribe to a term deposit based on direct marketing campaign data from a Portuguese banking institution. This is a binary classification problem where the goal is to identify potential customers who are likely to subscribe to a term deposit product. 
  The prediction model helps the bank:
    Optimize marketing campaign effectiveness
    Reduce marketing costs by targeting likely subscribers
    Improve customer satisfaction through personalized outreach
    Allocate resources more efficiently
    
b. Dataset description 
    Dataset Name: Bank Marketing Dataset
    Source: UCI Machine Learning Repository
    URL: https://archive.ics.uci.edu/ml/datasets/bank+marketing
    Dataset Characteristics
      Total Samples: 41,188 customer records
      Number of Features: 20 (before encoding)
      Features after Preprocessing: 62 (after one-hot encoding)
      Target Variable: y (binary: yes/no for term deposit subscription)
      Problem Type: Binary Classification
| Class                   | Count  | Percentage |
|-------------------------|--------|------------|
| No subscription (0)     | 36,548 | 88.7%      |
| Subscribed (1)          | 4,640  | 11.3%      |
    Imbalance Ratio7.88:1    

c. Models used:
  Model Performance Comparison
| Model | Accuracy | AUC | Precision | Recall | F1 Score | MCC |
|------|----------|------|-----------|--------|----------|------|
| Logistic Regression | 0.8616 | 0.9383 | 0.4453 | 0.8930 | 0.5943 | 0.5679 |
| Decision Tree | 0.8362 | 0.9356 | 0.4027 | 0.9166 | 0.5596 | 0.5381 |
| K-Nearest Neighbors (kNN) | 0.9029 | 0.9047 | 0.6063 | 0.4118 | 0.4904 | 0.4490 |
| Naive Bayes | 0.8258 | 0.8302 | 0.3550 | 0.6545 | 0.4603 | 0.3917 |
| Random Forest | 0.8347 | 0.9356 | 0.4009 | 0.9241 | 0.5592 | 0.5393 |
| XGBoost | 0.8673 | 0.9487 | 0.4576 | 0.9123 | 0.6095 | 0.5867 |

  Model Observations Table:

| ML Model | Observation about Model Performance |
|----------|--------------------------------------|
| **Logistic Regression** | Delivers solid and well-balanced performance (Accuracy: **0.8616**, AUC: **0.9383**). Maintains high recall (**0.8930**), making it reliable where identifying positive cases is important. |
| **Decision Tree** | Achieves very high recall (**0.9166**) but lower precision (**0.4027**), indicating a tendency to over-predict the positive class and produce more false positives. |
| **kNN** | Produces the **highest accuracy (0.9029)** and **best precision (0.6063)**, but recall is relatively low (**0.4118**). Good overall correctness but misses many positives. Sensitive to feature scaling and computationally heavier at inference. |
| **Naive Bayes** | Shows the weakest overall performance (Accuracy: **0.8258**, AUC: **0.8302**). Limited by the feature independence assumption. Still useful as a fast and interpretable baseline. |
| **Random Forest** | Achieves the **highest recall (0.9241)**, capturing most positive cases. Precision remains modest (**0.4009**). Suitable where minimizing false negatives is critical. |
| **XGBoost** | **Best overall performer** with strongest balance across metrics (F1: **0.6095**, AUC: **0.9487**, MCC: **0.5867**). Provides robust discrimination and generalization. Most suitable for deployment. |
  
