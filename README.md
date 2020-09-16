# Predicting Housing Prices using Cross Validation and Grid Search in Regression Models
> Analysis and prediction for the housing market prices using Cross Validation and Grid Search in several regression models

## Goals of this Project
In this article, I analyze the factors related to housing prices in Melbourne and perform the predictions for the housing prices using several machine learning techniques. The models used in this analysis are Linear Regression, Ridge Regression, K-Nearest Neighbors (hereafter, KNN), and Decision Tree. Using the methods of the Cross Validation and Grid Search techniques, I find the optimal values for hyper parameters in each model, and compare the results to find the best machine learning model to predict the housing prices in Melbourne.

## How to Run this Project
- Install Python 3.
- Install Jupyter Notebook.
- Install the Python requirements with ```pip install -r requirements.txt```.
- Save ```settings.py``` in your computer and create a new PATH system variable to locate the folder where the ```settings.py``` is saved.
   - In order to draw the melbourne housing map using gmplot, you have to create ```private.py``` file containing a line ```API_KEY = "your own api_key"```. Then, save this file in the same folder as where ```settings.py``` is.
- Open ```melbourne_housing.ipynb``` in the Jupyter Notebook and run the cells.

(Link to the notebook: https://github.com/yjeong5126/housing_prices/blob/master/melbourne_housing.ipynb)

## Data
The data for this project is the Melbourne Housing Market from the Kaggle dataset. The geographical distribution of the houses in Melbouren is as follows:

![](https://github.com/yjeong5126/housing_prices/blob/master/images/melbourne_housing.png)

## Results
### Basic Predictions
The results of the basic predictions for each model are as follows:

- Linear Regression

![](https://github.com/yjeong5126/housing_prices/blob/master/images/linear_regression_1.PNG)

The R² of the linear regression is 0.6146, which means that about 60% of the variance of the housing prices in the data can be predicted by the model. The RMSE is 264,465. This means that for all the predictions for the testing set, the average difference for each prediction is \\$264,465.

- Ridge Regression

![](https://github.com/yjeong5126/housing_prices/blob/master/images/ridge_regression_1.PNG)

The result above is obtained with the regularization parameter(alpha) equal to 100. The R² of this model is 0.6133, and the RMSE is 264,920.

- KNN Regression

![](https://github.com/yjeong5126/housing_prices/blob/master/images/knn_regression_1.PNG)

The result above is obtained with the number of the neighbors equal to 5. The R² of this model is 0.7053, and the RMSE is 231,250.

- Decision Tree Regression

![](https://github.com/yjeong5126/housing_prices/blob/master/images/dt_regression_1.PNG)

Max depth is set to 15. The R² of this model is 0.6920, and the RMSE is 236,424.

### Cross Validation Summary

The optimal values of the hyper-parameters for each model are as follows:
- Ridge: alpha = 10
- KNN: the number of neighbors = 16
- Decision Tree: max depth = 9

The following graphs show the distributions and the changes of the metric scores in the cross validation at the optimal values of the hyper-parameters.

![](https://github.com/yjeong5126/housing_prices/blob/master/images/cross_val_summary_graph.PNG)

The model showing the best performance for the prediction is K-Nearest Neighbors, and the optimal value for the number of neighbors is 16.
