# Fraud_Detection_using_Decision_Tree_and_XGBoost
📌 Problem Statement
Financial fraud is a significant challenge for modern banking and payment systems. This project aims to build a robust machine learning model to detect fraudulent transactions among legitimate ones. Given the high imbalance in financial datasets (where fraud is rare compared to normal activity), the objective is to leverage advanced algorithms to identify suspicious patterns effectively, thereby minimizing financial losses and enhancing security.

🛠️ Machine Learning Techniques
In this project, we implemented and compared two powerful classification algorithms:

1. Decision Tree Classifier: A flowchart-like structure that makes decisions based on feature values.

2. XGBoost (Extreme Gradient Boosting): A high-performance gradient boosting library designed for speed and accuracy, particularly effective       for imbalanced tabular data.

📊 Data Preprocessing & Visualization

To ensure model accuracy and handle real-world data inconsistencies, the following steps were taken:

--> Error Handling: Used on_bad_lines='skip' to bypass malformed rows in the raw dataset.

--> Data Cleaning: Identified and removed NaN (null) values from the target variable (isFraud) and imputed numeric features with the median.

-->Encoding & Scaling: Converted categorical variables into numerical format using LabelEncoder and standardized features using StandardScaler.

-->EDA (Exploratory Data Analysis):

->Visualized the class imbalance using Count Plots.

->Analyzed feature relationships through Correlation Heatmaps.

->Determined Feature Importance to see which transaction attributes (like 'amount' or 'oldbalanceOrg') most strongly indicate fraud.

📈 Evaluation Results
The models were evaluated using Accuracy, Precision, Recall, and F1-Score.
<img width="701" height="160" alt="Screenshot 2026-05-03 at 10 01 18 AM" src="https://github.com/user-attachments/assets/23f25d90-e5ef-430d-b1f4-870fd91445c6" />

While both models achieved high overall accuracy, XGBoost demonstrated a higher F1-score for the fraud class, indicating a better balance between precision and recall for detecting rare fraudulent events.

🧠 Key Learnings
--> Handling Imbalance: In fraud detection, accuracy is often a misleading metric; F1-score and Recall are far more critical for identifying as     many fraudulent cases as possible.  

--> Robust Data Loading: Real-world datasets often contain malformed rows; using advanced pandas parameters like on_bad_lines is essential for      stable data pipelines.  

--> Gradient Boosting Advantages: XGBoost consistently outperformed the standard Decision Tree in identifying complex fraudulent patterns,          proving its effectiveness for tabular data challenges.  

--> Importance of Cleaning: Machine learning models cannot process NaN values in the target variable, making rigorous cleaning a non-negotiable     step in the workflow
