```
# Diabetes Dataset Classification

### Author  
Anam Jafar  

### Start Date  
December 26, 2024  


## Project Overview  
This project focuses on classifying patients as diabetic or non-diabetic based on health metrics using supervised learning. The dataset includes demographic, clinical, and lifestyle-related features. The objective was to preprocess the data, engineer meaningful features, and build a machine learning model to predict diabetes effectively.  



## Dataset  
- **Source:** Provided (raw CSV file)  
- **Size:** 77,000 rows and 10 columns  
- **Type:** Primarily numeric with one categorical variable  

### Features  
- **Patient_ID:** Unique identifier (not used in analysis)  
- **Age:** Age in years  
- **Gender:** Male/Female (categorical)  
- **BMI:** Body Mass Index (missing values present)  
- **Glucose_Level:** Blood glucose concentration (missing values present)  
- **Blood_Pressure:** Blood pressure levels (missing values present)  
- **Insulin:** Insulin levels (missing values present)  
- **Diabetes_Pedigree_Function:** Score estimating likelihood of diabetes based on family history  
- **Pregnancies:** Number of pregnancies (relevant for female patients)  
- **Outcome:** Target variable (1 = Diabetic, 0 = Non-Diabetic)  


## Methodology  
### 1. Data Preprocessing  
- Removed irrelevant columns (`Patient_ID`)  
- Encoded categorical features (e.g., `Gender`)  
- Scaled numerical features for consistency  
- Imputed missing values in BMI, Glucose, Blood Pressure, and Insulin  

### 2. Feature Engineering  
- Created interaction terms such as `BMI * Glucose_Level` and `Pregnancies / Age`  
- Grouped continuous variables into bins (e.g., age groups)  

### 3. Modeling  
- Applied **Random Forest Classifier**  
- Addressed class imbalance using **SMOTE** for the training set  

### 4. Evaluation Metrics  
- Accuracy  
- Precision  
- Recall  
- F1-score  
- ROC-AUC Score  


## Results  
- **Accuracy:** 60.06%  
- **Precision (Class 1):** 36%  
- **Recall (Class 1):** 19%  
- **F1-Score (Class 1):** 25%  
- **ROC-AUC Score:** 50.38%  



## Insights  
**Strengths:**  
- Model performs reliably for the majority class (Outcome = 0)  
- Random Forest effectively captures non-linear feature interactions  

**Weaknesses:**  
- Struggles with predicting minority class (Outcome = 1)  
- Low recall for diabetic patients due to class imbalance  



## Limitations and Future Work  
- **Class Imbalance:** Explore advanced oversampling techniques or weighted loss functions  
- **Feature Engineering:** Introduce domain-specific features to improve predictions  
- **Model Selection:** Test Gradient Boosting, Logistic Regression, or Neural Networks with hyperparameter tuning  
- **Binary Simplification:** Consider focusing on balanced binary classification for better recall  


## Conclusion  
This project demonstrates the use of Random Forest for diabetes prediction, achieving 60.06% accuracy. While effective for non-diabetic cases, improvements are needed for diabetic patient prediction. Future work should emphasize handling class imbalance and enhancing feature engineering for better generalization.  



## Tools and Technologies  
- **Programming Language:** Python  
- **Libraries:** pandas, matplotlib, seaborn, scikit-learn  



## Contact  
- **LinkedIn:** [linkedin.com/in/anam-jafar6](https://www.linkedin.com/in/anam-jafar6/)  
- **GitHub:** [github.com/anamjafar6](https://github.com/anamjafar6)  
