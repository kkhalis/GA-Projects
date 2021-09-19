# Project 2 - Ames Housing Data and Kaggle Challenge

## Problem Statement
The Ames Housing board is looking to see how we can predict the prices of future houses, based on a list of features. These features are a combination of nominal, ordinal, continuous and discrete values.

To do that, the board has tasked you and the team to create a prediction model that can predict the prices of houses within Ames, given a list of features that may or may not contribute to the sale price of a house.
Welcome to Project 2! It's time to start modeling.

### Contents
* Data import, helper functions, cleaning and mapping of ordinal values
* EDA: Previewing Data and Highlighting Outliers
* Testing on Various Regression Models
* Applying our selected model on the Kaggle test set
* Conclusion

### Datasets
2 datasets have been used for this project as shown below:

* [`test.csv`](./datasets/train.csv): 2006 to 2010 housing information of Ames, Iowa. Inclusive of SalePrice
* [`new_test.csv`](./datasets/new_test.csv): Kaggle test set to use to predict house prices.

### Data Dictionary
You can access the data dictionary, split into markdown format [*here*](https://github.com/kkhalis/GA-Projects/blob/master/project_2/DataDictionary.md).

### Conclusion
On submission to Kaggle, the best performing score for prediction was 24338.24.

ElasticNet may have performed better, we should take into consideration on computational speed of our models as a larger dataset for training and prediction might incur exponential time for computation.

While doing multiple runs over various subsets of data (e.g, correlation coefficients above a certain threshold), we notice that numeric features usually contribute to having better predictions. However, we can also see the minimal reduction of the RMSE scores in the predictions over time, giving only small returns when providing more features.

|Correlation % to <br> SalePrice | No. of Numeric<br> Features | LR (RMSE) | Ridge (RMSE) | Lasso (RMSE) | ElasticNet (RMSE) |
|:-:|:-:|:-:|:-:|:-:|:-:|
| > 40%|22|26366|26260|26362|26308|
| > 30%|26|25471|25292|25468|25336|
| > 20%|30|25428|25159|25423|25172|
| > 10%|32|25343|25085|25339|25086|

Although interaction terms did help to improve the score, applying Polynomial features across the set may help to improve the accuracy of the model.

Presentation slides can be found [*here*](https://docs.google.com/presentation/d/1W-U_6W32IP5Oh4XHre0GjcRVlr4jo0FOwydsHqSQ7rc/edit?usp=sharing).