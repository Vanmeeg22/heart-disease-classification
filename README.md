# Predicting heart disease using machine learning

This notebook looks into using various Python-based machine learning and data science libraries in an attempt to build a machine learning model capable of predicting whether or not someone has heart disease based on their medical attributes.

We're going to take the following approach:
1. Problem definition
2. Data
3. Evaluation
4. Features
5. Modelling
6. Experimentation

## 1. Problem Definition

In a statement,
> Given clinical parameters about a patient, can we predict whether or not they have heart disease?

## 2. Data
The original data came from Cleveland data from the UCI Machine Learning Repository. https://archive.ics.uci.edu/dataset/45/heart+disease

There is also a version of it available on Kaggle. https://www.kaggle.com/datasets/redwankarimsony/heart-disease-data

## 3. Evaluation
> If we can reach 95% accuracy at predicting whether or not a patient has heart disease during the proof of concept, we'll pursue the project.

## 4. Features

**Data dictionary**

1. `age` Age of the patient in years
2. `sex` Male/Female
3. `cp` chest pain type
   * 0: Typical angina - chest pain related decrease blood supply to the heart
   * 1: Atypical angina - chest pain not related to heart
   * 2: Non-anginal pain - typically esophageal spasms (non heart related)
   * 3: Asymptomatic - chest pain not showing signs of disease
4. `trestbps` resting blood pressure (in mm Hg on admission to the hospital)
5. `chol` serum cholesterol in mg/dl
6. `fbs` (if fasting blood sugar > 120 mg/dl) (1 = True; 0 = False)
    * (blood sugar > 126 mg/dl) signals diabetes
7. `restecg` resting electrocardiographic results
    * 0: Normal
    * 1: ST-T Wave Abnormality
        * Can range from mild symptoms to severe problems
        * Signals non-normal heart beat
    * 2: Left ventricular hypertrophy
        * Enlarged heart's main pumping chamber
8. `thalach` maximum heart rate achieved
9. `exang` exercise induced angina (1 = True; 0 = False)
10. `oldpeak` ST depression induced by exercise relative to rest
11. `slope` the slope of the peak exercise ST segment
    * 0: Upsloping - better heart rate with exercise (uncommon)
    * 1: Flatsloping - minimal change (typical healthy heart)
    * 2: Downsloping - signs of unhealthy heart
12. `ca` number of major vessels (0-3) colored by fluoroscopy
    * colored vessels means the doctor can see the blood passing through.
    * the more blood movement the better (no clots)
13. `thal` thalium stress result
    * 1, 3: normal
    * 6: fixed defect - used to be defect but ok now
    * 7: reversible defect - no proper blood movement when exercising
14. `num` have disease or not (1 = Yes; 0 = No) (the predicted attribute)