# Project 2: Predictive Analysis for Cardiovascular Disease
Author: Amin

## Problem Statement

A hospital wanted to study its list of patients and determine what factors influenced whether a patient had a cardiovascular disease or not. 

It wanted to come up with a profile of its patients, particularly those with the disease. Furthermore, in getting this profile, they can determine a future patient's risk of developing a cardiovascular disease based on his/her own profile. 

As part of a team that does analysis for the healthcare sector, this project seeks to understand the patient profile for this hospital and determine factors that would influence a patient in having a cardiovascular disease. In addition to that, this project also seeks to come up with a model to assist the hospital in predictive analysis for future patients. These two goals would allow the hospital to better advise future patients what risk they fall under. 

**About the Dataset**

Data description
There are 3 types of input features:

Objective: factual information.  
Examination: results of medical examination.  
Subjective: information given by the patient.  

The dataset consists of 70,000 records of patients data, 11 features + target.

**Features**:  
1. Age | Objective Feature | age | int | days
2. Height | Objective Feature | height | int | cm
3. Weight | Objective Feature | weight | float | kg
4. Gender | Objective Feature | gender | categorical | Male/Female
5. Systolic blood pressure | Examination Feature | ap_hi | int
6. Diastolic blood pressure | Examination Feature | ap_lo | int
7. Cholesterol | Examination Feature | cholesterol | 1: normal / 2: above normal / 3: well above normal
8. Glucose | Examination Feature | gluc | 1: normal / 2: above normal / 3: well above normal
9. Smoking | Subjective Feature | smoke | int | binary
10. Alcohol intake | Subjective Feature | alco | int | binary
11. Physical activity | Subjective Feature | active | int | binary
12. Presence or absence of cardiovascular disease | Target Variable | cardio | int | binary

**Data Source**: https://www.kaggle.com/datasets/sulianova/cardiovascular-disease-dataset


## Objectives: 

1) Determine the patient profile of those with and without a cardiovascular disease by looking at their lifestyle choices and/or risk factors.  

2) Create a model that would be able to predict whether an individual has a cardiovascular disease or not.  


## Conclusion  

**Objectives**:  

1) Determine the patient profile of those with and without a cardiovascular disease by looking at their lifestyle choices and/or risk factors.  

- **Age**: Generally, across all variables, individuals around the age of 55 years old tend to have a cardiovascular disease irregardless of lifestyle choices and/or risk factors.  

- **BMI**: With respect to all other variables, individuals with higher BMI tend to have cardiovascular disease. When compared to the target variable, **higher** BMI also showed **higher** likelihood of having cardiovascular disease.  

- **Cholesterol**: Noticeable difference were observed between individuals with and without cardiovascular disease.  

    - Count of individuals with normal cholesterol levels are **lesser** in diseased group.  
    - Count of individuals with above normal cholesterol levels are **more** in diseased group.  
    - Count of individuals with way above cholesterol levels are **more** in diseased group.  
    
- **Glucose**: Slight difference observed between individuals with and without cardiovascular disease.  

    - Count of individuals with normal glucose levels are **lesser** in diseased group.  
    - Count of individuals with above normal glucose levels are **more** in diseased group.  
    - Count of individuals with way above glucose levels are **more** in diseased group.  
    
- **Activity**: Slight difference observed between individuals with and without cardiovascular disease.  

    - Count of individuals who are active are **lesser** in diseased group.  
    - Count of individuals who are not active are **more** in diseased group.  
    
- All other variables showed **little/negligible** difference between individuals with and without cardiovascular disease.  


2) Create a model that would be able to predict whether an individual has a cardiovascular disease or not.  
- **XGBoost** is the best model out of all for the prediction of cardiovascular disease.  

    - **Recal**l is the more important metric for this project. XGBoost had the best at 0.72 without any hyperparameter tuning  
    - Has an **accuracy** of 0.73  
    - Has an **ROC AUC** of 0.73  
    - Has a **f1-score** of 0.72  


**Next Steps**: 

1) Tuning the hyperparameters did little to no improvement across all metrics used.  
    - Better refinement of this process needs to be done.  
    
2) Reduce the number of features using techniques like PCA or SelectKBest, and only take in the best features to run in our models.  

3) Additional data could be included.  
    - Currently, only individuals's lifestyle choices and risk factors were provided. Presence of co-morbidities like diabetes or stroke could be included so that it can be fed into our models to get better results.  
