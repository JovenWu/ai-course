# Week 3 — Linear Regression

## Overview

This assignment implements linear regression for smartphone price prediction. The project demonstrates machine learning fundamentals using a dataset of smartphone specifications to predict their market prices.

## Problem Statement

Goal: Build a linear regression model that predicts smartphone prices based on various technical specifications and features.

Input features may include:
- RAM, Storage, Camera specifications
- Screen size, Battery capacity
- Brand, Operating system
- Other technical specifications

Output: Predicted smartphone price

## Key Components

The implementation is contained in [Phone_Price_Prediction.ipynb](Phone_Price_Prediction.ipynb) which includes:

- Data preprocessing and exploration
- Feature engineering and selection
- Linear regression model training
- Model evaluation and performance metrics
- Price prediction on test data

## Files in this folder

- [Phone_Price_Prediction.ipynb](Phone_Price_Prediction.ipynb) — main notebook containing the linear regression implementation
- [data-smartphone.csv](data-smartphone.csv) — dataset with smartphone specifications and prices
- [readme.md](readme.md) — this file

## How to run the smartphone price prediction

1. Open [Phone_Price_Prediction.ipynb](Phone_Price_Prediction.ipynb) in Jupyter or VS Code
2. Ensure your Python environment has the required packages (typically: pandas, numpy, matplotlib, seaborn, scikit-learn)
3. Run all notebook cells sequentially
4. The notebook will:
   - Load and explore the smartphone dataset
   - Preprocess the data (handle missing values, encode categorical variables)
   - Train a linear regression model
   - Evaluate model performance
   - Make price predictions

## Dataset

The [data-smartphone.csv](data-smartphone.csv) contains smartphone specifications and their corresponding market prices. The dataset is used to train and test the linear regression model.

## Model Approach

- **Algorithm**: Linear Regression
- **Preprocessing**: Data cleaning, feature encoding, normalization
- **Evaluation**: Performance metrics such as MSE, RMSE, R²
- **Visualization**: Plots showing model performance and feature relationships

## Expected Outputs

- Model performance metrics
- Visualizations of actual vs predicted prices
- Feature importance analysis
- Trained model ready for price predictions

## Notes

- This is a supervised learning regression problem
- The model learns relationships between smartphone features and prices
- Results can be used for market analysis and pricing strategies