# Task 2: Short-Term Stock Price Prediction

##  Objective
This project focused on forecasting the closing stock price of Tesla Inc. (**TSLA**) for the following trading day, leveraging past market performance data.

##  Dataset Overview
- **Data Source:** Acquired using the `yfinance` Python package from Yahoo Finance  
- **Period Covered:** [Insert specific timeframe used, e.g., "From August 2023 to August 2025"]
- **Input Variables:**
  - Opening Price  
  - Daily High  
  - Daily Low  
  - Trading Volume  
- **Target Output:** Next day's Closing Price

##  Process Breakdown

### Data Collection
- Collected TSLA’s historical trading data programmatically using the `yfinance` API.

### Preprocessing Steps
- Shifted the `"Close"` column forward by one day to form the prediction target (`Next_Close`).  
- Addressed missing entries that resulted from the shifting operation.

### Feature Engineering
- Selected `['Open', 'High', 'Low', 'Volume']` as the predictor variables for the model.

### Model Development
- Split the dataset into training (80%) and testing (20%) subsets.  
- Utilized a **Random Forest Regressor** to model the relationship between selected features and the next day’s close.

### Performance Evaluation
- Assessed the model using **Root Mean Squared Error (RMSE)** to measure prediction accuracy.  
- Created comparison plots of actual vs predicted closing prices.

### Visualization
- Displayed time series plots to visually interpret how well the model captures price trends over time.

##  Findings
- **RMSE Score:** [Insert the calculated RMSE from your results]  
- While the model performs reasonably well in capturing general trends, its predictions may not fully reflect rapid market shifts or sharp volatility.
