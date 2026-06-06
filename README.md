# Diabetes-Prediction-ML
Machine learning predicting diabetes using supervised machine learning classification model such as Logistic Regression, Decision Tree, Support Vector Machine (SVM)
Diabetes Prediction Using Machine Learning

Project Overview
This project applies machine learning techniques to predict the onset of diabetes based on clinical and demographic data. The goal was to create an accurate, interpretable predictive model while addressing potential biases in healthcare data utilization.

Note: This was developed as a collaborative academic project for the MSc Software Engineering Machine Learning module at the University of West London.

Dataset
Source: Pima Indian Diabetes Dataset

Size: 768 participants

Features: 11 independent predictor variables, including medical measurements (Glucose, Blood Pressure, BMI, Insulin), patient history (Pregnancies, Diabetes Pedigree Function), and lifestyle factors.

Target Variable: Binary outcome indicating whether a patient is diabetic (1) or non-diabetic (0).

Data Preprocessing & Exploratory Data Analysis (EDA)
During our EDA, we identified a class imbalance (65% non-diabetic / 35% diabetic) and handled several data quality issues to ensure robust model training:

Missing Data Imputation: Missing medical values (recorded as zeros in Insulin, SkinThickness, Blood Pressure, and BMI) were imputed using median values to preserve data distribution.

Outlier Handling: Extreme outliers in Glucose and Insulin were handled via winsorisation, capping values at the 5th and 95th percentiles.

Feature Engineering: Developed new predictive indicators, including BMI categories, age groups, high insulin flags, and a metabolic risk score. Categorical variables (like Family History) were encoded to an ordinal scale.

Data Splitting: Data was split into Training (70%), Validation (15%), and Test (15%) sets using stratified sampling to maintain class proportions.

Scaling: Features were normalized using StandardScaler.

Models Evaluated
We tested and compared three distinct machine learning algorithms:

Logistic Regression (Baseline interpretable model)

Support Vector Machine (SVM) (Non-linear classification)

Decision Tree Classifier (Hyperparameter tuned)

Results & Best Model
The Decision Tree model performed the best after hyperparameter tuning (max_depth=5, min_samples_split=10).

Test Accuracy: 81%

F1-Score: 0.77

Recall: 0.75

The model demonstrated minimal overfitting, with less than 3% variance between training and testing performance. Logistic Regression achieved a moderate 78% test accuracy, while the SVM achieved 77%.

Key Predictors (Feature Importance)
The model identified the following features as the most significant predictors of diabetes:

Glucose: 0.42 importance

Age: 0.18 importance

BMI: 0.15 importance

Conclusion
The tuned Decision Tree proved to be the most suitable model for potential deployment due to its balance of predictive accuracy, computational efficiency, and high interpretability for healthcare professionals.
