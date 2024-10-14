# Capstone Project: Sales Forecasting

#### By Tara Danneman

## Project Overview

Fresh Analytics, a data analytics company, aims to understand and predict the demand for various items across restaurants. The primary objective of this project is to forecast the sales of items at different restaurants over several years. Accurate demand forecasting is crucial for making informed business decisions related to production, sales, and staffing. This project involves using historical sales data to develop predictive models that can provide reliable sales forecasts, ultimately aiding in better business planning and decision-making.

## Table of Contents

- [Project Overview](#project-overview)
- [Problem Statement](#problem-statement)
- Datasets
- [Project Tasks](#project-tasks)
- Dependencies
- [How to Run](#how-to-run)

## Problem Statement

Fresh Analytics seeks to improve its demand forecasting capabilities to support business decisions at both international and domestic levels. The project involves using historical sales data to develop predictive models that can provide reliable sales forecasts, ultimately aiding in better business planning and decision-making.

## Datasets

The project uses three datasets:
- `restaurants.csv`: Information about restaurants.
- `sales.csv`: Sales transactions data.
- `items.csv`: Information about items.

## Project Tasks

### Step 1: Preliminary Analysis

1. **Import the datasets**:
    - Import `restaurants.csv`, `sales.csv`, and `items.csv` into the Python environment using pandas.
2. **Examine the datasets**:
    - Check the shape, structure, and summary statistics of each dataset.
    - Identify and handle any outliers or missing values.
3. **Merge the datasets**:
    - Merge the datasets into a single DataFrame that includes [`date`](command:_github.copilot.openSymbolFromReferences?%5B%22%22%2C%5B%7B%22uri%22%3A%7B%22scheme%22%3A%22file%22%2C%22authority%22%3A%22%22%2C%22path%22%3A%22%2Fc%3A%2FUsers%2Ftarad%2FOneDrive%2FDocuments%2FAI%20ML%20Class%2FIncremental_Capstone%2FCapstone%20Project%2FCapstone_project_beta.ipynb%22%2C%22query%22%3A%22%22%2C%22fragment%22%3A%22%22%7D%2C%22pos%22%3A%7B%22line%22%3A50%2C%22character%22%3A69%7D%7D%5D%2C%22c04b2de4-cd79-4965-9156-a617de4bb904%22%5D "Go to definition"), `item id`, [`price`](command:_github.copilot.openSymbolFromReferences?%5B%22%22%2C%5B%7B%22uri%22%3A%7B%22scheme%22%3A%22file%22%2C%22authority%22%3A%22%22%2C%22path%22%3A%22%2Fc%3A%2FUsers%2Ftarad%2FOneDrive%2FDocuments%2FAI%20ML%20Class%2FIncremental_Capstone%2FCapstone%20Project%2FCapstone_project_beta.ipynb%22%2C%22query%22%3A%22%22%2C%22fragment%22%3A%22%22%7D%2C%22pos%22%3A%7B%22line%22%3A50%2C%22character%22%3A88%7D%7D%5D%2C%22c04b2de4-cd79-4965-9156-a617de4bb904%22%5D "Go to definition"), `item count`, `item name`, [`kcal`](command:_github.copilot.openSymbolFromReferences?%5B%22%22%2C%5B%7B%22uri%22%3A%7B%22scheme%22%3A%22file%22%2C%22authority%22%3A%22%22%2C%22path%22%3A%22%2Fc%3A%2FUsers%2Ftarad%2FOneDrive%2FDocuments%2FAI%20ML%20Class%2FIncremental_Capstone%2FCapstone%20Project%2FCapstone_project_beta.ipynb%22%2C%22query%22%3A%22%22%2C%22fragment%22%3A%22%22%7D%2C%22pos%22%3A%7B%22line%22%3A50%2C%22character%22%3A124%7D%7D%5D%2C%22c04b2de4-cd79-4965-9156-a617de4bb904%22%5D "Go to definition"), `store id`, and `store name`.

### Step 2: Exploratory Data Analysis (EDA)

1. **Date-wise sales analysis**:
    - Plot the overall date-wise sales to understand the sales pattern over time.
2. **Sales fluctuation analysis**:
    - Analyze and visualize how sales fluctuate across different days of the week.
3. **Monthly sales trends**:
    - Examine and visualize the sales trends for different months of the year.
    - Compare the performances of different restaurants and items in terms of total sales per month.
4. **Quarterly sales distribution**:
    - Analyze the sales distribution across different quarters averaged over the years to identify patterns.
    - Compare the performances of different restaurants in terms of total sales per quarter.
5. **Popular items identification**:
    - Identify the most popular items overall and the stores where they are sold.
    - Find out the most popular item at each store.
6. **Revenue vs. sales volume analysis**:
    - Determine if the store with the highest sales volume also makes the most money per day.
7. **Expensive item analysis**:
    - Identify the most expensive item at each restaurant and find out its calorie count.

### Step 3: Machine Learning Model Development

1. **Prepare and normalize/standardize the data**:
    - Perform feature engineering to standardize features.
    - Remove irrelevant features.
    - Split the data into training and testing sets, using the last six months as testing data.
2. **Model building and comparison**:
    - Build and train Linear Regression, Decision Tree, Random Forest, and XGBoost models.
    - Compute the Root Mean Square Error (RMSE) for each model to compare their performance.
3. **Forecasting**:
    - Use the best-performing model to make sales forecasts for the next year.

### Step 4: Deep Learning Model Development

1. **Data preparation**:
    - Use sales amount for predictions instead of item count.
    - Define the train and test series for the LSTM model.
    - Generate synthetic data for the last 12 months if necessary.
2. **Build and train the LSTM model**:
    - Design and build the LSTM network.
    - Train the LSTM model on the training data.
3. **Model evaluation**:
    - Use the LSTM model to make predictions for the test data.
    - Calculate the Mean Absolute Percentage Error (MAPE) to evaluate the model's performance.
4. **Forecasting**:
    - Develop another LSTM model using the entire series for training.
    - Use this model to forecast sales for the next three months.

### Step 5: Model Deployment and Reporting

1. **Deploy the model**:
    - Deploy the best-performing model (machine learning or deep learning) to a production environment for real-time predictions.
2. **Reporting**:
    - Create a detailed report summarizing the findings, model performance, and forecasts.
    - Include visualizations and key insights derived from the EDA and model results.
3. **Maintenance**:
    - Set up a process for regularly updating the model with new data to maintain its accuracy and relevance.

## Dependencies

- pandas
- numpy
- matplotlib
- seaborn
- scikit-learn
- xgboost
- tensorflow

## How to Run

1. **Clone the repository:**
   ```sh
   git clone <repository-url>
   ```
2. **Navigate to the project directory:**
   ```sh
   cd <project-directory>
   ```
3. **Install the required dependencies:**
   ```sh
   pip install -r requirements.txt
   ```
4. **Run the Jupyter Notebook:**
   ```sh
   jupyter notebook CAPSTONE_PROJECT_BETA.ipynb
   ```

Feel free to explore the notebook and modify the code as needed to further analyze and visualize the data.

