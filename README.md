## Code Readme
This README file provides an overview and explanation of the code provided. The code performs various data analysis and visualization tasks on a dataset containing pollution level data.

## Libraries Used
- numpy
- pandas
- seaborn
- matplotlib
- sklearn.metrics
- math
- datetime
- statsmodels.api

## Data Loading and Preprocessing
- The code begins by loading the dataset from the "Data.csv" file using pandas.
- The columns of the dataset are extracted, with the 'date' column identified as the date column, and the remaining columns as the pollutants' data.

- Missing values in the dataset are handled using cubic interpolation to fill the gaps.

- Visualization: Average Pollution Levels
- The code plots the average pollution levels for different gases during a single day, averaged over a 90-day period. The graph shows the trends and patterns in pollution levels throughout the day.
- Noticeable increases in pollution levels are observed between the time interval of 13:45 and 14:45, suggesting a correlation with the blasting activities of coal in the region.
QQ Plot Analysis
- The code generates QQ plots for each pollutant, which are used to assess the distribution of the data.
The QQ plots compare the theoretical quantiles to the sample quantiles of the data. The plots help determine if the data follows a normal distribution or exhibits deviations.

- Seasonal Decomposition: The code performs seasonal decomposition on the pollutant data using the multiplicative model. Seasonal decomposition helps identify trends, seasonal patterns, and residuals in the data. The results are plotted to analyze the trend and seasonality components of the data.

Augmented Dickey-Fuller Test
- The code conducts the Augmented Dickey-Fuller (ADF) test to check the stationarity of the data. The ADF test assesses if the data has a unit root, indicating non-stationarity. The critical values, p-value, and ADF statistic are displayed to interpret the test results. Based on the results, the absence of trend and seasonality in the pollutant levels is concluded.

Autocorrelation Analysis
- The code plots the autocorrelation function (ACF) for each pollutant.The ACF helps identify the correlation between a time series and its lagged values. The results indicate the suitability of an Autoregressive (AR) model for describing the data.

Autoregressive Modeling
- The code fits an Autoregressive (AR) model to the pollutant data based on the identified patterns.The optimal value of p (number of lagged values) is determined using the partial autocorrelation function (PACF). The AR model summary is displayed, providing information on the model coefficients and statistical measures.

Conclusion
- This code provides valuable insights into the pollution level dataset, including trends, seasonality, stationarity, autocorrelation, and autoregressive modeling. The analysis and visualizations help understand the patterns and characteristics of the data.
