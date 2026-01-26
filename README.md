# blood_donor

#Project Overview
This project focuses on the analysis and prediction of blood donor availability using structured donor data. The primary objective was to evaluate whether feature engineering improves predictive performance, while ensuring proper validation practices to avoid data leakage and overfitting. The task was formulated as a binary classification problem, where the target variable represents donor availability.

#Dataset Description
The dataset contains demographic and donation-related information for individual blood donors. Features include donor history and relevant characteristics, while the target variable indicates whether a donor is available. The dataset size and structure make it suitable for classical machine learning models, with an emphasis on interpretability and generalization.

#Modeling Approach
Multiple classification models were evaluated, including:
Logistic Regression
Random Forest
XGBoost
Support Vector Machine (SVM)

All models were trained and evaluated using stratified cross-validation, ensuring that class imbalance was properly handled.


#Key Findings
The experimental results showed that extensive feature engineering did not consistently improve model performance. In several cases, complex transformations increased variance and led to lower cross-validated F1-scores.
The baseline Logistic Regression model, combined with regularization and proper validation, achieved the most stable and reliable results. Feature engineering provided only marginal improvements in Recall and ROC-AUC for some models (notably Logistic Regression and XGBoost), but these gains were not substantial enough to justify increased complexity.

#Conclusion
Multiple models were evaluated throughout this project. After applying feature engineering techniques, the Random Forest demonstrated the strongest performance on the validation set. These results highlight the importance of feature engineering when working with structured datasets and justify the selection of Random Forest as the best-performing model in this study.

