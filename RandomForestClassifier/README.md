## Predicting Whether It Will Rain Tomorrow Using Random Forest Classifier. 

We Need to predict Whether it will rain tomorrow or not. We will use the dataset from the [Rain in Australia dataset](https://kaggle.com/jsphyg/weather-dataset-rattle-package) competition on [Kaggle](https://kaggle.com). This dataset contains about 10 years of daily weather observations from numerous Australian weather stations.
Here's a small sample from the dataset:
> 
> ![](https://i.imgur.com/5QNJvir.png)  

## Machine Learning WorkFlow:  
1. Downloading a real-world dataset
2. Preparing a dataset for training
3. Training and interpreting decision trees
4. Training and interpreting random forests
5. Overfitting, hyperparameter tuning & regularization
6. Making predictions on single inputs


## Preparing the Data for Training
We'll perform the following steps to prepare the dataset for training:

- Create a train/test/validation split
- Identify input and target columns
- Identify numeric and categorical columns
- Impute (fill) missing numeric values
- Scale numeric values to the $(0, 1)$ range
- Encode categorical columns to one-hot vectors  

## Training a Random Forest

While tuning the hyperparameters of a single decision tree may lead to some improvements, a much more effective strategy is to combine the results of several decision trees trained with slightly different parameters. This is called a random forest model. 

The key idea here is that each decision tree in the forest will make different kinds of errors, and upon averaging, many of their errors will cancel out. This idea is also commonly known as the "wisdom of the crowd":

<img src="https://i.imgur.com/4Dg0XK4.png" width="480">  
A random forest works by averaging/combining the results of several decision trees:

<img src="https://1.bp.blogspot.com/-Ax59WK4DE8w/YK6o9bt_9jI/AAAAAAAAEQA/9KbBf9cdL6kOFkJnU39aUn4m8ydThPenwCLcBGAsYHQ/s0/Random%2BForest%2B03.gif" width="640">


We'll use the `RandomForestClassifier` class from `sklearn.ensemble`.  
Once again, the training accuracy is almost 100%, but this time the validation accuracy is much better. In fact, it is better than the best single decision tree we had trained so far. Do you see the power of random forests?

This general technique of combining the results of many models is called "ensembling", it works because most errors of individual models cancel out on averaging. Here's what it looks like visually:

<img src="https://i.imgur.com/qJo8D8b.png" width="640">  
## Hyperparameter Tuning with Random Forests

Just like decision trees, random forests also have several hyperparameters. In fact many of these hyperparameters are applied to the underlying decision trees. 

Let's study some the hyperparameters for random forests. You can learn more about them here: https://scikit-learn.org/stable/modules/generated/sklearn.ensemble.RandomForestClassifier.html 
## Machine Learning WorkFlow:  
1. Downloading a real-world dataset
2. Preparing a dataset for training
3. Training and interpreting decision trees
4. Training and interpreting random forests
5. Overfitting, hyperparameter tuning & regularization
6. Making predictions on single inputs
