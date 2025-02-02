# Diabetes Prediction Using Machine Learning
This project builds a machine learning model to predict whether a person has diabetes based on medical and demographic features.
## **About Diabetes**
Diabetes is a condition where blood glucose, or blood sugar, is elevated. It occurs when the body's insulin production or utilization is insufficient.

Glucose, derived from the food we eat, is normally broken down with the help of insulin—a crucial hormone facilitating glucose entry into our cells.

Unfortunately, diabetes arises when the body fails to produce enough insulin or cannot use it effectively. This leads to an accumulation of excess glucose in the blood, contributing to various health complications. Although there is no cure for diabetes, proactive steps can be taken to safeguard one's health.

## **Dataset Overview**
The dataset used is the [Diabetes Dataset](https://www.kaggle.com/datasets/johndasilva/diabetes) from Kaggle. This dataset contains multiple medical attributes that influence diabetes diagnosis.

The target variable in the dataset is 'Outcome,' where 0 represents no diabetes, and 1 indicates diabetes. Following are the attributes in the dataset taken.

- **Pregnancies**: Number of times pregnant
- **Glucose**: Glucose concentration in blood (plasma). 
    - Normal range: 4.0 to 5.4 mmol/L (72 to 99 mg/dL) and up to 7.8 mmol/L (140 mg/dL) 2 hours after eating.
- **Blood Pressure**: Diastolic blood pressure (mm Hg). 
    - Normal range: less than or equal to 120/80 mmHg.
- **SkinThickness**: Triceps skinfold thickness (mm). 
    - Standard values: 2.5mm (men) or about 20% fat; 18.0mm (women) or about 30% fat.
- **Insulin**: 2-Hour serum insulin (mu U/ml). 
    - Normal range: 16–166 mIU/L 2 hours after glucose administration.
- **BMI**: Body mass index (weight in kg / (height in m²)). 
    - underweight:BMI ≤ 18.5
    - normal weight: 18.5–24.9
    - overweight (25–29.9), obese (BMI ≥ 30).
- **DiabetesPedigreeFunction**: A function scoring diabetes likelihood based on family history.
- **Outcome (target variable)**: 0 — no diabetes, 1 — has diabetes.
- **Age**

## **Data Preprocessing**
- Loaded the dataset using Pandas library.
- Checked for missing values and handled them accordingly.
- Standardized numerical features using StandardScaler.

Missing values before and after data preprocessing
|Before Preprocessing | After Preprocessing |
|----------------------|----------|
 <img src="images\missing_values_before.png" width="350" height="400">| <img src="images\missing_values_after.png" width="350" height="400"> 

## **Model Training and Evaluation**
- Implemented Logistic Regression as a baseline model.
- Implemented Random Forest Classifier for improved performance.
- Split the dataset into training (80%) and testing (20%).
- Evaluated Accuracy, Precision, Recall, and F1-Score as performance metrics.
- Plotted confusion metrices for both models.
- Generated ROC curve to visualize model perfomance.

| Model                | Accuracy | Precision | Recall | F1-Score |
|----------------------|----------|-----------|--------|----------|
| Logistic Regression | .7875   | .7708    | .5401 | .6352   |
| Random Forest       | .9710   | .9710    | .9781 | .9745   |

### Confusion metrices
|Logistic Regression | Random Forest|
|----------------------|----------|
<img src="images\lr_cm.png" width="350" height="300"> |<img src="images\rf_cm.png" width="350" height="300"> 

### ROC curves
|Logistic Regression | Random Forest|
|----------------------|----------|
<img src="images\lr_roc.png" width="350" height="300"> |<img src="images\rf_roc.png" width="350" height="300"> 






