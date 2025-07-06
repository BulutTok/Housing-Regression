# Benchmarking Regression Algorithms for House Price Prediction

This repository contains a Jupyter Notebook (`housing_price_model.ipynb`) that implements an end-to-end pipeline for predicting house prices using the **Kaggle House Prices: Advanced Regression Techniques** dataset.

## Table of Contents

* [Project Overview](#project-overview)
* [Dataset](#dataset)
* [Environment Setup](#environment-setup)
* [Usage](#usage)
* [Project Structure](#project-structure)
* [Methodology](#methodology)

  * [1. Data Exploration](#1-data-exploration)
  * [2. Data Preprocessing & Feature Engineering](#2-data-preprocessing--feature-engineering)
  * [3. Modeling](#3-modeling)
  * [4. Evaluation](#4-evaluation)
* [Results](#results)
* [Contributing](#contributing)
* [License](#license)
* [Contact](#contact)

## Project Overview

The goal of this project is to build and compare several regression models to predict sale prices of houses based on their attributes. We implement preprocessing, feature engineering, model training, and evaluation all within a single notebook.

## Dataset

I use the **House Prices: Advanced Regression Techniques** dataset from Kaggle. It includes 79 explanatory variables describing (almost) every aspect of residential homes in Ames, Iowa.

* Competition link: [https://www.kaggle.com/c/house-prices-advanced-regression-techniques](https://www.kaggle.com/c/house-prices-advanced-regression-techniques)

## Environment Setup

1. **Clone the repository**

   ```bash
   git clone <repo-url>
   cd <repo-folder>
   ```

2. **Create a virtual environment** (recommended)

   ```bash
   python3 -m venv venv
   source venv/bin/activate  # on Windows: venv\Scripts\activate
   ```

3. **Install dependencies**

   ```bash
   pip install -r requirements.txt
   ```

> **requirements.txt** should include:
>
> ```text
> numpy
> pandas
> scikit-learn
> xgboost
> matplotlib
> seaborn
> ```

## Usage

1. Download the Kaggle dataset and place `train.csv` and `test.csv` in a `data/` folder at the project root.
2. Launch Jupyter Notebook:

   ```bash
   jupyter notebook housing_price_model.ipynb
   ```
3. Run each cell sequentially. Adjust parameters or models as desired.

## Project Structure

```text

│── train.csv
│── test.csv
├── housing_price_model.ipynb
├── README.md
└── requirements.txt
```

## Methodology

### 1. Data Exploration

* Load data with `pandas`.
* Analyze distributions, check missing values, and visualize key relationships.

### 2. Data Preprocessing & Feature Engineering

* Impute missing values (median for numerical, mode for categorical).
* Encode categorical features using one-hot encoding.
* Scale numerical features if required.
* Create new features (e.g., total square footage).

### 3. Modeling

I train and compare the following regressors:

* **Linear Regression**
* **Ridge Regression**
* **Lasso Regression**
* **ElasticNet**
* **Decision Tree Regressor**
* **Extra Trees Regressor**
* **K-Nearest Neighbors Regressor**
* **Gradient Boosting Regressor**
* **XGBoost Regressor**

### 4. Evaluation

Models are evaluated using:

* **R² Score**
* **Root Mean Squared Error (RMSE)**
* **Mean Absolute Error (MAE)**

## Results

The performance of each model on the test set:

| Model                       | R² Score | RMSE   | MAE    |
| --------------------------- | -------- | ------ | ------ |
| Ridge                       | 0.8891   | 0.1304 | 0.0910 |
| Linear Regression           | 0.8888   | 0.1306 | 0.0911 |
| XGradientBoosting Regressor | 0.8483   | 0.1525 | 0.1152 |
| Gradient Boosting Regressor | 0.8440   | 0.1547 | 0.1032 |
| KNeighbors Regressor        | 0.7735   | 0.1863 | 0.1376 |
| Extra Trees Regressor       | 0.6975   | 0.2154 | 0.1571 |
| Decision Tree Regressor     | 0.6464   | 0.2329 | 0.1739 |
| Lasso Regression            | -0.0015  | 0.3919 | 0.3139 |
| ElasticNet Regression       | -0.0021  | 0.3920 | 0.3139 |

> **Best performance** was achieved by **Ridge Regression** with an R² of 0.8891.


## Contributing

1. Fork the repository.
2. Create a new branch: `git checkout -b feature/your-feature`.
3. Commit your changes: `git commit -m 'Add some feature'`.
4. Push to the branch: `git push origin feature/your-feature`.
5. Open a Pull Request.

## License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.

## Contact

Created by Bulut Tok. Feel free to reach out with questions or suggestions!")}

