## Credit_Risk_Analysis

# Overveiw of the analysis:
Credit Risk is hard to predict. In this project, we want to look at all the factors in our Loan_Stat.csv to help predict whether someone has a low or high risk. One method that data scientists use for this type of issue is creating a model and then evaluate and train the models that they create. 

In this specific project we are using imbalanced-learn and scikit-learn libraries to build models and evalute them using a resampling method. In the first couple of models I oversampled the data using randomoversampler and smote algorithms and undersample the data with the clustercentroid algorithm. In the remaining models I used a combination approach to over and undersample the data using smoteenn. Finally, I compared two machine learning models that minimize bias, balancedrandomforestclassifier and easyensembleclassifier.

# Results
* Naive Random Oversampling results: Our balanced accuracy test it 64%, the precision for the high_risk has a very low positivity at 1% and the recall is 71%
![image](https://user-images.githubusercontent.com/46943357/209397173-6cad5c17-7fca-41ec-a0df-d893b5bca0ef.png)

* SMOTE oversampling results: the accuracy score is 64.6%, the precision for the high_risk loans has a low positvity again at 1% and recall is 58% overall
![image](https://user-images.githubusercontent.com/46943357/209398166-b7983747-1594-48b7-ab70-88f61ddb6c76.png)

* Undersampling results: balanced accuracy score is 64.6% overall, the precision is at 99% and the recall is 40%
![image](https://user-images.githubusercontent.com/46943357/209398455-d61703c6-6c25-4b96-9b0d-f5aea1caca88.png)

* Combination(over and undersampling) results: balanced accuracy score is 64% the precision is 99% and the recall is 58% overall
![image](https://user-images.githubusercontent.com/46943357/209398649-81dd9e55-6d17-4d51-8f5d-a31e8245a806.png)

* Balanced Random Forest Classifier results: the accuracy score is 77.7% the precision is 99% and the recall is 88%
![image](https://user-images.githubusercontent.com/46943357/209399830-8280b336-3621-4419-9e53-8bbb965333fb.png)

* Easy Ensemble AdaBoost Classifier results: the accuracy score is 93.1% the precision is 99% and the recall is 94%
![image](https://user-images.githubusercontent.com/46943357/209399882-e1472647-bd29-4880-9f4b-1a2d39d67e47.png)

# Summary

In the first four models we undersampled, oversampled and did a combination of both to try and determine which model is best at predicting which loans are the highest risk. The next two models we resampled the data using ensemble classifiers to try and predict which which loans are high or low risk.

In our first four models our accuracy score is not as high as the ensemble classifiers and the recall in the oversampling/undersampling/mixed models is low as well. Typically in your models you want a good balance of recall and precision which is why I recommend the ensemble classifiers over the first four models. It appears that the Easy Ensemble had the best balance of all the models because of it's high accuracy score and good balance of precision and recall scores.

