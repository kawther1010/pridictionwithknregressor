# Bitcoin Price Prediction Using KNeighborsRegressor

## Project Overview

This project aims to predict Bitcoin prices using the KNeighborsRegressor model from scikit-learn. The dataset includes various features such as 'Timestamp', 'Open', 'High', 'Low', 'Close', 'Volume_(BTC)', 'Volume_(Currency)', and 'Weighted_Price'. The model is evaluated using different subsets of columns: 2 columns, 4 columns, and all columns. The performance metrics for each subset are calculated and analyzed.

## Dataset

The dataset contains the following columns:
- Timestamp
- Open
- High
- Low
- Close
- Volume_(BTC)
- Volume_(Currency)
- Weighted_Price

## Results

### Using 2 Columns

**Features**: `Open`, `Close`

- R² Score: 0.9999995089550199
- Mean Absolute Error: 2.288534705293843
- Mean Squared Error: 39.45953122240686

### Using 4 Columns

**Features**: `Open`, `Close`, `Volume_(BTC)`, `Volume_(Currency)`

- R² Score: 0.9997601853520564
- Mean Absolute Error: 14.749925276034881
- Mean Squared Error: 19271.093220545736

### Using All Columns

**Features**: `Open`, `High`, `Low`, `Close`, `Volume_(BTC)`, `Volume_(Currency)`, `Weighted_Price`

- R² Score: 0.9998864379898277
- Mean Absolute Error: 22.866829397141696
- Mean Squared Error: 9125.648091595029
- Root Mean Squared Error: 95.52825807893196

## Interpretation

The KNeighborsRegressor model shows excellent predictive performance across all feature subsets, as indicated by the high R² scores close to 1. Here is a detailed interpretation of the results:

- **Using 2 Columns**: The model achieves an R² score of 0.9999995089550199, indicating an almost perfect fit. The Mean Absolute Error (MAE) and Mean Squared Error (MSE) are also very low, suggesting high accuracy when using only the 'Open' and 'Close' columns.
  
- **Using 4 Columns**: With four features ('Open', 'High', 'Low', 'Close'), the model still performs very well, although the MAE and MSE increase slightly compared to using just 2 columns. This could imply that adding more features doesn't necessarily improve the model's accuracy significantly for this dataset.
  
- **Using All Columns**: Including all features results in a slight decrease in R² score compared to using only 'Open' and 'Close'. The MAE and MSE are higher, which may suggest overfitting or that the additional columns introduce noise rather than useful information for prediction.

In conclusion, the model performs best with the simplest feature set (2 columns), indicating that 'Open' and 'Close' prices alone provide sufficient information for accurate prediction in this context. Adding more features does not necessarily enhance model performance and may even introduce noise.
