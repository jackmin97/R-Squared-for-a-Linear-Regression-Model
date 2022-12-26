# R-Squared-for-a-Linear-Regression-Model
In this notebook, we will use the R-Squared parameter to measure the goodness of fit of a Linear Regression model. 

### 1. Read the Data
The price data for Bank Of America and J.P. Morgan stocks are stored in the CSV file. The CSV file contains the price data of the stocks from 1 January 2019 to 31 December 2019. The stock price of J.P. Morgan is predicted using the stock price of Bank of America using linear regression and is stored in a column. To read a CSV file, we can use the read_csv method of pandas.

We can see that the data consists of the stock price of BAC and J.P. Morgan and the predicted stock price of J.P. Morgan.

### Definition of R-squared
R-squared is also known as the Coefficient of Determination and is denoted by 𝑅2 - The R-squared explains the percentage of variation in the dependent variable, y, that is described by the independent variable, X. It is equal to the square of correlation.

The value of  𝑅2  always lies between 0 and 1.

𝑅2  will be 1 if and only if all the 𝑦𝑖's would be exactly equal to the respective 𝑦̂ 𝑖's. That means 𝑅2 will be 1 when the model will be able to predict all the values precisely. And 𝑅2 will be 0 when the model will not be able to capture any relationship between the 𝑋's and the 𝑦's.

### 2. Calculate R-squared
The R-squared is 0.82, which means that 82% of the variance in the stock price of J.P. Morgan is explained by the variance in the stock price of Bank of America.

Let us read another CSV file and check the value of  𝑅2 . This file has observed and predicted stock price of J.P. Morgan. This time, the stock price of J.P. Morgan has been predicted using the stock price of Nestle.

This time the R-squared value is 0.35, which means that only 35% of the variance in the stock price of J.P. Morgan is explained by the variance in the stock price of Nestle.

Let us have a look at the plot of the JPM Price vs BAC Price and JPM Price vs Nestle Price.

The first value (82%) is better as it explains more variance. In the first graph, you can see that the points are closer to the line of best fit and scattered in the second graph. This explains the difference between the two values of the  𝑅2 .
Intuitively, the change in the stock price of J.P. Morgan would be highly correlated to the change in the stock price of Bank of America and it would not be correlated to the change in the stock price of Nestle. This is because both, J.P. Morgan and Bank of America, belong to the same sector of Banking and are very sensitive to factors like interest rates. Nestle belongs to a different sector, Fast Moving Consumer Goods. The dynamics of this sector are different and are affected by different factors.

### Limitations of R-squared
R-squared does not allow us to see if the predictions are biased. This can be done by the analysis of the residuals. Any pattern in the residual plot will help us identify the bias in our model if any. Hence a high  𝑅2  alone will always not be a good statistic.
