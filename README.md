# Traffic Crash Analysis and Prediction using Machine Learning

This project involves a comprehensive analysis of road traffic collisions in Maryland, USA, with the goal of understanding crash patterns and predicting various outcomes using machine learning models. By leveraging a dataset containing 97,000+ collision records, we applied advanced data cleaning, exploratory data analysis (EDA), and machine learning techniques to derive actionable insights for improving road safety.  

---

## Table of Contents  
- [Introduction](#introduction)  
- [Dataset](#dataset)  
- [Techniques and Methodologies](#techniques-and-methodologies)  
- [Key Findings](#key-findings)  
- [Machine Learning Models](#machine-learning-models)  
- [Results](#results)  
- [Future Work](#future-work) 

---

## Introduction  
Traffic accidents remain a critical global issue, causing significant loss of life, injuries, and economic burdens. This project focuses on leveraging data analytics and machine learning to identify crash patterns and predict outcomes like collision severity, hit-and-run incidents, and driver behavior.  

---

## Dataset  
The dataset contains 97,458 records with 44 features, representing traffic collisions in Maryland. It was obtained from [Crash Reports - Incidents Data - Maryland, USA](https://data.montgomerycountymd.gov/Public-Safety/Crash-Reporting-Incidents-Data/bhju-22kf/about_data). Key features include:  
- **Categorical**: Weather, Light Conditions, Collision Type, Driver Substance Abuse.  
- **Numerical**: Distance, Mile Point, Latitude, Longitude.  

### Data Cleaning  
- Removed redundant categories and handled missing values using techniques like inter-feature correlation and probability-based random sampling.  
- Resolved class imbalances by eliminating off-road crashes and consolidating null values into meaningful categories (e.g., "NONE" for non-motorist data).  

---

## Techniques and Methodologies  
- **Exploratory Data Analysis (EDA)**:  
  - Time Series Analysis: Seasonal patterns of crashes across months and years.  
  - Spatial Analysis: Hotspot mapping of crash locations.  
  - Correlation Analysis: Chi-Square, Cramer’s V, and Theil’s U for categorical feature relationships.  

- **Machine Learning Models**:  
  - Implemented and evaluated Logistic Regression, Decision Trees, Random Forests, and XGBoost.  
  - Used Recursive Feature Elimination (RFE) for feature selection.  
  - Applied weighted loss functions to handle class imbalance.  

- **Data Engineering**:  
  - Encoded categorical features using Label Encoding.  
  - Balanced dataset classes using future-suggested techniques like SMOTE.  

---

## Key Findings  
- **Seasonal Trends**: Higher crash rates during October and December (holiday season).  
- **Collision Types**: Fatal crashes were often linked to opposite-direction sideswipe and angle-left turn crashes.  
- **Hit-and-Run Behavior**: Strongly correlated with driver substance abuse and light conditions.  
- **Weather Impact**: Most crashes occurred under clear weather conditions.  

---

## Machine Learning Models  
This project formulated six key problem statements:  

1. **Collision Severity Prediction**  
   - Models: Random Forest, XGBoost (Best: F1-Score 0.66).  

2. **Hit-and-Run Prediction**  
   - Models: XGBoost (Best: F1-Score 0.87).  

3. **Driver Fault Detection**  
   - Models: XGBoost (Best: F1-Score 0.93).  

4. **Driver Substance Abuse Prediction**  
   - Models: XGBoost (Best: F1-Score 0.72).  

5. **Collision Type Detection**  
   - Models: Random Forest, XGBoost (Overfitting due to class imbalance).  

6. **Junction Type Prediction**  
   - Models: XGBoost (Best: F1-Score 0.67).  

---

## Results  
- Random Forests and XGBoost provided the highest accuracy and F1-scores for most problem statements.  
- Model performance was impacted by class imbalances in the dataset, necessitating future optimization strategies.  

---

## Future Work  
- **Class Balancing**: Implement SMOTE or other synthetic sampling techniques.  
- **Hyperparameter Tuning**: Fine-tune models for improved accuracy and generalization.  
- **Feature Reduction**: Apply PCA, LDA, or Autoencoders to optimize feature sets.  
- **External Data Integration**: Include weather data for improved predictions.  
- **Time Series Forecasting**: Predict crash frequencies for proactive safety measures.  
