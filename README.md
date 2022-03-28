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

- Accuracy score : measures how many observations in the testing set were correctly predicted by the model (i.e the higher the better)
  Accuracy = TP+TN/TP+FP+FN+TN
- Precision : measure of how reliable a positive classification is (i.e the higher the better
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
| Actual (Low Risk)| 7,324 | 9,780


|             | Precision | Recall | F1 Score|
| :---        |     :--- |    :---   |:---    |
| High Risk   | 0.01    | 0.72  |0.02
| Low Risk    | 1.00     | .057    | 0.73

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

Screenshots of results below


1.) Naive Random Oversampling:
![Naive Random Oversampling](https://user-images.githubusercontent.com/93900628/160312317-b8863a91-b298-42df-bd84-f94d13700653.png)

2.) SMOTE Oversampling
![Screen Shot 2022-03-27 at 8 43 39 PM](https://user-images.githubusercontent.com/93900628/160312628-13a2de46-592f-4d51-87e0-fc14cc3f0557.png)

3.) Undersamping
![Screen Shot 2022-03-27 at 8 46 01 PM](https://user-images.githubusercontent.com/93900628/160312839-38b58e6b-55ea-4e88-b687-9f0889058214.png)

4.) SMOTEEN Combination Over and Undersampling
![Screen Shot 2022-03-27 at 8 46 56 PM](https://user-images.githubusercontent.com/93900628/160312900-21986cb1-e4ca-4ee2-a690-c545e985e8cb.png)

5.) Easy Ensemble Classifier
![Screen Shot 2022-03-27 at 8 48 38 PM](https://user-images.githubusercontent.com/93900628/160313010-1819f1f6-408c-459f-ba39-8b03b531309b.png)

6.) Balanced Random Forest Classifier
![Screen Shot 2022-03-27 at 8 51 20 PM](https://user-images.githubusercontent.com/93900628/160313289-157be44c-d4f0-4104-b0fa-3519922f4483.png)


Analyzing the results we can conclude the following:

1.) Accuracy: The Easy Ensemble Classifier model has the highest accuracy of 0.93, with the Balanced Random Forest Classifier has an accuracy rate of 0.79

2.) Precision: All the models have an average precision of 0.99 which means that the models correctly identified the majority of high-risk loan applications.

3.)Recall: The Easy Ensemble Classifier has an average recall score of 0.94 which is the highest of all the different methods.

4.) F1 Score: The Easy Ensemble Classifier has an average recall score of 0.97 which is the highest of all the different method which also means that there is not a huge imbalance between the precision and recall scores.

In conclusion based on the above metrics above I would recommend using the Easy Ensemble Classifier method to predict the Credit Risk.






