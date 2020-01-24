
# 1. Amazon-Employee-Access-Challenge
This respository explores the implementation of different machine learning concepts (Feature Selection, Feature Encoding,Cross Validation, ROC_AUC, Classification Models etc.) by developing a ML solution with the dataset available from Amazon Employee Access Kaggle's Challenge. 
A link to the Kaggle for this competition can be found [here](https://www.kaggle.com/c/amazon-employee-access-challenge). 

# 2.Goal of the Project
The objective of this competition is to build a model, learned using historical data, that will determine an employee's access needs, such that manual access transactions (grants and revokes) are minimized as the employee's attributes change over time. The model will take an employee's role information and a resource code and will return whether or not access should be granted.

# 3 File Descriptions:

*AmazonEmployeeAccess.ipynb* - the code and explanation of the steps taken
*train.csv* - is the dataset used in this problem and included in the repository
*requirements.txt* - a list of packages used for this project

# 4.Solution Approach

The problem is treated as a classification problem as the final goal is to determine whether a employee should be a given access ('1) or not ('0'). The steps followed are as below-

**Step 1:** Import Packages and Dataset
>* Import packages for data pre-processing, visualization, modeling and evaulating the accuracy of the models.
>* Import the dataset to be used for analysis. Since its an old competition and submission is no longer accepted, only the *train.csv* data is imported for this analysis. The solution is then developed by splitting the *train.csv* dataset 50/50 for training and evaluating the models on unseen data.

**Step 2:** Feature Inspection
>* A quick inspection of the dataset shows to check features in the dataset are categorical\numerical and if any of them has any null values. This step helps to determine how the data should be processed prior applying a model.

**Step 3:** Feature Selection
>* To identify features that are critical for modeling, a feature selection step is performed using the univariate selection method from available scikit modules.

**Step 4:** Feature Encoding
>* Once the top 6 significant features are idenitified and uncenssary features are eliminated from the dataset, a hashing trick was applied to encode the categorical features prior applying different machine learning models to the dataset.

**Step 5:** Training Different Models and Performance Evaluation based on Cross Validation Scores
>* Four different classification were then applied on the training dataset and the best performing model was then selected based on the cross validation scores.

**Step 6:** Compute ROC curve with cross validation for Model Performance on Unseen Data
>* Once the best model is identified in the previous step, it is used to the predict on the test data obtained  from the 50/50 split. Accuracy  of the best model in predicting the test data is then calculating the ROC curve and AUC scores.

# 5.Conclusion
* Among the four classification models used, Random Forest was the best perofrming model in terms of CV score. The CV score helps to evaluate how the model would perform on unseen data. 

* When random forest model was applied to unseen data, the computed ROC_AUC score was 0.68 which is slightly les than the performance of the model (0.7057) on the training dataset. 

# 6.Future Work
 * Hyperparameter tuning of the classification models.
 * Reducing collision loss during hash encoding. 

