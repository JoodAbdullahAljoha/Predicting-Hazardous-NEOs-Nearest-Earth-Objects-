# Hazardous NEO Classification

This project focuses on predicting whether a Near-Earth Object (NEO) is hazardous based on a dataset of NEOs observed by NASA from 1910 to 2024. The objective is to classify NEOs into two categories: hazardous and non-hazardous, which is vital for planetary defense.

## Dataset
The dataset contains 338,199 records of NEOs, with features like `absolute_magnitude`, `estimated_diameter_min`, `estimated_diameter_max`, `relative_velocity`, and `miss_distance`. The target variable is `is_hazardous`, which indicates whether an NEO is classified as hazardous by NASA.

## Approach
The following steps were taken to preprocess and model the data:
1. **Data Preprocessing**: 
   - Scaling numerical features using `StandardScaler`.
   - Handling categorical variables using `LabelEncoder`.
   - Addressing class imbalance using **SMOTE** (Synthetic Minority Over-sampling Technique).

2. **Modeling**:
   - We trained multiple machine learning models, including **Logistic Regression** and **Random Forest Classifier**, to predict the hazardous NEOs.

3. **Evaluation Metrics**:
   - We evaluated model performance using precision, recall, F1-score, confusion matrix, and AUC-ROC score.
   
## Results

### Logistic Regression:
- **Accuracy**: 80%
- **Precision**: 0.85 (non-hazardous), 0.75 (hazardous)
- **Recall**: 0.71 (non-hazardous), 0.88 (hazardous)
- **F1-Score**: 0.78 (non-hazardous), 0.81 (hazardous)
  
### Random Forest Classifier:
- **Accuracy**: 92%
- **Precision**: 0.95 (non-hazardous), 0.90 (hazardous)
- **Recall**: 0.89 (non-hazardous), 0.96 (hazardous)
- **F1-Score**: 0.92 (non-hazardous), 0.93 (hazardous)
- **AUC-ROC Score**: 0.974

## Conclusion
The **Random Forest Classifier** outperforms the **Logistic Regression** model in terms of accuracy, recall, and F1-score. The AUC-ROC score further indicates the superior ability of the Random Forest model to discriminate between hazardous and non-hazardous NEOs.


