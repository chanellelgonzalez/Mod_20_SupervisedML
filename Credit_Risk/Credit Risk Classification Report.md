# Module 12 – Credit Risk Classification Report

## Overview of the Analysis

 Machine Learning models are wonderful tools to use in predicting outcomes. For our purposes today, we are using these models to see if we can predict the health of loans in our database based on the loan's features. Obviously, we want to avoid costs and losses from risky loans as much as possible, so if we can accurately predict at risk loans, we can avoid the pitfalls of potential defaults, charge-offs and foreclosures.  
 
 In this sample of our data, we pulled out some standard features we can expect each loan to contain and we thought would be a significant varible in predicting a loans health, such as: loan size, interest rate, borrower income, DTI, number of accounts, derogatory marks, total debt. Of course, we pulled out the current loan status, healthy or risky, for each loan to compare with the final results and validate the models' performance. 

 Once the original data sample set is pulled, we split the sample into two samples to feed the model. The first is called a training sample used to "train" the model. We give it the features and the answer, so it can build the initial relationships. The training subset is the majority of the data at about 85% the total sample. The remaining 15% of the original sample is called a test data sample. Once the model is trained, we run the test data features through the model and match the predictions to the actual loan status. 
 
 And because it never hurts to get a second opinion, in addition to the initial logistic regression model, we ran it through the logistic regression model again. However, on the second run, we upped the ante and used an oversampling method with the training data sample. Fortunately for all of us, we have a lot more healthy loans than risky ones. Unfortunately, in modeling lower sample sizes on one side or the other can affect the performance of a model. This "oversampling" method allows us to randomly duplicate the risky loans, so the number of loans is balanced and even on both sides, healthy and risky.  
 
## Results

•	Machine Learning Model 1 – Initial Data:
o	Overall Accuracy: 99.24%
o	Precision:
  - Healthy Predictions: 100%
  - Risky Projections: 87%
o	Recall: 
  - Healthy Predictions: 100%
  - Risky Projections: 89%

•	Machine Learning Model 2 – Oversampling Data:
o	Overall Accuracy: 99.52%
o	Precision:
  - Healthy Predictions: 100%
  - Risky Projections: 87%
o	Recall: 
  - Healthy Predictions: 100%
  - Risky Projections: 100%

## Summary

As is easy to see from the results above, both of the models did a pretty good job at accurately predicting overall outcomes. When we get down into looking at how it breaks out when predicting healthy and risky loans, we start to see a difference. 

The logistic model run on the original data was good, but we thought we could do better. Since our goal here is to accurately predict risky loans, we went for the second opinion and I am glad we did. When adding the additional samples to the risky side of the data set, we were able to increase accuracy a little, and we got the recall up to 100% for the risky loans.  

On the whole, I believe that this logistic model with oversampling, has a near perfect result and I am excited to see what we can do with it!

