## Cirrhosis Disease Prediction

### Project Overview

This project aims to predict the **presence and stage of cirrhosis disease** based on various clinical and demographic factors. By analyzing features such as patient age, sex, drug use, edema, and a range of lab test results (bilirubin, cholesterol, albumin, copper, etc.), the goal is to develop a machine learning model that can accurately classify a patient's liver health status. This is a critical task for medical diagnosis and patient management.

-----

### Technical Highlights

  * **Dataset**: [Kaggle - Cirrhosis Prediction Dataset](https://www.kaggle.com/datasets/fedesoriano/cirrhosis-prediction-dataset)
  * **Size**: 418 entries, 20 columns. The dataset contains a significant number of missing values.
  * **Key Features**:
      * Age, Sex, Ascites, Hepatomegaly, Spiders, Edema, Bilirubin, Cholesterol, Albumin, Copper, Alk\_Phos, SGOT, Tryglicerides, Platelets, Prothrombin.
  * **Approach**:
      * **Data Cleaning**: Missing values were imputed using the median for numerical columns and the mode for categorical columns. The target variable Stage also had missing values, which were filled with the median.
      * **Exploratory Data Analysis**: The code checks basic statistics, null values, duplicates, and unique values for all columns.
      * **Label Encoding**: Applied to categorical features (Sex, Ascites, Drug, Hepatomegaly, Spiders, Edema, Status) to convert them into a numerical format. Stage was also encoded.
      * **Multi-class Classification**: The target variable Stage has four distinct categories (1, 2, 3, 4).
      * **Models Used**:
          * Logistic Regression, Ridge Classifier, SVC, Random Forest, XGBoost, AdaBoost, Gradient Boosting, Bagging, Decision Tree.
  * **Best Accuracy**:
      * **53.6%** with Bagging Classifier.
      * **51.2%** with XGBoost Classifier.
      * **50.0%** with AdaBoost and Gradient Boosting Classifiers.
      * The low accuracies suggest that predicting the stage of cirrhosis from this dataset is a very challenging task, possibly due to the dataset's small size, the number of missing values, and the complexity of the disease.

-----

### Purpose and Applications

  * Assist medical professionals in the **preliminary diagnosis and staging of cirrhosis**.
  * Provide a tool for risk assessment and patient management.
  * Support data-driven research on the clinical markers of liver disease progression.
  * Serve as a foundational model for developing more comprehensive liver health prediction systems.

-----

### Installation

Clone the repository and download the dataset.

Install the necessary libraries:

```bash
pip install pandas numpy seaborn matplotlib scikit-learn xgboost
```

-----

### Collaboration

We welcome contributions to improve the project. You can help by:

  * Exploring more robust strategies for handling missing values, such as using an advanced imputation method.
  * Performing comprehensive hyperparameter tuning and cross-validation for all models.
  * Investigating the impact of different feature selection or transformation techniques on model performance.
  * Collecting a larger and more diverse dataset to enhance model generalization and reliability.
