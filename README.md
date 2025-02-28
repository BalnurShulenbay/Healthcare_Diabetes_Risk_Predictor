# Diabetes Prediction Model

## Overview
This project develops and compares various machine learning models to predict diabetes based on health metrics from the National Health and Nutrition Examination Survey (NHANES) dataset. The models classify individuals into three categories based on their glycohemoglobin (HbA1c) levels:
- Normal (HbA1c < 5.7%)
- Prediabetes (5.7% ≤ HbA1c ≤ 6.4%)
- Diabetes (HbA1c ≥ 6.5%)

## Dataset
The analysis uses data from multiple NHANES datasets:
- Demographic information
- Laboratory results
- Examination measurements
- Diet information
- Health questionnaire responses
# Diabetes Prediction using demographic data and body measurements

# About our data

The [National Health and Nutrition Examination Survey (NHANES)](https://www.cdc.gov/Nchs/Nhanes/about_nhanes.htm) is a program of studies designed to assess the health and nutritional status of adults and children in the United States. The survey is unique in that it combines interviews and physical examinations. NHANES is a major program of the National Center for Health Statistics (NCHS). NCHS is part of the Centers for Disease Control and Prevention (CDC) and has the responsibility for producing vital and health statistics for the Nation.

The NHANES program began in the early 1960s and has been conducted as a series of surveys focusing on different population groups or health topics. In 1999, the survey became a continuous program that has a changing focus on a variety of health and nutrition measurements to meet emerging needs. The survey examines a nationally representative sample of about 5,000 persons each year. These persons are located in counties across the country, 15 of which are visited each year.

The NHANES interview includes demographic, socioeconomic, dietary, and health-related questions. The examination component consists of medical, dental, and physiological measurements, as well as laboratory tests administered by highly trained medical personnel.

To date, [thousands of research findings have been published using the NHANES data.](https://www.ncbi.nlm.nih.gov/pubmed?orig_db=PubMed&term=NHANES&cmd=search)

Content
The 2013-2014 NHANES datasets include the following components:

**1. Demographics dataset:**

A complete variable dictionary can be found [here](https://wwwn.cdc.gov/Nchs/Nhanes/Search/variablelist.aspx?Component=Demographics&CycleBeginYear=2013)

**2. Examinations dataset, which contains:**

Blood pressure

Body measures

Muscle strength - grip test

Oral health - dentition

Taste & smell

A complete variable dictionary can be found [here](https://wwwn.cdc.gov/Nchs/Nhanes/Search/variablelist.aspx?Component=Examination&CycleBeginYear=2013)

**3. Dietary data - total nutrient intake, first day:**

A complete variable dictionary can be found [here](https://wwwn.cdc.gov/Nchs/Nhanes/Search/variablelist.aspx?Component=Dietary&CycleBeginYear=2013)

**4. Laboratory dataset, which includes:**

Albumin & Creatinine - Urine

Apolipoprotein B

Blood Lead, Cadmium, Total Mercury, Selenium, and Manganese

Blood mercury: inorganic, ethyl and methyl

Cholesterol - HDL

Cholesterol - LDL & Triglycerides

Cholesterol - Total

Complete Blood Count with 5-part Differential - Whole Blood

Copper, Selenium & Zinc - Serum

Fasting Questionnaire

Fluoride - Plasma

Fluoride - Water

Glycohemoglobin

Hepatitis A

Hepatitis B Surface Antibody

Hepatitis B: core antibody, surface antigen, and Hepatitis D antibody

Hepatitis C RNA (HCV-RNA) and Hepatitis C Genotype

Hepatitis E: IgG & IgM Antibodies

Herpes Simplex Virus Type-1 & Type-2

HIV Antibody Test

Human Papillomavirus (HPV) - Oral Rinse

Human Papillomavirus (HPV) DNA - Vaginal Swab: Roche Cobas & Roche Linear Array

Human Papillomavirus (HPV) DNA Results from Penile Swab Samples: Roche Linear Array

Insulin

Iodine - Urine

Perchlorate, Nitrate & Thiocyanate - Urine

Perfluoroalkyl and Polyfluoroalkyl Substances (formerly Polyfluoroalkyl Chemicals - PFC)

Personal Care and Consumer Product Chemicals and Metabolites

Phthalates and Plasticizers Metabolites - Urine

Plasma Fasting Glucose

Polycyclic Aromatic Hydrocarbons (PAH) - Urine

Standard Biochemistry Profile

Tissue Transglutaminase Assay (IgA-TTG) & IgA Endomyseal Antibody Assay (IgA EMA)

Trichomonas - Urine

Two-hour Oral Glucose Tolerance Test

Urinary Chlamydia

Urinary Mercury

Urinary Speciated Arsenics

Urinary Total Arsenic

Urine Flow Rate

Urine Metals

Urine Pregnancy Test

Vitamin B12

A complete data dictionary can be found [here](https://wwwn.cdc.gov/Nchs/Nhanes/Search/variablelist.aspx?Component=Laboratory&CycleBeginYear=2013)

**Questionnaire dataset, which includes information on:**

Acculturation

Alcohol Use

Blood Pressure & Cholesterol

Cardiovascular Health

Consumer Behavior

Current Health Status

Dermatology

Diabetes

Diet Behavior & Nutrition

Disability

Drug Use

Early Childhood

Food Security

Health Insurance

Hepatitis

Hospital Utilization & Access to Care

Housing Characteristics

Immunization

Income

Medical Conditions

Mental Health - Depression Screener

Occupation

Oral Health

Osteoporosis

Pesticide Use

Physical Activity

Physical Functioning

Preventive Aspirin Use

Reproductive Health

Sexual Behavior

Sleep Disorders

Smoking - Cigarette Use

Smoking - Household Smokers

Smoking - Recent Tobacco Use

Smoking - Secondhand Smoke Exposure

Taste & Smell

Weight History

Weight History - Youth

A complete variable dictionary can be found [here](https://wwwn.cdc.gov/Nchs/Nhanes/Search/variablelist.aspx?Component=Questionnaire&CycleBeginYear=2013)

**6. Medication dataset, which includes prescription medications:**

A complete variable dictionary can be found [here](https://wwwn.cdc.gov/Nchs/Nhanes/Search/variablelist.aspx?Component=Questionnaire&CycleBeginYear=2013)
## Data Preprocessing
The preprocessing pipeline includes:
- Merging multiple data sources
- Handling missing values
- Feature selection and engineering
- Converting glycohemoglobin levels to diabetes classification labels

## Features Used
The final model uses these key features:
- Gender
- Years in US (binary)
- Family income
- Arm circumference
- Sagittal abdominal diameter
- Grip strength
- Breastfeeding history

## Models Implemented
Several machine learning algorithms were implemented and compared:
1. Logistic Regression
2. AdaBoost with Decision Tree base
3. Bagging with Decision Tree base
4. Bagging with K-Nearest Neighbors
5. Multi-Layer Perceptron (Neural Network)

## Results
The models achieved the following accuracy scores on the test set:
- MLP: 78.44%
- Logistic Regression: 78.36%
- Bagging with KNN: 78.34%
- Bagging with Decision Tree: 76.58%
- AdaBoost: 64.49%

The MLP classifier with a (100, 50) hidden layer architecture performed the best, though the difference between the top three models is minimal.

## Requirements
- Python 3.x
- pandas
- numpy
- matplotlib
- seaborn
- scikit-learn

## Usage
To run the model:
```python
# Import the file
from diabetes_prediction_model import *

# Train the model with your own data
# X_train, y_train = your_data
# model.fit(X_train, y_train)

# Make predictions
# predictions = model.predict(X_test)
```

