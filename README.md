# Housing Price Prediction

## Overview
This project involves predicting house prices based on various features using multiple regression models. The analysis is performed in a Python environment, specifically using Google Colab and Kaggle.

## Prerequisites
Before running this project, you need to:
- Have a Python environment with Jupyter Notebook or Google Colab.
- Install required libraries: `numpy`, `pandas`, `scikit-learn`, `matplotlib`, `seaborn`, `xgboost`, `plotly`, and `statsmodels`.

## Installation
1. Clone this repository to your local machine using:
2. Install the required Python libraries


## Data
The data for this project is sourced from the Kaggle Housing Prices Competition. To access the data:
- Log in to your Kaggle account.
- Join the [Housing Prices Competition](https://www.kaggle.com/c/house-prices-advanced-regression-techniques).
- Download the `train.csv` and `test.csv` datasets.

## Configuration for Kaggle API
To download datasets directly from Kaggle:
1. Go to your Kaggle account settings and create a new API token. This will download a `kaggle.json` file.
2. Place the `kaggle.json` file in your `~/.kaggle/` directory and set permissions:
   chmod 600 ~/.kaggle/kaggle.json

3. Use the Kaggle API to download datasets:
kaggle competitions download -c house-prices-advanced-regression-techniques


## Models Used
This project evaluates several regression models:
- Linear Regression
- Ridge Regression
- Lasso Regression
- ElasticNet
- Extra Tree Regressor
- Gradient Boosting Regressor
- XGBoost Regressor
- Decision Tree Regressor
- K-Neighbors Regressor

## Usage
1. Run the Jupyter Notebook or Python script to train the models and predict house prices.
2. Evaluate the performance of each model using metrics such as R2 score, RMSE, and MAE.




## Acknowledgments
- Kaggle for the dataset and competition platform.
- Google Colab for the cloud-based Python environment.

