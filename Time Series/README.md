# Time Series Data Analysis

## Dataset 1: Lake Huron Water Level (1875-1972)

### Time Series Plot of Dataset
![Time Series Plot of Dataset](https://github.com/irfantaha/Projects-and-Assignments/blob/4e899b955177b12b0a252de361db279dfe58e135/Images/Lake%20Huron%201.png)

The dataset gives the annual water level of Lake Huron. As such, the series does not exhibit any seasonality as intra-year seasonalities such as the four seasons and glacier melt is not taken into consideration. The data seems to follow a downward trend up to roughly the year 1930. Afterwards, the downward trend disappeared.

Upon further research, it is interesting to note that the low water levels in the **1930s & 1960s** are caused by a reduced precipitation during the winter months, exacerbated by higher temperatures in summer, leading to increased evaporation. This is further proof of cyclicality which is confirmed by modern data showing lows again in 1998/99. (https://www.michigan.gov/egle/0,9429,7-135-3313_3677_3704-12566--,00.html)

### Linear Regression and Piecewise Linear Trend Models
![](https://github.com/irfantaha/Projects-and-Assignments/blob/4e899b955177b12b0a252de361db279dfe58e135/Images/Lake%20Huron%202.png)

The linear model does not take into account the change in trend at the knot at 1915 which seems to suggest there is no trend component in the series after 1915. As such, the forecast from the linear model predicts that the water level will continue dropping for the next 8 years.

The piecewise model provides the better forecasts compared to the linear model as it takes into account the trend change at the knot at 1915 as water level at Lake Huron seems to fluctuate around a common mean after 1915.

### ARIMA Models
![](https://github.com/irfantaha/Projects-and-Assignments/blob/4e899b955177b12b0a252de361db279dfe58e135/Images/Lake%20Huron%204.png)

Using the auto.arima() function from the 'forecast' library, the model obtained is ARIMA(2,0,0).

## Dataset 2: Monthly Sales of a Gift Shop in Queensland, Australia

### Time Series Plot of Dataset
![](https://github.com/irfantaha/Projects-and-Assignments/blob/37c3da8dfb6cf277664e5f073977bbb9fef40bf8/Images/Fancy1.png)

From the time plot of the dataset, we could observe a general upward trend and strong seasonality in the time series. The upward trend is expected as the shop expanded its business over the years. The ACF plot shows significant spikes at lags 12 and 24, indicating that there is a surge in sales in the month of December which is expected due to the large influx of visitors during the Christmas festivities. This seasonal spike in sales in the month of December is consistent throughout the years.

We could also observe an increase in monthly sales in the month of March. This could be explained by the influx of visitors to the beach during the annual local surfing festival every March since 1988.

However, we could see an unexpected fluctuation in December 1990 and March 1991. The growth in monthly sales in both months of March and December have been increasing throughout the years. However, in Dec 1990 and Mar 1991, the increase in the monthly sales is significantly smaller compared to previous years. Upon further research, a category 4 Cyclone Joy hit Queensland in Dec 1990, resulting in extensive flooding. This could potentially explain the unexpected fluctuations in both months, as the impact from the disaster would most likely result in the cancellation or postponement of the annual festival.

### Forecast - Total Monthly Sales
![](https://github.com/irfantaha/Projects-and-Assignments/blob/37c3da8dfb6cf277664e5f073977bbb9fef40bf8/Images/Fancy5.png)
