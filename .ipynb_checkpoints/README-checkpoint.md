##Auto Insurance 

##Project Description

In this notebook I focus on classifying whether or not an individual will file for a claim, given several features.This model can be extended for fraud detection,therefore preventing companies from making losses.

##Data Source

The data is avaible in two csv's one for train and another for test.The data was initially held for competition on "https://www.kaggle.com/c/auto-insurance-fall-2017/data".


##Exploratory Data Analysis

The data set consisted of a TARGET_FLAG column, which was to predicted based on features pertaining to the demographics information eg. AGE, SEX,EDUCATION,JOB etc. and to the information related to the vehicle owned eg CAR_TYPE,RED_CAR,CAR_AGE,URBANCITY etc.Several graphs in the initial part of the notebook explore the relationships among data.

##Preprocessing and Feature Engineering

###Missing Data:
???	Since the % of missing data in the train and test set never exeeds 10%,therefore in this notebook I have dropped the na values
###Column type:
???	Columns such as INCOME,HOME_VAL,BLUEBOOK and OLDCLAIM, have been cleaned to convert them object format to int type. This also included dropping symbols like "$"  and ","

##Modelling ,metrics and hyperparameter tuning
I tried several models in the pipeline such as Logistic Regression, SGD classifer,k-neighbors, Gaussian Na??ve Bayes, Lgbm, AdaBoost and Random Forest. Since the dataset is highly imbalanced in nature, I chose the Recall score as the primary metric and precision as the secondary.I also used Repeated Stratified Sampling to maintain the original ratio of the classes in the dataset.

GaussianNB, LGBM and AdaBoost are the top three performers.
I performed hyperparameter tuning on Ada Boost and obtained the following results
{'m__learning_rate': 0.01, 'm__n_estimators': 500}
The recall score was 63.3%

##Future Scope
???	So far the predictions were made by dropping the na rows,however we canimpute the same by using Bayesian imputer and Categorical Imputer from Sklearn
???	Model tuning can also be done on other better performing models

##Tools used
???	Python with Numpy,Pandas and Scikit Learn
???	Github
???	Jupyter Notebook




