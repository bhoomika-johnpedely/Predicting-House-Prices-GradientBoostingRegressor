### Project Overview
#### Title: Predicting House Prices

#### Introduction
This project aims to predict house prices on a given data set with 80 predictors. The dataset can be found at: https://www.kaggle.com/competitions/house-prices-advanced-regression-techniques/data. This is a supervised regression problem that may be solved in multiple different ways. I have solved the same problem in R using Multiple Linear Regression when I was first introduced to the dataset. However, in an attempt to apply and demonstrate my newly acquired machine learning knowledge and skills in python, I have revisited the project using a different approach. The performance of my model has improved slightly. Moreover, I have advanced my ML knowledge and skills in the process. 

#### Data Exploration and Preprocessing
- The dataset has 1460 rows and 81 columns, one of which is the target variable, SalePrice.
- The target variable, SalePrice shows a skewed distribution. Hence, I decided to log transform the variable to be included in the model and then inverse the transformation for the predicted variables.
- There were 5 features with too much data missing. I decided to remove them from my training dataset. For other variables that had any null values, I imputed the numerical features with the median and categorical features with the mode.
- I one-hot encoded the categorical variables to make them more suitable for a regression modelling technique.
- I ended up having 73 predictor variables and 1 target variable in my training data. 

#### Modeling
- I did a test-train split with 20% test size.
- To find the right model for my problem, I experimented with 4 modelling techniques that can use both numerical and categorical data to complete a regression task: Random Forest, Gradient Boosting, Elastic Net and SVR.
- After evaluating the MAE and R-squared for each of these models, I selected GradientBoostingRegressor for this task since it had the least MAE (0.0925) and the highest R-squared (90.34%).
- I used the whole training dataset to train the model and predicted on the test set that I submitted to Kaggle.

#### Results
-  After submitting the predictions. Kaggle gave me a public score of 0.13.
-  For this challenge, the scores ranged from 0 to 1 with the median score, around 0.14. Lower values are better as long as it doesn't indicate an overfitted model. 

#### Conclusion
I achieved the goal of predicting house prices using an advanced regression modelling technique. I used log transformation and one-hot encoding in addition to other transformations to make my data more suitable for this modelling task. I selected the model on metrics MAE and R-squared after evaluating it on 4 different models. Then, I predicted the target and received a competitive submission score from Kaggle. Overall, I got the opportunity to use pandas, numpy and scikit-learn libraries to solve an interesting regression problem. 

#### Next Steps
If I wanted to increase the scope of the project or ever revisit it, I would experiment with feature-engineering and hyperparameter tuning to improve model performance. 

