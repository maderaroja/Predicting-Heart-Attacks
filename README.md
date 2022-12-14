# Predicting Heart Attacks

According to the [Government of Canada](https://www.canada.ca/en/public-health/services/publications/diseases-conditions/heart-disease-canada.html):
- every hour about 14 Canadian adults, age 20 and over with diagnosed heart disease, die.

This makes heart disease, and in this specific case: heart attack, an important issue with which to treat.

The present project works with a sample of real world publicly available health data pertaining to heart attacks. The goal is to explore a predictive model for heart attacks. This model employs various health related biometrics.

## 1. An Exploratory Data Analysis (EDA)
An EDA is included that aims to provide an understanding of the dataset and what challenges or issues it may contain. This allows for the use of data visualizations to further describe the data and feature relationships within it.

## 2. A Random Forest Predictive Model
A random forest predictive model is used because it provides better accuracy (tradeoff) than other classifiers, which includes a lower risk of over-fitting. The data includes categorical features, which might result in a bias (tradeoff) of the random forest algorithm. This does not heavily disadvantage the exploratory intent of this project.

The aim of this model is to predict the likelihood of a patient getting a heart attack. All features, excepting the target feature (`Heart_attack`), are in play. This comprises:
- `age`
- `sex`
- `chest_pain`
- `Rblood_pressure`
- `cholesterol`
- `Fblood_sugar`
- `Rest_ECG`
- `Max_heart_rate`
- `exercize_angina`
- `oldpeak`
- `slope`
- `major_vessels`
- `TStress_result`
- `Blood_oxygen`

Some features could be left out in a refined version of this predictive model, such as slope. Further consultation is needed in order to determine the value, use, and relationship of this and other features with the target feature, `Heart_attack`.

## 3. Data Dictionary
A data dictionary is provided that explains each feature name.

| Attribute |  Description | 
|----------|:-------------:|
| age |  Age of the patient |
| sex |    Sex of the patient   |
| cp | Chest pain type ~ 0 = Typical Angina, 1 = Atypical Angina, 2 = Non-anginal Pain, 3 = Asymptomatic |
| trtbps | Resting blood pressure (in mm Hg) |
|chol | Cholestoral in mg/dl fetched via BMI sensor |
|fbs | (fasting blood sugar > 120 mg/dl) ~ 1 = True, 0 = False |
|restecg | Resting electrocardiographic results ~ 0 = Normal, 1 = ST-T wave normality, 2 = Left ventricular hypertrophy |
|thalachh | Maximum heart rate achieved |
|oldpeak | Previous peak|
| slp | Slope|
| caa | Number of major vessels|
| thall | Thalium Stress Test result ~ (0,3) |
| exng | Exercise induced angina ~ 1 = Yes, 0 = No |
| o2Saturation | Blood oxygen saturation (%) |
| output | Target variable|

The data was cleansed to reflect easy to understand feature names, to remove null values, and to correct dtypes.

## 4. Visualizations
Several visualizations were carried out as an exploratory step into the relationship among the features.

### Interactive Tooltip Barchart - interaction enabled when code is ran
<img src ="Figures/fig1.png" width="100%" />

### Numeric Features Plot
<img src ="Figures/numeric_plot.png" width="100%" />

### Correlation Plot
<img src ="Figures/cc_plot.png" width="100%" />

### Confusion Matrix
<img src ="Figures/confusion_matrix.png" width="100%" />


## 5. Production

This model can be placed into production via automation, using auto sklearn for example. At present, the model can be executed by running the DS_EDA.py or DS_EDA.ipynb files included here. Production is elaborated upon in these two files, as are each section of this README.md file.


