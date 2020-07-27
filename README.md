# linear_regression_salary
# Oversampling
## - Random Oversampler

The Balanced Accuracy Score is 0.774

Confusion Matrix:
TP = 76   FN = 25
FP = 3507 TN = 13597

Classification Report:

   pre       rec       spe        f1       geo       iba       sup

high_risk       0.02      0.75      0.79      0.04      0.77      0.60       101
  
low_risk       1.00      0.79      0.75      0.89      0.77      0.60     17104

avg / total       0.99      0.79      0.75      0.88      0.77      0.60     17205


## - SMOTE Oversampling

Balanced Accuracy Score: 0.767

Confusion Matrix:
TP = 74   FN = 27
FP = 3409 TN = 13695


Classification Report:

   pre       rec       spe        f1       geo       iba       sup

high_risk       0.02      0.73      0.80      0.04      0.77      0.58       101

low_risk       1.00      0.80      0.73      0.89      0.77      0.59     17104

avg / total       0.99      0.80      0.73      0.88      0.77      0.59     17205

# - Undersampling

Balanced Accuracy Score: 0.767

Confusion Matrix:
TP = 74   FN = 27
FP = 3409 TN = 13695

Classification Report:
          
   pre       rec       spe        f1       geo       iba       sup

high_risk       0.02      0.73      0.80      0.04      0.77      0.58       101

low_risk       1.00      0.80      0.73      0.89      0.77      0.59     17104

avg / total       0.99      0.80      0.73      0.88      0.77      0.59     17205

# Combination
## - SMOTEENN
Balanced Accuracy Score: 0.647

Confusion Matrix:
TP = 73   FN = 28
FP = 7342 TN = 9762

Classification Report:
 
   pre       rec       spe        f1       geo       iba       sup

high_risk       0.01      0.72      0.57      0.02      0.64      0.42       101

low_risk       1.00      0.57      0.72      0.73      0.64      0.41     17104

avg / total       0.99      0.57      0.72      0.72      0.64      0.41     17205

# Final Recommendation
The ideal algorithm is 100% accurate, but we could not use model to achieve for this loan project. In this analysis, we can minimize the number of false negatives to improve the accuracy, and it will help the company to track low risk loans quickly. 

The Random Oversampler method has the highest accuarcy 77.4%, which also has the lowest proportion of True Positives to False Negatives. However, the number of False Positives is very high, 3507. In this method, we tried to fast track loan approval by approving all negatives, but we will approve 97.9% of the High-Risk loans at the same time. It is not safe for the company to use this method. 

We also try to fast track loan rejections by rejecting high_risk loans. However, this also provides little benefit as the percent of the high_risk is low as 0.6%. Using the method, we can not save manhours.

I don't recommend using any of these methods until we can find a way to reduce the number of False Negatives.
