# Time-Series-Analysis-using-ARIMA-and-Moving-Average
This post demonstrates processing and visualization of data for time series analysis. It also shows modelling with Moving Averages, ARIMA, Pivot Table, Dickey Fuller test,etc.

This dataset contains information about sales of a company's products and includes features such as type of customer segment, mode of shipment, name of customer, details about customer, name of product sold, quantity, discount, profit, sales, etc.
The task here is to analyze how the sales of the company changes w.r.t. key predictors and also to predict the sales at a near future date.

# Procedure followed

First we carry out some data exploration like number of null values, number of unique categories and sub-categories of products sold, and sales of each category.
We then remove redundant columns, which we would not use for our time series analysis. We chose only one category of products for our analysis (in this case, Office Supplies). We can as well take either of the product caegory for consideration.
Once we have the dataframe containing the time and the sales features, we format the dataframe with timeframe as our index. This will be handy for our time series plot.
After we have our preliminary plot of Sales v/s Time, we do some interesting Dataframe manipulation such as:
1) Creating Pivot Table of Sales and year (further subdivided into months), and plotting sales of each month.
2) We then plot variation of sales throughout each year separately

Next, we plot moving average curve and 12 Month Rolling Standard Deviation. 
Following which, we use seasonal decomposition on our 'Log of Sales' to understand trends like Seasonality, Residuality. We use Log of sales, in order to make the sales data relatively stationary (as verified by Dickey Fuller's p-value test)
Our data can be further stationarized by taking one-time-shift (backwards). 
Next, I plot ACF and PACF plot to understand the AR and MA terms and chose parameters (p,d,q) for our time-series-analysis.
Finally, I make use of these parameters for time-series forecast.
