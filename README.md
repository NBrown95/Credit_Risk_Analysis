# Credit Risk Analysis

## Overview of Project

For this project, we are employing different techniques to train and evaluate credit card data. Credit risk in inherently an unbalanced classification problem. This means that we oversampled the data using RandomOverSampler and SMOTE algorithms, undersampled the data with the ClusterCentroids algorithm, and a combination of both resampling techniques with the SMOTEENN algorithm. Then, we compared two new machine learning models that reduce bias call BalancedRandomForestClassifier and EasyEnsembleClassifier. We use these techniques to predict credit risk and then evaluate the performance of each model.

## Results

### RandomOverSampler

The following image shows the accuracy of the model as well as the confusion matrix and classification report for the RandomOverSampler model.

![RandomOverSampler](https://user-images.githubusercontent.com/81498850/129461902-c6feac72-344d-4f30-9f02-4052a86b0d16.png)

As we can see, this model had:
* A balanced accuracy score of 65%
*	A precision score of 99%
*	A recall score of 60%
*	An F1 score of 75%

The strength of this model is that it is very precise. This means that the model is very good at determining high credit risk.

### SMOTE

The following image shows the accuracy of the model as well as the confusion matrix and classification report for the SMOTE model.

![SMOTEOverSampler](https://user-images.githubusercontent.com/81498850/129461922-cbe572b9-f6cf-401c-81a0-d1773d648155.png)

As we can see, this model had:
*	A balanced accuracy score of 66%
*	A precision score of 99%
*	A recall score of 69%
*	An F1 score of 81%

This model was more accurate at predicting risk and had higher recall and F1 scores than the previous model. This model is also extremely precise.

### ClusterCentroids

The following image shows the accuracy of the model as well as the confusion matrix and classification report for the ClusterCentroids model.

![ClusterCentroids](https://user-images.githubusercontent.com/81498850/129461934-f2c20571-9743-4c6d-9306-e8fb7e41dce6.png)

As we can see, this model had:
*	A balanced accuracy score of 54%
*	A precision score of 99%
*	A recall score of 40%
*	An F1 score of 56%

Undersampling the data seemed to have made the model less accurate in its predictions while also lowering the recall score and F1 score.

### SMOTEENN 

The following image shows the accuracy of the model as well as the confusion matrix and classification report for the SMOTEENN model.

![SMOTEENNCombo](https://user-images.githubusercontent.com/81498850/129461944-0724e232-2407-45e0-a6ed-5e8a9d8026ff.png)

As we can see, this model had:
*	A balanced accuracy score of 66%
*	A precision score of 99%
*	A recall score of 58%
*	An F1 score of 73%

This model improved the prediction accuracy and recall from the undersampling model but failed to improve from the oversampling models. 

### BalancedRandomForestClassifier

The following image shows the accuracy of the model as well as the confusion matrix and classification report for the BalancedRandomForestClassifier model.

![BalancedRandomForestClassifier](https://user-images.githubusercontent.com/81498850/129461958-74af5162-9dc0-44aa-8d17-9ea2b7767a63.png)

As we can see, this model had:
*	A balanced accuracy score of 79%
*	A precision score of 99%
*	A recall score of 87%
*	An F1 score of 93%

This model seemed to predict credit risk very well. The accuracy score is much higher as well as a heightened recall and F1 score. 

### EasyEnsembleClassifier

The following image shows the accuracy of the model as well as the confusion matrix and classification report for the EasyEnsembleClassifier model.

![EasyEnsembleClassifier](https://user-images.githubusercontent.com/81498850/129461971-146c95f9-7020-44c0-b0bb-70d59a2da0c9.png)

As we can see, this model had:
*	A balanced accuracy score of 93%
*	A precision score of 99%
*	A recall score of 94%
*	An F1 score of 97%

This model was by far the most accurate of all the models we used. The scores for accuracy, precision, recall, and the F1 score were all above 90%.

## Summary 

All six of these models gave a precision score of 99%. This could be due to the imbalanced nature of the data and the resampling methods artificially inflate this number. However, some of these models outperformed the others with very high accuracy scores as well as high F1 scores. Undersampling the data with ClusterCentroids gave the worst predictions for credit risk. 

### Recommendation

The recommended model to predict credit risk with this dataset is EasyEnsembleClassifier. This model reduced bias greatly while resampling the data and achieved an accuracy score of over 90%. This model is accurate, precise, and sensitive and therefore, this model is recommended. 
