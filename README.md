# crypto_pred_model
Utilising economic data and technical indictors to predict price changes in Ethereum. This project considers daily Ethereum data from:

2016-03-09 - 2022-01-03

The project is organised in the following manner:

Adding column with daily prices changes in percentage format - add_percentage_changes.ipynb  
Adding fundamental and technical indicators - adding_fundaandtech_indicators.ipynb  
Prepping data for model fitting - dataprep_and_modelfit.ipynb  


In this project I utilised Fed Interest rates, S&P 500 values over the past ~6 years as the economic indicators in this project  

In addition, I introduced Bitcoin and Gold prices over the past 6 years - two assets that historically have acted as indicators 
for the crypto markets as a whole.  

With regards to technical indicators I calculated the RSI and the Exponential Moving Average of Ethereum's prices.  

Random Forest and SVM were the initial ML models used in this project but I plan to implement deep learning models in the future
in hopes of getting better results. Furthermore, future interations will consist of more thorough analyses and a greater number of
relevant data points/indicators.  

The goal is to develop a model that considers the overarching state of the market (economic indicators) in addition to more specific 
technical indicators to determine tomorrow's percentage change in price. My hypothesis was that categorising percentage changes would
help make more accurate predictions. So instead of predicting an exact number like -3.45% I made 6 categories - A, B, C, D, E, F - all
representing a percentage change unknown to the model. Below are the categories in which the percentage changes were placed  

A = 2<x<4 ---> 2% - 4% change  
B = 4<x<10 ---> 4% - 10% change  
C = 10<x ---> 10% or greater change  
D = -4<x<-2 ---> -2% to -4% change   
E = -10<x<-4 ---> -4% to -10% change  
F = -10>x --->  

