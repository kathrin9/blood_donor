#Blood Donor Availability Prediction
#Project Overview

This project focuses on the analysis and prediction of blood donor availability using structured donor data. The primary objective was to evaluate whether feature engineering improves predictive performance, while ensuring proper validation practices to avoid data leakage and overfitting. The task was formulated as a binary classification problem, where the target variable represents donor availability.

#Dataset Description

The dataset contains demographic and donation-related information for individual blood donors. Features include donor history and relevant characteristics, while the target variable indicates whether a donor is available. The dataset size and structure make it suitable for classical machine learning models, with an emphasis on interpretability and generalization.

#Data Preparation and Preprocessing

Before modeling, the data underwent a careful preprocessing phase. This included cleaning and formatting features, handling missing values where necessary, and ensuring consistent data types. All preprocessing steps were implemented using scikit-learn Pipelines, guaranteeing that transformations were applied only within training folds and preventing data leakage.

Two experimental setups were designed:

Baseline modeling, using minimal preprocessing and no additional feature engineering

Feature-engineered modeling, applying domain-driven transformations to assess their impact on performance

#Modeling Approach

Multiple classification models were evaluated, including:

Logistic Regression

Random Forest

XGBoost

Support Vector Machine (SVM)

Logistic Regression was selected as the primary model due to its strong generalization performance, lower variance, and interpretability. Tree-based and boosting models were used as benchmarks for comparison.

All models were trained and evaluated using stratified cross-validation, ensuring that class imbalance was properly handled.

#Evaluation Strategy

Model performance was assessed using several metrics, with a focus on:

F1-score (primary metric)

Recall (critical in donor availability prediction)

ROC-AUC

Accuracy and Precision (for completeness)

Each model was evaluated before and after feature engineering, allowing for a direct comparison of performance changes.

#Key Findings

The experimental results showed that extensive feature engineering did not consistently improve model performance. In several cases, complex transformations increased variance and led to lower cross-validated F1-scores.

The baseline Logistic Regression model, combined with regularization and proper validation, achieved the most stable and reliable results. Feature engineering provided only marginal improvements in Recall and ROC-AUC for some models (notably Logistic Regression and XGBoost), but these gains were not substantial enough to justify increased complexity.

#Conclusion

This project demonstrates that, for small-to-medium structured datasets, simpler models with careful validation and minimal feature engineering can outperform more complex approaches. Logistic Regression proved to be an effective and interpretable solution for predicting blood donor availability, offering strong generalization and robustness without unnecessary complexity.
