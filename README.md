# Enhancing-Hospital-Efficiency-using-Machine-Learning.

## Project Overview
This project aims to predict the length of hospital stay for patients using machine learning techniques. The dataset consists of various features related to patients, hospitals, and treatment details. The goal is to build a predictive model that classifies the duration of the hospital stay into specific categories.

## Dataset
The dataset is split into two parts: train.csv and test.csv. The training set is used to train the model, and the test set is used to evaluate the performance of the model.

### Data Columns

case_id: Unique identifier for each case.

Hospital_code: Code for the hospital.

Hospital_type_code: Type of hospital.

City_Code_Hospital: Code for the city where the hospital is located.

Hospital_region_code: Region code of the hospital.

Available Extra Rooms in Hospital: Number of extra rooms available in the hospital.

Department: Department handling the case.

Ward_Type: Type of ward.

Ward_Facility_Code: Code for the ward facility.

Bed Grade: Grade of the bed.

patientid: Unique identifier for the patient.

City_Code_Patient: Code for the city where the patient is from.

Type of Admission: Type of admission.

Severity of Illness: Severity of the illness.

Visitors with Patient: Number of visitors with the patient.

Age: Age group of the patient.

Admission_Deposit: Deposit paid at the time of admission.

Stay: Duration of stay in the hospital (target variable in the training set).

## Data Preprocessing

### Handling Missing Values:

Filled missing values in the Bed Grade and City_Code_Patient columns with the mode of the respective columns.

### Encoding Categorical Variables:

Used LabelEncoder to transform categorical features into numeric values.

### Feature Engineering:

Created new features by counting occurrences of combinations of columns:
count_id_patient
count_id_patient_hospitalCode
count_id_patient_wardfacilityCode

### Splitting the Dataset:

Combined the training and test datasets for uniform preprocessing.
Separated the datasets back after preprocessing.
Model Training

### Algorithm: XGBoost Classifier

Parameters:

max_depth=4
learning_rate=0.1
n_estimators=800
objective='multi:softmax'
reg_alpha=0.5
reg_lambda=1.5
booster='gbtree'
n_jobs=4
min_child_weight=2
base_score=0.75


### Training and Evaluation:

Split the training data into training and validation sets.
Evaluated the model using accuracy score.

### Results
The model achieved an accuracy score of approximately 0.71 on the validation set.

## Predictions

Predictions were made on the test set.
The Stay column in the test set was replaced with predicted values and mapped back to their respective categories.

## Output
The final output is a CSV file containing the case_id and predicted Stay for the test dataset.


## Acknowledgements
Thanks to the data providers and everyone who contributed to this project.
