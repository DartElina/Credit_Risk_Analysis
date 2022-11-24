# Credit Risk Analysis
## Overview of the loan prediction risk analysis:
Predicting credit risk is an imbalanced classifaction problem since default is relatively rare compared to good loans. Jill has asked us to apply imbalanced-learn and scikit-learn libraries to build and evaluate models using resampling. 

It is our aim to identify a machine learning model that will accurately predict bad loans, and minimize the number of mislabeled good loans. 

## Results:
### Oversampling Models
#### Naive Random OverSampling Results:
![naive random oversample](https://github.com/DartElina/Credit_Risk_Analysis/blob/aa1654a5591c29d7885e6ad0be74358bc67ad0a9/images/Naive%20Random%20Oversampling%20results.png)
- Accuracy: 64%
- Precision: 1%
- Recall: 66%
- f1 score: .02

Accuracy is 64%, however precison of high risk loans is 1%. This means the model is extremely unreliable in predicting bad loans. 

#### SMOTE Oversampling Results:
![Somte over sampling](https://github.com/DartElina/Credit_Risk_Analysis/blob/aa1654a5591c29d7885e6ad0be74358bc67ad0a9/images/Smote%20Over%20sample%20Results%20.png)
- Accuracy: 65%
- Precision: 1%
- Recall: 66%
- f1 score: .02

This model is similarly unreliable as the previous model. 

### Undersampling Models
#### Cluster Centroids Results:
![Cluster](https://github.com/DartElina/Credit_Risk_Analysis/blob/aa1654a5591c29d7885e6ad0be74358bc67ad0a9/images/Under%20sample%20Results%20.png)
- Accuracy: 54%
- Precision: 1%
- Recall: 61%
- f1 score: .02

Undersampling has less desirable results than oversampling. 

### Combination Over and Under Sampling Models
#### SMOTEEN Results:
![SMOTEEN](https://github.com/DartElina/Credit_Risk_Analysis/blob/aa1654a5591c29d7885e6ad0be74358bc67ad0a9/images/Combo%20over%20Under%20Sample%20results.png)
- Accuracy: 64%
- Precision: 1%
- Recall: 72%
- f1 score: .02

The combiation model also struggles to identify the bad loans. The recall has increased, however a high recall percentage indicates a high number of false postives, meaning this model flags good loans as bad loans, and still fails to accurately predict bad loans. 

### Ensemble Models
#### Balanced Random Forest Results:
![BRF](https://github.com/DartElina/Credit_Risk_Analysis/blob/aa1654a5591c29d7885e6ad0be74358bc67ad0a9/images/Balanced%20Random%20Forst%20Results%20.png)
- Accuracy: 79%
- Precision: 4%
- Recall: 67%
- f1 score: .07

The Balanced Random Forest has performed better than all the previous models. The Accuracy score is significantly higher. The precision score has quadrupled, which isn't saying much since the previous models were so low. 4 percent is still failing to identify bad loans. 

#### Easy Ensemble Classifier Results: 
![EEC](https://github.com/DartElina/Credit_Risk_Analysis/blob/aa1654a5591c29d7885e6ad0be74358bc67ad0a9/images/Easy%20Ensemble%20Classifier%20Results%20.png)
- Accuracy: 93%
- Precision: 7%
- Recall: 91%
- f1 score: .14

The Easy Ensemble Calssifier performs even better than the Balanced Random Forest Model. The accuracy score is very high. This is good. The precision score is however still below 10%. The F1 score has increased to .14. 
## Summary:

The model that has performed the best is the Easy Ensemble Classifier. As you can see in cunfusion matrices the last model labeled 979 good loans as bad loans. These are loans that would be denied with this model that have not defaulted. Compared to the worst performing model that mislabeled 10,347 this is a huge improvement! Additionally the last model minimized the number of mislabelled bad loans as well. The 93% accuracy score also indicates that this model is very successful. 

I recommend using the Easy Ensemble Classifier to predict bad loans. 
