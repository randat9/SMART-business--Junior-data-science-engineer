# SMART-business--Junior-data-science-engineer

# Sales Forecasting and Product Semantics Analysis

This repository contains solutions to two data science tasks involving sales forecasting and sentiment analysis of product reviews.

## Table of Contents
- [Task 1: Demand Forecasting](#task-1-demand-forecasting)
  - [Goal](#goal)
  - [Implementation](#implementation)
  - [Models Used](#models-used)
  - [Results](#results)
  - [Conclusion](#conclusion)
- [Task 2: Product Semantics Analysis](#task-2-product-semantics-analysis)
  - [Goal](#goal-1)
  - [Implementation](#implementation-1)
  - [Results](#results-1)
  - [Conclusion](#conclusion-1)
- [How to Use](#how-to-use)
- [Dependencies](#dependencies)
- [License](#license)

## Task 1: Demand Forecasting

### Goal
Develop a demand forecasting system for a short-term period (14 days) starting from 7 days after the last date in the data, for all product groups.

### Implementation
1. **Data Preparation**: Loaded and preprocessed the sales data, aggregating by product groups and dates.
2. **Model Development**: Implemented two models:
   - **Random Forest**: Utilized lagged features to capture temporal patterns.
   - **ARIMA**: Used to handle trends and seasonality in the time series data.
3. **Model Evaluation**: Split data into training and testing sets and evaluated models using Mean Squared Error (MSE).
4. **Forecasting**: Forecasted demand for the next 14 days.

### Models Used
- **Random Forest**: Robust against overfitting, capable of capturing complex interactions.
- **ARIMA**: Effective for time series data with trends and seasonality.

### Results
- **Random Forest MSE**: 15.583
- **ARIMA MSE**: Varies across categories, e.g., `ARIMA agro_industria_e_comercio MSE: 1.020`, `ARIMA beleza_saude MSE: 583.642`.

### Conclusion
The models were successfully implemented and evaluated. The forecasting system is capable of predicting future demand for various product categories.

## Task 2: Product Semantics Analysis

### Goal
Develop a system for determining sentiment and identifying prices in text comments.

### Implementation
1. **Sentiment Analysis**: Used TextBlob to classify comments as positive, neutral, or negative.
2. **Price Extraction**: Developed a regex-based approach to find numerical prices in comments.
3. **Visualization**: Displayed sentiment distribution and examples of extracted prices.

### Results
- Sentiment classification was accurately performed.
- Prices were successfully extracted from text comments.

### Conclusion
The system effectively classifies sentiments and extracts prices from product review comments. The implemented methods provide accurate results, meeting the task requirements.

## How to Use
1. Clone this repository:
    ```sh
    git clone https://github.com/your-username/sales-forecasting-and-semantics-analysis.git
    cd sales-forecasting-and-semantics-analysis
    ```
2. Install the required dependencies (see [Dependencies](#dependencies)).
3. Run the Jupyter notebooks provided in the repository:
   - `demand_forecasting.ipynb` for Task 1
   - `product_semantics_analysis.ipynb` for Task 2

## Dependencies
- pandas
- numpy
- sklearn
- statsmodels
- matplotlib
- seaborn
- textblob

Install the dependencies using pip:
```sh
pip install pandas numpy scikit-learn statsmodels matplotlib seaborn textblob
