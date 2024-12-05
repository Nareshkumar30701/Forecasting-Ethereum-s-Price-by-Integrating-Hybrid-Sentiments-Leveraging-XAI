# Forecasting-Ethereum-s-Price-by-Integrating-Hybrid-Sentiments-Leveraging-XAI
## Project Overview
This project focuses on predicting Ethereum price changes using a combination of financial data and sentiment analysis derived from news headlines. The analysis integrates traditional machine learning and deep learning models with sentiment analysis techniques and explainable AI (XAI) methods to understand model behavior.

## Dataset Description
Data Sources
Ethereum Data:

Features: Closing price, opening price, volume, low price, high price.
Granularity: Aligned with daily timestamps.
News Headlines:

Aggregated from three different sources.
Preprocessed and concatenated based on corresponding Ethereum trading dates.

## Methodology
Data Preprocessing
Ethereum data and news headlines were aligned based on timestamps.
Sentiment analysis was performed on the news headlines using three methods:
VADER
BERT
TextBlob
Averaged the sentiment scores from the three methods.
Combined the averaged sentiments with the Ethereum volume feature to create a new feature, Average Sentiments and Volume.
Feature Engineering
Used the following features for training:
Average Sentiments and Volume
Open price
Close price
Low price
High price
TF-IDF vectorizations of the concatenated news headlines
Correlation Analysis
The feature Average Sentiments and Volume was correlated with Ethereum price changes to validate its significance.
## Model Training
Machine Learning Models
XGBoost Regressor: Achieved the best performance.
Random Forest Regressor
LSTM (Long Short-Term Memory): Explored deep learning for temporal sequence prediction.
## Evaluation Metrics
Standard regression metrics like MAE, RMSE, and R².
## Explainable AI (XAI)
A series of XAI techniques were implemented to understand the decision-making process of the XGBoost Regressor:
SHAP (SHapley Additive exPlanations): Feature importance and contribution analysis.
Feature Permutation Importance: Evaluated the impact of individual features on model performance.
Results
Best Performing Model: XGBoost Regressor.
Significant Features: The Average Sentiments and Volume feature, along with price-related data, had a strong correlation with price changes.
