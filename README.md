# Sales Forecasting Capstone Project

### 1. Project Overview

This project focuses on predicting future sales for various restaurants using historical sales data. The goal is to generate accurate forecasts to assist in decision-making, such as inventory management, staff planning, and budgeting. The project utilizes machine learning algorithms like Random Forest and deep learning techniques like Long Short-Term Memory (LSTM) to generate sales forecasts for the upcoming year. 

### 2. Problem Statement

In a competitive market, forecasting sales plays a crucial role in optimizing business strategies. Fresh Analytics, a data analytics company, aims to predict the sales of items across different restaurants over several years to assist with decision-making. 
The objective of this project is to develop models capable of forecasting future sales based on historical sales patterns and trends. 

### 3. Dataset Description

**The dataset comprises three CSV files:** 

  Restaurants.csv: Contains information about restaurants, including their IDs and names. 

  Items.csv: Describes items sold by the restaurants, including item IDs, store IDs, and calories. 

  Sales.csv: Contains the daily sales data of items, including the date, item, price, and item count. 

**Key features:** 

  Date: The day on which the sales were recorded. 

  Item: The name of the item sold. 

  Price: The price per unit of the item. 

  Item count: The total number of items sold on that day. 

### 4. Project Approach

**4.1. Preliminary Data Processing**

  Data Cleaning: The data was cleaned to handle missing values and outliers. 

  Merging Data: The three datasets were merged to create a unified dataset containing all relevant information: date, restaurant ID, item ID, sales count, and other static features. 

  Feature Engineering: Additional features were derived from the date column, including day of the week, month, and quarter, to capture seasonal patterns and trends. 

**4.2. Machine Learning Modeling**

  Random Forest Regressor: A popular ensemble learning method that works by creating multiple decision trees and averaging their predictions. 

**4.3. Deep Learning Modeling** 

An LSTM model was employed to handle the time series nature of the sales data, as it is capable of capturing long-term dependencies in sequential data. The LSTM model was trained on the historical sales data to predict future sales trends. 

### 5. Model Evaluation 

To evaluate the performance of the models, we used common metrics: 

  Root Mean Square Error (RMSE): A standard measure to assess the differences between predicted and actual sales values. 

  Mean Absolute Percentage Error (MAPE): A percentage-based metric to understand how far off the predictions were from the true values. 

### 6. Forecast Visualization 

Once the best-performing model was selected, sales forecasts for the next year were generated. To present the results clearly: 

  Visualization: Individual sales forecasts for each restaurant were plotted. The y-axis of the sales plots was formatted as currency, and scaling was applied to sales values that were too small to be meaningful. 

  Currency Formatting: The y-axis was adjusted to display sales in thousands (K) or millions (M) based on the range of values. 

### 7. Challenges Encountered 

  Scaling Sales Values: Many of the predicted sales values were below 1, which made visualization difficult. We applied scaling factors to bring the values into a more visually meaningful range and formatted the axes accordingly. 

  Handling Time-Series Data: Capturing long-term trends and seasonality was challenging.

  Creating Test Data: Creating data to test the model was difficult, after a lengthy process involving the correct use of dataframes it was modertely resolved. Still an active part of the project that needs work. 

### 8. Conclusion 

The project successfully generated sales forecasts using a ML RandomForest model. The visualizations of the results provide a clear view of expected future sales, which can guide business decisions. 
Future work could explore additional time-series models, further tuning of the LSTM network, and adding external data (e.g., weather or holidays) to enhance forecast accuracy. 
