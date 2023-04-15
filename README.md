# Module_12_assignment
Utilizing Supervised Learning to detect credit risk & fraud.


# Credit Risk & Supervised Learning

Within the financial industry there are millions of applicant who apply for credit loans, among them not everyone are considered eligible.
With a vast amount of applications coming in at a daily basis, it would be an extremely daunting task to manually check and evaluate every candidate who appears. Thankfully with the power of supervised machine learning, the amount of time and resources used to verify customer creditworthiness is greatly reduced.


___
## <u>Overview:</u>

The purpose of this analysis is to utilize supervised learning to aggregate a large set of data and determine whether a customer is considered eligible or carries a high risk of defaulting on a credit loan. 
Using a dataframe with over 77500+ applicants, the information will be processed and examined using a Logistic Regression model with the original dataset and a resampled dataset.

___

## <u>Results:</u>

* Logistic Regression model + Original Data:
    * Accuracy: 0.99 - The classification report listed the model with a very high accuracy but it's not a perfect 1.00
    * Precision: 1.00 eligible [0], 0.85 high risk [1] - For eligible cases the precision score was rated as a 1.00 but for high risk cases it's reported as 0.85, this would result in some false positives coming through.
    * Recall: 0.99 eligible [0], 0.91 high risk [1] - With a recall score of 0.99, the model is able to properly analyze positive eligible cases, in other case for high risk applicants the model has resulted a score of 0.91. 

___
* LogisticRegression model + Resampled Data:
    * Accuracy:  0.99 - Like the first model, the report for the resampled data also show the accuracy score as 0.99
    * Precision: 1.00 eligible [0], 0.84 high risk [1] - Compared to the original dataset the precision score for high risk loans has lowered from 0.85 > 0.84
    * Recall: 0.99 eligible [0], 0.99 high risk [1] - The largest change from the classification report, the recall score for high risk loans has increased from 0.91 > 0.99
        indicating a near perfect probability of detecting True Positives and eliminating False Negatives

---

## <u>Summary:</u>
From the results of the classification reports, the models share the same accuracy score but with some differences with the precision and recall results. The score for precision between the models is minor with the difference being 0.01.
The results for recall proved more note-worthy as the score improved from 0.91 in the original dataset into 0.99 running the model with resampled data. In conclusion, it would be more efficient to use the Logistic Regression model with the resampled data to further analyze the number of true positives to properly identify whether an applicant is eligible or high risk.
