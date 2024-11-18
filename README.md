# Sales Forecasting Using Linear Regression

This project demonstrates the use of **Linear Regression** for forecasting sales based on historical data. By utilizing time series analysis, the model predicts future sales, which is crucial for businesses to plan inventory, manage resources, and make data-driven decisions.

## Project Overview

In this project, I worked with a sales dataset and used machine learning techniques to create a model that predicts monthly sales. The project involves the following key steps:

1. **Data Preprocessing**:
   - **Data Cleaning**: The dataset includes sales records with information about store, item, and sales for each day. I cleaned the data by dropping unnecessary columns and handling missing values.
   - **Date Conversion**: The date column was converted into a datetime format to enable easier manipulation of time-related features.
   - **Aggregation**: The sales data was aggregated into monthly totals to provide a better view of the sales trends over time.

2. **Feature Engineering**:
   - **Differencing**: To make the sales data stationary, I calculated the difference between consecutive months (sales_diff).
   - **Lag Features**: I created lag features (up to 12 months) that represent previous month sales, which are essential for forecasting future sales.

3. **Model Building**:
   - I used **Linear Regression**, a simple yet effective model, to predict future sales based on the engineered features.
   - The dataset was split into training and test sets to evaluate the model's performance on unseen data.

4. **Evaluation**:
   - The model's performance was evaluated using several metrics:
     - **Mean Squared Error (MSE)**
     - **Mean Absolute Error (MAE)**
     - **R² (Coefficient of Determination)**

5. **Visualization**:
   - I visualized the actual and predicted sales to visually assess the model's accuracy and performance.

## Technologies Used

- **Python** 3.x
- **pandas** for data manipulation
- **numpy** for numerical computations
- **matplotlib** for data visualization
- **scikit-learn** for machine learning models and metrics

## Requirements

To run this project, make sure you have the following Python libraries installed:

```
pip install pandas numpy matplotlib scikit-learn
```

## How to Run

1. Clone this repository to your local machine:

```
git clone https://github.com/your-username/sales-forecasting.git
```

2. Navigate to the project directory:

```
cd sales-forecasting
```

3. Open the Python script or Jupyter Notebook and execute the code cells.

## Results and Evaluation

The performance of the Linear Regression model was evaluated on the test data using the following metrics:

- **MSE (Root Mean Squared Error)**: 16,308.95
- **MAE (Mean Absolute Error)**: 12,518.32
- **R² (R-squared)**: 0.99, indicating that the model explains 99% of the variance in sales data.

## Visualization

The project includes visualizations that compare the predicted sales with the actual sales. This allows for an intuitive understanding of the model's forecasting accuracy.

## Future Improvements

While the Linear Regression model performs well, there are several ways to improve the forecasting accuracy:

- Experiment with more complex models like **Random Forest**, **XGBoost**, or **LSTM (Long Short-Term Memory)** for better performance.
- Incorporate external factors such as **seasonality**, **holidays**, or **promotions** into the model.
- Deploy the model as a web application for live sales predictions.
