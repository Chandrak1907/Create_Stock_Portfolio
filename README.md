# Create stock portfolio using machine learning

## Overview:
Notebook in this repo will create various technical analysis indicators using open source "pandas_ta" package and use those features to create a machine learning model to predict rate of return over the next couple of days. This is a regression problem.

Rate of return is defined as $r_{(k,t)} = \frac{C_{(k,t+2)} - C_{(k,t+1)}}{C_{(k,t+1)}} $

Where ${C_{(k,t)}}$ represents closing pricing of stock 'k' at time 't'


## Business use case:
Creating a portfolio of stocks that could give better returns with less volatility is the main requirement of portfolio creation. Some stocks could give high returns with even higher draw downs. Having such high volatile stocks in a portfolio could lead to high risk and higher margin requirements.

Traders use fundamental and technical analysis to identify the stocks that outperform the index using various valuation and quantiative techniques. This ML model attempts to predict rate of return using Open, High, Low and Close (OHLC) data.

# Dataset:

Dataset was sourced from a Kaggle competiton - "JPX Tokyo Stock Exchange Prediction". This [dataset](https://www.kaggle.com/competitions/jpx-tokyo-stock-exchange-prediction/data) consists of 
1. stock_prices.csv -> Historical stock data prices (non-confidential)
2. options.csv -> Options based data
3. secondary_stock_prices.csv -> Historical prices of stocks that are less liquid
4. trades.csv -> Trading volumes from previous business week
5. financials.csv -> Quarterly earnings reports
6. stock_list.csv -> General information about each stock

For this initial version of the notebook, only "stock_prices.csv" is used.
# Product/Services included in the project
1. Data science platform
2. Model catalog

# Pre-requisites to run the notebook
Notebook uses two conda pacakages:
1. "financialservices_p37_gpu_v1"
2. "generalml_p37_cpu_v1"

Install these two packages from environment explorer before running the notebook.

# Repo description

This repo has 3 folders. 
1. build_model - This folder hosts the notebook with code for feature engineering and model building

2. data- Copy the [data](https://www.kaggle.com/competitions/jpx-tokyo-stock-exchange-prediction/data) from Kaggle source to "data/train_files" folder. 

python notebook with create 5 parquet files one for each year of the data from 2017 to 2021.

3. artifacts - All files creating during cataloging the model are saved here

# How to run the notebook?
1. Download the Kaggle competition files from Kaggle and place the files in "data/train_files"
1. Access the notebook from "build_model" folder 
1. For feature engineering steps in the code - use "financialservices_p37_gpu_v1 conda environment 
1. For model building steps in the code use -"generalml_p37_cpu_v1"



