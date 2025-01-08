# Overview
This project explores trends in online recipe popularity by analyzing user reviews and examining their relationship with time and seasonal shifts. 
My goal was to identify patterns in user preferences across different times of the year and build a predictive model to analyze how various factors, 
such as preparation time, age, and seasonal-related themes, affected the popularity of certain recipes.

## Dataset
[Food.com Recipes and Interactions](https://www.kaggle.com/datasets/shuyangli94/food-com-recipes-and-user-interactions)

The dataset I used is too large to upload to my repository, but it can be accessed here. It is composed of 230K+ recipes and 1M+ user reviews
on Food.com over the years 2000-2018.

## Summary
I first conducted an exporatory data analysis on the dataset to look for patterns, trends, and any other interesting data.
Based on the results of my EDA, I chose 7 features from recipes and interactions to turn into feature vectors, in hopes of creating a model
that could accurately predict recipe ratings over time. I used an ARX Time-Series model and incorporated my feature vectors, and used a simple
autoregression model as a baseline. 

Contrary to my expectations, the ARX and autoregression models performed nearly identically on the test dataset. I believe that
since I chose feature vectors based on what I could observe in time trends, they were likely accounted for by the autoregression,
which already predicts based on time trends.

### Tools Used
- Python(Pandas, Matplotlib, Scikit-learn)
- Data Visualization(Seaborn)
- Auto Regression library(statsmodels)
