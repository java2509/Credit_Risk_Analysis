# Credit_Risk_Analysis

Overview of the loan prediction risk analysis:

Credit risk is an inherently unbalanced classification problem, as good loans easily outnumber risky loans. Therefore, you’ll need to employ different techniques to train and evaluate models with unbalanced classes. Jill asks you to use imbalanced-learn and scikit-learn libraries to build and evaluate models using resampling.

Using the credit card credit dataset from LendingClub, a peer-to-peer lending services company, you’ll oversample the data using the RandomOverSampler and SMOTE algorithms, and undersample the data using the ClusterCentroids algorithm. Then, you’ll use a combinatorial approach of over- and undersampling using the SMOTEENN algorithm. Next, you’ll compare two new machine learning models that reduce bias, BalancedRandomForestClassifier and EasyEnsembleClassifier, to predict credit risk. Once you’re done, you’ll evaluate the performance of these models and make a written recommendation on whether they should be used to predict credit risk.


Results:


- Accurancy Score - ratio of correctly predicted observation to the total observations 
- Precision Score - 
- Recall Score (Sensitivity) -  Recall is the ratio of correctly predicted positive observations to the all observations in actual class
- F1 score, also called the harmonic mean, can be characterized as a single summary statistic of precision and sensitivity. The formula for the F1 score is the following:
F1 score = 2(Precision * Sensitivity)/(Precision + Sensitivity)


1.) Naive Random Oversampling:

|  |Predicted( High Risk)| Predicted(Low Risk)|
| :---         |      :---      |       ---  |
| Actual (High Risk)|73   | 28  |
| Actual (Low Risk)| 7,069  | 10,035











2.) SMOTE Oversampling

|  |Predicted( High Risk)| Predicted(Low Risk)|
| :---         |      :---      |       ---  |
| Actual (High Risk)|73   | 28  |
| Actual (Low Risk)| 7324  | 9780

3.) Undersampling

|  |Predicted( High Risk)| Predicted(Low Risk)|
| :---         |      :---      |       ---  |
| Actual (High Risk)|71   | 30  |
| Actual (Low Risk)| 2030  | 15074

4.) Combination (Over and Under) Sampling

|  |Predicted( High Risk)| Predicted(Low Risk)|
| :---         |      :---      |       ---  |
| Actual (High Risk)|71   | 30  |
| Actual (Low Risk)| 2030  | 15074


|  |Predicted( High Risk)| Predicted(Low Risk)|
| :---         |      :---      |       ---  |
| Actual (High Risk)|71   | 30  |
| Actual (Low Risk)| 2030  | 15074




|  |Predicted( High Risk)| Predicted(Low Risk)|
| :---         |      :---      |       ---  |
| Actual (High Risk)|93 | 8 |
| Actual (Low Risk)| 995 | 16109|



There is a bulleted list that describes the balanced accuracy score and the precision and recall scores of all six machine learning models

Summary:

There is a summary of the results



There is a recommendation on which model to use, or there is no recommendation with a justification
