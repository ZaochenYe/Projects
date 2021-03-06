# =============================================

# [Competition of "favorita grocery sales forecast"](https://www.kaggle.com/c/favorita-grocery-sales-forecasting)

In this competition, you will be predicting the unit sales for thousands of items sold at different Favorita stores located in Ecuador. The training data includes dates, store and item information, whether that item was being promoted, as well as the unit sales. Additional files include supplementary information that may be useful in building your models.

# -------------------------------------------------------------------
## File Descriptions and Data Field Information

### train.csv

Training data, which includes the target unit_sales by date, store_nbr, and item_nbr and a unique id to label rows.
The target unit_sales can be integer (e.g., a bag of chips) or float (e.g., 1.5 kg of cheese).
Negative values of unit_sales represent returns of that particular item.
The onpromotion column tells whether that item_nbr was on promotion for a specified date and store_nbr.
Approximately 16% of the onpromotion values in this file are NaN.
NOTE: The training data does not include rows for items that had zero unit_sales for a store/date combination. There is no information as to whether or not the item was in stock for the store on the date, and teams will need to decide the best way to handle that situation. Also, there are a small number of items seen in the training data that aren't seen in the test data.

### test.csv

Test data, with the date, store_nbr, item_nbr combinations that are to be predicted, along with the onpromotion information.
NOTE: The test data has a small number of items that are not contained in the training data. Part of the exercise will be to predict a new item sales based on similar products..
The public / private leaderboard split is based on time. All items in the public split are also included in the private split.


### sample_submission.csv

A sample submission file in the correct format.
It is highly recommend you zip your submission file before uploading!

### stores.csv

Store metadata, including city, state, type, and cluster.
cluster is a grouping of similar stores.

### items.csv

Item metadata, including family, class, and perishable.
NOTE: Items marked as perishable have a score weight of 1.25; otherwise, the weight is 1.0.

### transactions.csv

The count of sales transactions for each date, store_nbr combination. Only included for the training data timeframe.

### oil.csv

Daily oil price. Includes values during both the train and test data timeframe. (Ecuador is an oil-dependent country and it's economical health is highly vulnerable to shocks in oil prices.)

### holidays_events.csv

Holidays and Events, with metadata
NOTE: Pay special attention to the transferred column. A holiday that is transferred officially falls on that calendar day, but was moved to another date by the government. A transferred day is more like a normal day than a holiday. To find the day that it was actually celebrated, look for the corresponding row where type is Transfer. For example, the holiday Independencia de Guayaquil was transferred from 2012-10-09 to 2012-10-12, which means it was celebrated on 2012-10-12. Days that are type Bridge are extra days that are added to a holiday (e.g., to extend the break across a long weekend). These are frequently made up by the type Work Day which is a day not normally scheduled for work (e.g., Saturday) that is meant to payback the Bridge.
Additional Notes

Wages in the public sector are paid every two weeks on the 15 th and on the last day of the month. Supermarket sales could be affected by this.
A magnitude 7.8 earthquake struck Ecuador on April 16, 2016. People rallied in relief efforts donating water and other first need products which greatly affected supermarket sales for several weeks after the earthquake.

# -------------------------------------------------------------------
## [Time Series Forecast Study with Python: Monthly Sales of French Champagne](https://machinelearningmastery.com/time-series-forecast-study-python-monthly-sales-french-champagne/)
In this tutorial, we will work through a time series forecasting project from end-to-end, from downloading the dataset and defining the problem to training a final model and making predictions.

This project is not exhaustive, but shows how you can get good results quickly by working through a time series forecasting problem systematically.

The steps of this project that we will through are as follows.

* Environment.
* Problem Description.
* Test Harness.
* Persistence.
* Data Analysis.
* ARIMA Models.
* Model Validation.



This will provide a template for working through a time series prediction problem that you can use on your own dataset.
# -------------------------------------------------------------------
## Important literatures and examples:
### 1. Drugs store sales forecast using Machine Learning [paper](http://cs229.stanford.edu/proj2015/191_report.pdf) and [poster](http://cs229.stanford.edu/proj2015/191_poster.pdf)
* We use AR model to predict the sales with small discrepancy to the test data, and we use RF and SVR to find relations between store mean sales and other features. There are certainly rooms for improvements. We can make further predictions on daily sales using SVR. Even though we found the relations between the features, and make fairly good predictions on average sales for each store. We think next we could try to use SVR see how the parameters set in AR change according to features. By doing so, we could automate the process of making predictions on daily sales for all the stores in the time series model.
### 2. [Winner example codes of Rossman store sales](https://github.com/ageek/kaggle/tree/master/2015-Kaggle/rossman-store-sales) 
* Rossmann operates over 3,000 drug stores in 7 European countries. Currently, Rossmann store managers are tasked with predicting their daily sales for up to six weeks in advance. Store sales are influenced by many factors, including promotions, competition, school and state holidays, seasonality, and locality. With thousands of individual managers predicting sales based on their unique circumstances, the accuracy of results can be quite varied.
### both 1 and 2 are from the same kaggle competition of "Rossman store sales"
### 3. [Revenue Forecasting for Enterprise Products](https://arxiv.org/pdf/1701.06624.pdf)
* In this paper, we provide insights into the three different machine learning models that we developed using standard time series and       regression algorithms. In particular, we use ARIMA (Autoregressive integrated moving average), ETS (Exponential smoothing) , STL        (Seasonal and trend decomposition using Loess) , and Random forest machine learning algorithms to provide the revenue forecast as a
guideline to be used by Microsoft Finance in their process of quarterly revenue forecast. 

## 4. [Time Series Forecasting with the Long Short-Term Memory Network in Python](https://machinelearningmastery.com/time-series-forecasting-long-short-term-memory-network-python/)
* Time Series Forecasting with the Long Short-Term Memory Network in Python
by Jason Brownlee on April 7, 2017 in Long Short-Term Memory Networks
The Long Short-Term Memory recurrent neural network has the promise of learning long sequences of observations.

* In this tutorial, you will discover how to develop an LSTM forecast model for a one-step univariate time series forecasting problem.

* After completing this tutorial, you will know:

* How to develop a baseline of performance for a forecast problem.
* How to design a robust test harness for one-step time series forecasting.
* How to prepare data, develop, and evaluate an LSTM recurrent neural network for time series forecasting.
# =============================================

## others: [https://machinelearningmastery.com/time-series-prediction-lstm-recurrent-neural-networks-python-keras/](https://machinelearningmastery.com/time-series-prediction-lstm-recurrent-neural-networks-python-keras/)
[http://www.jakob-aungiers.com/articles/a/LSTM-Neural-Network-for-Time-Series-Prediction](http://www.jakob-aungiers.com/articles/a/LSTM-Neural-Network-for-Time-Series-Prediction)
[https://github.com/lilianweng/stock-rnn](https://github.com/lilianweng/stock-rnn)

