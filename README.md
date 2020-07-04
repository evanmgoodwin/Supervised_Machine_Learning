# Supervised_Machine_Learning

## Summary Analysis

### Naive Random Sampling
- Balanced Accuracy Score: 63.5%
- High Risk Precision Score: 0.01
- High Risk Recall Score: 0.59 

### SMOTE
- Balanced Accuracy Score: 64.7%
- High Risk Precision Score: 0.01
- High Risk Recall Score: 0.67

### Cluster Centroid
- Balanced Accuracy Score: 51.3%
- High Risk Precision Score: 0.01
- High Risk Recall Score: 0.63

### SMOTEENN
- Balanced Accuracy Score: 64.2%
- High Risk Precision Score: 0.01
- High Risk Recall Score: 0.69

<br>

  For this challenge, we were tasked with creating four different supervised machine learning algorithms, and analysing their performance. The precision scores for high risk values were all 0.01. When looking at the high risk values, this is not necessarily that important, as we're really looking at the recall scores. The recall score in this scenario is more important because we want to detect as many high risk values as possible, even if it means having false positives. Loan applicants who are low risk but were predicted as high risk can always reapply for a loan, but high risk applicants who were predicted as low risk and accepted will have a negative impact on the business.
  
  Looking at the classification reports, we can see that the F1 vales are impacted by the low precision scores. Most of the F1 scores for all the models are 0.01 or 0.02. For our analysis, we will focus on the balanced accuracy and high risk recall scores.
  
  Our two oversampling models (Naive Random Sampling and SMOTE) performed fairly similarly. The biggest difference was in the recall score; SMOTE's was 0.08 higher. One positive thing we can infer from this is that there is probably a low number of (or no) outliers. Since data values are interpolated in SMOTE, outliers can produce even more outliers, or data points that may be off the true dataset. Since the recall score is higher in the SMOTE model, it doesn't seem that any outliers had an impact on the sampling. 
  
  The Cluster Centroid model, our only standalone undersampling model, performed the worst. With such an imbalanced dataset, this is not entirely surprising. One of the inherent drawbacks of undersampling is that we get rid of useful data in the majority class, which will negatively impact the model's accuracy. The Cluster Centroid model had the lowest balanced accuracy score, at 51.3%.
  
  The SMOTEENN model, a combination model using oversampling and undersampling, generally performed the best. It has the highest recall score at 0.69, and the second highest balanced accuracy score at 64.2%.
  
  If we had to choose from one of the four models analysed, the recommendation would be to use the SMOTTEEN sample. As said before, the recall score of the high risk values plays the most important role in reviewing the models' effectiveness. One possible concern of any oversampling, overfitting, doesn't seem to be an issue in our case since none of the scores are close to or at 100%. That being said, none of these models are ideal. The accuracy scores alone, between 50% and 65%, do not make any of these very trustworthy. A larger dataset and more training is suggested to produce more accurate results. Further anaylsis with other machine learning algorithms would also help determine the best model to use. 
