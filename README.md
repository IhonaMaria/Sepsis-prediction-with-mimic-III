# PREDICTING SEPSIS AMONG ICU ADMISSIONS USING MIMIC-III DATA

### INTRODUCTION
This is a project I did in collaboration with my collegues Lloyd Linton Jones and Patryk Szpetnar for the Electronic Health Record course in the Biomedical Data Science Master. 
We were asked to choose a research question and use MIMIC-III database (https://physionet.org/content/mimiciii/1.4/) in order to solve it. 
Our curiosity led us to explore the field of sepsis, which is an overreaction of the immune system to an infection and that causes lots of hospital deaths. The objective of the project was to develop a machine learning model that was able to predict whether a patient admitted to the ICU had sepsis or not. 

### METHODOLOGY
- Dataset creation: Our university (URV) gave us access to the mimic-III database and we used SQL to select and merge information from the different tables. You can find the dataset used as "data.xlsx". There are several sheets in the excel file, so in order to read it in Python, remember to choose this option: sheet_name="full" to show the full dataset. The SQL code used to get the dataset used in this project can be found in the repository under the name **"EHR_dataset_creation_and_ML_groupA.ipynb"**.

- Exploratory data anlysis: This was done with Python and the objective was to gain valuabe insights on the data. Some specific variables that we thought were related with sepsis were studied and examined. The steps and the code followed can be found in **"EHR_data_analysis_groupA.ipynb"**.
  
- Modelling and prediction: In this part the data was preparated before the prediction model creation (label encoding, NaN imputing and normalization were attempted). The data was divided into train and test set and three algporithms were built and evaluated: XGBclassifier, Neural Network and K-nearest neighbours. Metrics like f1 score, AUC_ROC, recall and others were used to evaluate the models. 

### RESULTS AND DISCUSSION
The exporatory data anlysis revealed that sepsis patients exhibit higher heart rate, respiratory rate, creatinine, bilirubin, and lactate levels. However, some kind of standarization of the mean values would be interesting for further results. 
The results obtained have been surprisingly high given the low correlation values. The best algorithm was the XGBclassifier with an f1 score of 0,756. The processing, training and evaluation of the algorithm can be found in this file: **"EHR_dataset_creation_and_ML_groupA.ipynb"**. 

For a deeper discussion and more details on the methodology and the results feel free to read the paper named **"EHR_A3_Report_GroupA"** from the repository, where you will gain a better understanding and representation of the project. 
