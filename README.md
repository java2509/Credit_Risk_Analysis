# Credit_Risk_Analysis
### Overview of the loan prediction risk analysis:

Credit risk is an unbalanced classification problem, as good loans outnumber risky loans. Machine learning methods using imbalanced-learn and scikit-learn libraries are applied to train and test models with unbalanced classes and determine which model is superior at predicting credit risk. 

The following models ran for this analysis: 

- Logistic Regression - Random Oversampling
- Logistic Regression - SMOTE Oversampling
- Logistic Regression - Undersamping
- Logistic Regression - SMOTEEN Combination Over and Undersampling
- Easy Ensemble Classifier
- Balanced Random Forest Classifier


The following model outputs were analyzed for all 6 models.

- Accuracy score : measures how many observations in the testing set were correctly predicted by the model
  Accuracy = TP+TN/TP+FP+FN+TN
- Precision : measure of how reliable a positive classification is
  Precision = TP/(TP + FP)
- Recall/sensitivity : measure of predicted positive observations to the all observations in actual class
  Recall = TP / (TP + FN)
- F1 Score : weighted average of recall and precision (also known as the harmonic mean)
  F1 Score = 2( precision * sensitivity ) / (precision + sensitivity)

### Results:

1.) Naive Random Oversampling:

- Accuracy: 0.654

|  |Predicted( High Risk)| Predicted(Low Risk)|
| :---         |      :---      |       ---  |
| Actual (High Risk)|73   | 28  |
| Actual (Low Risk)| 7,069  | 10,035


|             | Precision | Recall | F1 Score|
| :---        |     :--- |    :---   |:---    |
| High Risk   | 0.01    | 0.72  |0.02
| Low Risk    | 1.00     | .059    | 0.74



2.) SMOTE Oversampling

- Accuracy: 0.66
 
|  |Predicted( High Risk)| Predicted(Low Risk)|
| :---         |      :---      |       ---  |
| Actual (High Risk)|64   | 37  |
| Actual (Low Risk)| 5,296  | 11,808


|             | Precision | Recall | F1 Score|
| :---        |     :--- |    :---   |:---    |
| High Risk   |   0.01  | 0.63   | 0.02 |
| Low Risk    |    1.00  | 0.69    | 0.82|


3.) Undersampling

- Accuracy: 0.54

|  |Predicted( High Risk)| Predicted(Low Risk)|
| :---         |      :---      |       ---  |
| Actual (High Risk)|70   | 31  |
| Actual (Low Risk)| 10,324  | 6,780|

|             | Precision | Recall | F1 Score|
| :---        |     :--- |    :---   |:---    |
| High Risk   | 0.01    | 0.69  | 0.01 |
| Low Risk    |  1.00   |  0.40   | 0.56|1

4.) Combination (Over and Under) Sampling SMOTEENN

- Accuracy: 0.64

|  |Predicted( High Risk)| Predicted(Low Risk)|
| :---         |      :---      |       ---  |
| Actual (High Risk)|73 | 28 |
| Actual (Low Risk)| 7,324 | 9,780 |


|             | Precision | Recall | F1 Score|
| :---        |     :--- |    :---   |:---    |
| High Risk   |   0.01  | 0.72  | 0.02|
| Low Risk    |    1.00  | 0.57 |0.73|

5.) Balanced Random Forest Classifier
- Accuracy: 0.79

|  |Predicted( High Risk)| Predicted(Low Risk)|
| :---         |      :---      |       ---  |
| Actual (High Risk)|71   | 30  |
| Actual (Low Risk)| 2,030  | 15,074

|             | Precision | Recall | F1 Score|
| :---        |     :--- |    :---   |:---    |
| High Risk   |  0.03   | 0.70   | 0.06|
| Low Risk    |   1.00   | 0.88    | 0.94|

6.) Easy Ensemble Classifier
- Accuracy: 0.93

|  |Predicted( High Risk)| Predicted(Low Risk)|
| :---         |      :---      |       ---  |
| Actual (High Risk)|93 | 8 |
| Actual (Low Risk)| 995 | 16,109 |

|             | Precision | Recall | F1 Score|
| :---        |     :--- |    :---   |:---    |
| High Risk   |   0.09  | 0.92  | 0.16|
| Low Risk    |    1.00  | 0.94 |0.97|


Summary:


