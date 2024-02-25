# Diabetes Classification Project
This project aims to classify patients as diabetic or non-diabetic based on various health attributes.  
The project was implemented in both Python and R programming languages.

## Project Collaborators
This project was done in collaboration with MohShahin.

## Dataset
The dataset used in this project is the Pima Indians Diabetes Database, which contains various health attributes of patients. The dataset can be found among the files.

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
The model achieved an accuracy of 98% on the dataset as well as 98% on every other metric (Precision, recall, f1 score) for both the positive and the negative class.
