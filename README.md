# Predicting Housing Prices using Cross Validation and Grid Search in Regression Models
Analysis and prediction for the housing market prices using Cross Validation and Grid Search in several regression models

## Goal of this Project
In this article, I analyze the factors related to housing prices in Melbourne and perform the predictions for the housing prices using several machine learning techniques. The models used in this analysis are Linear Regression, Ridge Regression, K-Nearest Neighbors (hereafter, KNN), and Decision Tree. Using the methods of the Cross Validation and Grid Search techniques, I find the optimal values for hyper parameters in each model, and compare the results to find the best machine learning model to predict the housing prices in Melbourne.

## How to Run this Project
- Install Python 3.
- Install Jupyter Notebook.
- Install the Python requirements with ```pip install -r requirements.txt```.
- Save ```settings.py``` in your computer and create a new PATH system variable to locate the folder where the ```settings.py``` is saved.
   - In order to draw the melbourne housing map using gmplot, you have to create ```private.py``` file containing a line ```API_KEY = "your own api_key"```. Then, save this file in the same folder as where ```settings.py``` is.
- Open ```melbourne_housing.ipynb``` in the Jupyter Notebook and run the cells.

(Link to the notebook: https://github.com/yjeong5126/housing_prices/blob/master/melbourne_housing.ipynb)
