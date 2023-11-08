# credit-risk-classification
Data Bootcamp Module 20 Challenge

## Overview of the Analysis

In this analysis, the purpose is to evaluate the performance of a machine learning (Logistic Regression) model used in a financial context, specifically for making lending decisions.   The goal is to assess the model's ability to predict the creditworthiness of loan applicants.  
The analysis involves the use of features related to applicants' financial information to predict whether a loan is likely to be healthy (label "0") or high-risk (label "1").

## Procedure

Step 1:  Read the `lending_data.csv` data from the `Resources` folder into a Pandas DataFrame.

Step 2:  Create the labels set (`y`)  from the “loan_status” column, and then create the features (`X`) DataFrame from the remaining columns.  

Step 3: Split the data into training and testing datasets by using `train_test_split`.  

Step 4: Create a Logistic Regression Model with the Original Data.  
* Fit a logistic regression model by using the training data (`X_train` and `y_train`).
* Save the predictions on the testing data labels by using the testing feature data (`X_test`) and the fitted model.
* Evaluate the model’s performance by generating a confusion matrix and printing the classification report.  
<br>

## Results
<br>

                     precision    recall  f1-score   support

                 0       1.00      1.00      1.00     18759
                 1       0.87      0.89      0.88       625
          accuracy                           0.99     19384
         macro avg       0.94      0.94      0.94     19384
      weighted avg       0.99      0.99      0.99     19384
<br>

#### Accuracy Scores:

The machine learning model achieved high accuracy scores, indicating its overall ability to classify loans correctly.

#### Precision and Recall Scores:

For Label "0" (healthy loans), precision, recall, and f1-score are all excellent (100%), indicating the model's high accuracy in identifying healthy loans with minimal false positives and false negatives.
For Label "1" (high-risk loans), precision and recall scores are good but not perfect (87%, 89%), suggesting some false positives and false negatives. The f1-score (88%) for Label "1" signifies a reasonable balance between precision and recall.
For further clarification please refer to the end of the `credit_risk_classification.ipynb` file.



## Summary
The machine learning model demonstrates strong performance in distinguishing between healthy and high-risk loans. For Label "0" (healthy loans), the model excels in terms of precision, recall, and f1-score, making it highly reliable in correctly identifying creditworthy applicants. For Label "1" (high-risk loans), while not perfect, the model maintains a good balance between precision and recall, showing the capability to identify potential high-risk applicants.

The performance of the model largely depends on the problem being addressed. If the primary concern is minimising the risk of approving high-risk loans (Label "1"), the model performs well but might still result in some false negatives. On the other hand, if the emphasis is on accurately identifying healthy loans (Label "0"), the model is exceptionally effective.

Based on the results, the model is recommended for use by the company, especially if they prioritise correctly identifying healthy loans. 
The model can be a valuable tool in streamlining the lending decision process, reducing the risk of approving high-risk loans and ultimately improving the company's overall loan portfolio quality.

If, however, there are critical concerns about false negatives for high-risk loans, additional measures may be considered, such as model recalibration or using alternative techniques to address the class imbalance in the dataset.
