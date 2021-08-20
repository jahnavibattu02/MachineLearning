# Extreme Gradient Boosting Model(XGBoost)
## Prudential Life Insurance Decision Predicition.  

**Problem Statement:** 
Prudential, one of the largest issuers of life insurance in the USA.

In a one-click shopping world with on-demand everything, the life insurance application process is antiquated. Customers provide extensive information to identify risk classification and eligibility, including scheduling medical exams, a process that takes an average of 30 days.

By developing a predictive model that accurately classifies risk using a more automated approach, you can greatly impact public perception of the industry.
**Download the data here:** [Kaggle-Dataset]( https://www.kaggle.com/c/prudential-life-insurance-assessment/data)  

### Gradient Boosting Model  
We're now ready to train our gradient boosting machine (GBM) model. Here's how a GBM model works:

1. The average value of the target column and uses as an initial prediction every input.  
2. The residuals (difference) of the predictions with the targets are computed.  
3. A decision tree of limited depth is trained to predict just the residuals for each input.  
4. Predictions from the decision tree are scaled using a parameter called the learning rate (this prevents overfitting).  
5. Scaled predictions fro the tree are added to the previous predictions to obtain the new and improved predictions.  
6. Steps 2 to 5 are repeated to create new decision trees, each of which is trained to predict just the residuals from the previous prediction.  
- The term "gradient" refers to the fact that each decision tree is trained with the purpose of reducing the loss from the previous iteration (similar to gradient descent). The term "boosting" refers the general technique of training new models to improve the results of an existing model.   

###  Hyperparameter Tuning and Regularization before training the best fit model  
<img src="https://i.imgur.com/EJCrSZw.png" width="480">

Check out the following resources to learn more about hyperparameter supported by XGBoost:

- https://xgboost.readthedocs.io/en/latest/python/python_api.html#xgboost.XGBRegressor
- https://xgboost.readthedocs.io/en/latest/parameter.html.  
1. _n_estimators:_  
The number of trees to be created. More trees = greater capacity of the model.  
2. _max_depth:_ 
As you increase the max depth of each tree, the capacity of the tree increases and it can capture more information about the training set.  
3. _learning_rate:_
The scaling factor to be applied to the prediction of each tree. A very high learning rate (close to 1) will lead to overfitting, and a low learning rate (close to 0) will lead to underfitting.  
4. _booster:_
Instead of using Decision Trees, XGBoost can also train a linear model for each iteration. This can be configured using booster.  
### Machine Learning Workflow:
Workflow of the project:

- Downloading a real-world dataset from a Kaggle competition. 
- Exploring Data Analysis. 
- Data Preprocessing. 
- Training and interpreting a gradient boosting model using XGBoost. 
- Training with KFold cross validation and ensembling results. 
- Configuring the gradient boosting model and tuning hyperparamters. 
- Making Predictions on test dataset and Evaluation.  
<img src="https://www.deepnetts.com/blog/wp-content/uploads/2019/02/SupervisedLearning.png" width="400">
