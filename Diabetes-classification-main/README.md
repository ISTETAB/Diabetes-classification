# Diabetes Classification Project
This project aims to classify patients as diabetic or non-diabetic based on various health attributes.  
The project was implemented in both Python and R programming languages.

## Project Collaborators
This project was done in collaboration with MohShahin.

## Dataset
The dataset used in this project is the Pima Indians Diabetes Database, which contains various health attributes of patients. The dataset can be found among the files.
  #### Introduction
  Diabetes is a widespread and pressing health issue globally, affecting millions of people today. The goal of the project is to develop a machine learning model capable of predicting the likelihood of an individual developing diabetes based on relevant observed features including but limited to: gender, age, smoking and other relevant factors in our dataset. This project is relevant to the team’s interests as each one of us is working with similar machine learning medical-applications such as iris diseases recognition and classification and choosing a project as such creates a cohesive learning experience for the team. Moreover, other factors that were considered while choosing this problem was the availability of well-documented datasets that readily available and the significance of issue in the health domain as 422 million people today suffer from diabetes, that is 0.52% of the word’s population.
  
  #### Dataset Selection and Description
  The chosen dataset for our model was carefully selected among multiple ones that were available. The selection focused on relevance of features in the dataset and the diversity of these features to encompass the most suitable range of features that also ensures a complexity challenging enough to reflect and apply our skills. Below is the detailed explanation of the data set used:
  
  #### Features:
  1. **Gender:**
     - Categorical variable representing the gender of the individual, i.e., males or females.
  
  2. **Age:**
     - Continuous variable indicating the age of the individual (ranging from as high as 80 years to as low as 0.08 years old).
  
  3. **Hypertension:**
     - A binary variable (0 or 1) that denotes the presence or absence of hypertension for the individuals.
  
  4. **Heart Disease:**
     - Binary variable (0 or 1) indicating whether the individual has or does not have a history of a heart disease.
  
  5. **Smoking History:**
     - Categorical variable that represents the smoking history of the individual, the three categories are (never, current, former).
  
  6. **BMI (Body Mass Index):**
     - Continuous variable measuring the body mass index, it provides insights to the individual weight status.
     - A BMI of 18.5 to 24.9 is considered to be healthy, anything above is considered overweight and anything below is underweight.
  
  7. **HBA1C Level:**
     - Continuous variable representing the level of glycosylated hemoglobin, an important of indicator of diabetes management.
     - Normal HBA1C values are considered to be below 5.7%, anyone with an HbA1c value of 5.7% to 6.4% is considered to be prediabetic, while diabetes can be diagnosed with a HbA1c of 6.5% or higher.
  
  8. **Blood Glucose Level:**
     - Continuous variable denoting the blood glucose level, a very critical parameter in diabetes diagnosis.
     - Expected values for normal fasting blood glucose level are between 70 mg/dl and 100 mg/dl. However, in our case, the data collected is not strictly meeting the fasting condition and so the common medical practice is to set the limit to 140 mg/dl for the highest normal range, and 200 mg/dl and above for concerning range, anything between is usually considered in the pre-diabetic phase.
  
  #### Rationale for Dataset Selection:
  
  - **Feature diversity and relevance:**
    - The dataset incorporates a wide array of different features that captures relative demographic (age, gender), medical history (heart diseases and hypertension), lifestyle choices (smoking) and relative health test metrics (BMI, HbA1c and blood glucose level).
  
  - **Real-World relevance:**
    - Attributes are all considerably relevant to our test including important health metrics that are conventionally used in the medical field to make a diabetes diagnoses.
  
  - **Balanced Target Variable:**
    - The dataset contains good balance in target variable distribution (Diabetes), preventing model bias and ensuring a more comprehensive outcome to our model.
  
  All in all, the selected dataset provides a rich but also challenging environment for developing a diabetes prediction model that encompasses a mass of features crucial for accurate and reliable predictions in the context of diabetes assessment.


## Model
This project uses a subclassed TensorFlow model that utilizes Dense layers followed by a sigmoid activation function.  
The model is written to be dynamic; therefore, optimizing it using optuna was easily feasible.  
In the optimization process, a custom F1 score is implemented where it is possible to control the weight of Recall according to the parameter Beta to improve the recall for the 
minority class.  
Finally, a custom threshold is picked that maximizes the F1 score, and the model is saved as TensorFlow Lite.  

## Project Report
The full report of the R implementation of this project can be found in the final_project.html file. To view the report, please download the file and open it in a web browser.  
As for the Python implementation, you can view it in the Jupyter Notebook directly.

## Results
The model achieved a macro average F1 score of 85% and a weighed average F1 score of 95% on the test set.
