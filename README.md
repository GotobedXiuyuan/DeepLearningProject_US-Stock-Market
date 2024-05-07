# Economic Indicators as Predictors of US Stock Market Trends: An Analysis from 1979 to 2019

## Team Members
- Cordilia Zhao zz2418@nyu.edu
- Wenqing Zhu wz1575@nyu.edu
- Chris Wu xw2147@nyu.edu

## Github repo:
1. Use datasets and the final_combined_sp500.ipynb to join the datasets
2. Use process_data.ipynb to introduce variation for the dataset
3. Use DS301_projectoutput_graph.ipynb to run the models and analysis


## Introduction
This project explores the relationship between various economic indicators and US stock market trends over four decades, using a blend of machine learning models to predict stock market movements based on historical data.


## Methodology

### Data Variation Introduction
To enhance our model's accuracy, we introduced random variations to datasets with sparse frequency (monthly or quarterly):
- Monthly data like 'FederalFundsRate' and 'InflationRate' received random noise based on a 0.5% standard deviation of the mean monthly values.
- Quarterly data for 'GDP' and 'Debt' had a 1% standard deviation applied, while 'UnemploymentRate' used a smaller 0.5% deviation.

### Model Development
We developed a hybrid model combining LSTM and Transformer architectures to leverage both long-term dependencies and the ability to focus on different sequence parts:
- **LSTM Layer**: Captures temporal dependencies.
- **Transformer Layer**: Includes multi-head attention for complex dependency understanding and layer normalization for stability.
- **Output Layer**: Uses global average pooling to simplify output while retaining essential information.

### Cross-validation
Implemented three methods to validate our model:
- **Time-series cross-validation**
- **Walkthrough validation**
- **Bootstrapping**
Each method helped ensure the model’s robustness and reliability by simulating various real-world scenarios.

## Results
Our hybrid model outperformed individual LSTM and Transformer models with a significantly lower RMSE score, indicating high predictive accuracy and efficiency.

## Hyperparameter Tuning
We fine-tuned several parameters such as LSTM units, learning rates, and dropout rates to find the optimal settings, which significantly contributed to the model's performance.

## Cross-Validation and Hyperparameter Optimization
Further tests with cross-validation combined with systematic hyperparameter adjustments confirmed the model's effectiveness across different data subsets.


