# Table of Contents

1. [Overview](#overview)
2. [Installation](#installation)
3. [Project Motivation](#motivation)
4. [File Descriptions](#files)
5. [Results](#results)
6. [Licensing, Authors, and Acknowledgements](#licensing)

---

# Overview <a name="overview"></a>

In this project we apply advanced regression concepts to build a model which can properly predict the price of houses in Iowa. It is part of a Kaggle competition which can be found [here](https://www.kaggle.com/competitions/house-prices-advanced-regression-techniques/overview/description).

### Problem
 
With 79 explanatory variables describing (almost) every aspect of residential homes in Ames, Iowa; we need to be able to determine its price, minimizing the error of the prediction. 
  
### Metrics

  - RMSE
  - R2
  - MAE
  - MSE
  - MAE log 

For more info about these metrics, check this [post](https://towardsdatascience.com/what-are-the-best-metrics-to-evaluate-your-regression-model-418ca481755b).

# Installation <a name="installation"></a>

This project uses Python 3.9.13. The following libraries are necessary for running the files: 

  - pandas==1.4.4
  - ptitprince==0.2.6
  - matplotlib==3.5.2
  - seaborn==0.11.0
  - numpy==1.21.5
  - scikit-learn==1.0.2
  - shap==0.41.0
  - wordcloud==1.8.2.2
  - pytz==2022.1
  - optuna==3.0.5
  - joblib==1.1.0
  - xgboost==1.7.1
  - lightgbm==3.3.3
  - catboost==1.1.1

### Instructions:

1. Clone this github repository.
`https://github.com/alexrop/house_prices_kaggle.git`

2. Run the notebook *House_Prices_Kaggle.ipynb*

  - You should adapt the notebook to your own environment. For example I import/export files by using my local path (windows and user), so you should change it by your own.
  - All 6 models are in the same notebook, where 3 of them have hyperparameters tuninng with optuna, so if you *run all* it could take a while. I recomend to run it by parts
> I highly recommend working on virtual environments as [conda](https://conda.io/projects/conda/en/latest/user-guide/tasks/manage-environments.html#activating-an-environment) or [venv](https://docs.python.org/3.6/library/venv.html) 



# Project Motivation <a name="motivation"></a>

Basically I was interested in comparing the XGBoost, LightGBM and CatBoost algorithms in a regression problem, looking to know which one obtains better results under similar circumstances. 

# File Descriptions <a name="files"></a>

The following is the distribution of the files inside this repo.

```
house_prices_kaggle
    |-- data
          |-- data_description.txt --> Description of all variables in dataset
          |-- sample_submisssion.csv --> Example of how we should store the final results in order to submit at the Kaggle's competition
          |-- test.csv --> Dataset which we will test our best model
          |-- train.csv --> Dataset which we will train our models
    |-- model_trials
          |-- images --> Folder which contains some images about the develop of the models
          |-- models --> Folder wich contains the back up of all 6 models. They are stored in .joblib format
          |-- notebooks --> Some notebook's older versions
    |-- House_Prices_Kaggle.ipynb  --> Oficial notebook which contains all develop
    |-- submission.csv --> File which was submitted to the Kaggle's competition

```
The structure of the notebook is as follows:

    1. Introduction
    2. Preparation
    3. Data
    4. EDA
    5. Transformation
    6. Modeling
    7. Results

# Results <a name="results"></a>

The best model was a **Catboost - Basic parameters* and below are its metrics.


| RMSE | R2 |	MAE | MSE | MAE log | 
|---|---|---|---|---|
| 25854.924510	| 0.912849	| 15649.355775 | 6.684771e+08 | 0.018547 |


# Licensing, Authors, Acknowledgements <a name="licensing"></a>

All data and guidelines here were provided by [Kaggle](https://www.kaggle.com/competitions/house-prices-advanced-regression-techniques/overview/description)

Author: Alexander R. Ulloa Opazo
