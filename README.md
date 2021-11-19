We are team of two people: Serikzhan Sadakbayev and Derrick

We are selecting Predicting Housing Prices (Linear Regression) topic.

For now, we are planning to use regression analysis to predict future housing prices, using different independent variables, that affect that market. Also we want to add mechanism that would make changes to our variables and correct them in case prediction of a housing prices wasn’t correct. 

First we download data set into computer using a link to raw data from git. We use 'requests' in order to download a data.
Then we import pandas and put our data into the dataframe.
Our aim is to see what highly affects on the price of houses, so we want to see correlation between sales price and other factors, so we use corr function to see it, then the result we sort values by SalesPrice column. Here we can see the following high correlations with sale price. The highest among all is OverallQual, which has 79% of correlation.
YearRemodAdd     0.507101
YearBuilt        0.522897
TotRmsAbvGrd     0.533723
FullBath         0.560664
1stFlrSF         0.605852
TotalBsmtSF      0.613581
GarageArea       0.623431
GarageCars       0.640409
GrLivArea        0.708624
OverallQual      0.790982

df.plot.scatter(x = 'SalePrice', y = 'LotArea')
Here we use scatter for SalePrice and LotArea and see that almost all of our LotArea is under 50k and SalePrice under 500k.
df.plot.scatter(x = 'SalePrice', y = 'OverallQual')
Next scatter helps us understand the range of each quality point price range
df.plot.scatter(x = 'SalePrice', y = 'GrLivArea')
Above grade (ground) living area square feet is also highly concentrated under 400k price range
df.plot.scatter(x = 'SalePrice', y = 'GarageCars')
Higher the number of cars in garage wider the range price of houses, but for 4 cars garage houses the range is the lowest.
