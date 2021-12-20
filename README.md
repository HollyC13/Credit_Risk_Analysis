# Credit_Risk_Analysis
Module_17

## Overview
Apply machine learning to a credit card credit dataset from LendingClub, a peer-to-peer lending services company, by using various resampling
methods to build and evaluate models to determine if they are useful in predicting credit risk.

### Results of Resampling Methods
#### Oversampling

- Naive Random Oversampling </p>

Precision (pre) and Recall (rec) Scores:
    <img src="https://github.com/HollyC13/Credit_Risk_Analysis/blob/57a1b83ecf2579b49aada4f5e5096ceefd485df0/Resources/NaiveRandomOversampling.png"> 
</p>
Balanced Accuracy Score: 0.65 </p>
Analysis:  Precision for high_risk is only 1% while the high number of low_risk data results in precision of 100%. Recall for both categories is in the low - mid 60%s.
</p>
<br>

- Synthetic Minority Oversampling Technique (SMOTE) </p>
Precision (pre) and Recall (rec) Scores:
    <img src="https://github.com/HollyC13/Credit_Risk_Analysis/blob/57a1b83ecf2579b49aada4f5e5096ceefd485df0/Resources/SMOTE.png"> 
</p>
Balanced Accuracy Score: 0.63 </p>
Analysis:  As with the Naive Random Oversampling method, Precision for high_risk is only 1% while the high number of low_risk data results in precision of 100%. Recall for both categories is in the low 60%s.
<br>

#### Undersampling

- ClusterCentroids </p>
Precision (pre) and Recall (rec) Scores:
    <img src="https://github.com/HollyC13/Credit_Risk_Analysis/blob/57a1b83ecf2579b49aada4f5e5096ceefd485df0/Resources/ClusterCentroids.png"> 
</p>
Balanced Accuracy Score:  0.53 </p>
Analysis:  As with our Oversampling methods, Precision for high_risk is only 1% while the high number of low_risk data results in precision of 100%.  Recall for high_risk is in the low 60%s while recall for low_risk drops to 45%.
<br>

#### Combination (Over and Under) Sampling

- SMOTEEN (Combination of SMOTE and Edited Nearest Neighbors (ENN) algorithms)</p>
Precision (pre) and Recall (rec) Scores:
    <img src="https://github.com/HollyC13/Credit_Risk_Analysis/blob/57a1b83ecf2579b49aada4f5e5096ceefd485df0/Resources/SMOTEENN.png"> 
</p>
Balanced Accuracy Score:  0.62</p>
Analysis:  As with our previous methods, Precision for high_risk is only 1% while the high number of low_risk data results in precision of 100%.  Recall for high_risk improves slightly to 70% while recall for low_risk improves slightly to 54%.
<br>


#### Ensemble Learners

- Balanced Random Forest Classifier </p>
Precision (pre) and Recall (rec) Scores:
    <img src="https://github.com/HollyC13/Credit_Risk_Analysis/blob/57a1b83ecf2579b49aada4f5e5096ceefd485df0/Resources/RandomForest.png"> 
</p>
Balanced Accuracy Score:  0.79</p>
Analysis:  Precision for high_risk improves minimally to 4% while low_risk remains at 100%.  Recall for high_risk is 67% while recall for low_risk improves signficantly to 91%.
</p>
<br>


- Easy Ensemble AdaBoost Classifier </p>
Precision (pre) and Recall (rec) Scores:
    <img src="https://github.com/HollyC13/Credit_Risk_Analysis/blob/57a1b83ecf2579b49aada4f5e5096ceefd485df0/Resources/AdaBoost.png"> 
</p>
Balanced Accuracy Score:  0.93</p>
Analysis:  Precision for high_risk improves minimally to 7% while low_risk remains at 100%.  Recall for high_risk improves significantly to 91% while recall for low_risk improves slightly to 94%.
<br>

### Summary
The two Ensemble Learner techniques clearly outperform the other resampling methods in this case.  If one of these had to be utilized, The Easy Ensemble AdaBoost Classifier appears to be the best option.  Unfortunately, precision for high_risk is extremely low for all techniques, including the Ensemble Learners.  As a result, I do not recommend using any of these six models to predict credit risk.
