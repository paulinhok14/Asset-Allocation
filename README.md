## **Asset Allocation Model**

I created this model for a personal purpose, but feel free to use it if useful.

The asset allocation model consists of using libraries and APIs such as YahooFinance, GoogleFinance and also Brazilian Central Bank open data.

As soon as a Start and End Date is defined (01-01-2013 -> 20-10-2023 in the examples), price history data is calculated for 4 traditional asset classes, represented by indices:

**1- Emerging Market Equities** (IBOV), **2- Developed Economy Equities** (IVV, which represents the S&P500 + the USD/BRL exchange rate variation), **3- Real Estate** (IFIX) and **4- Fixed Income** (CDI, also considered a "risk-free rate" for the study).

![Historical Quotation](src/historical_quotation.png)

In addition to the historical variation plot, the Average Returns, Standard Deviation, and also the Covariance between the 4 asset classes are calculated.

![Return and Risk Assets](src/return_and_risk_assets.png)
![Correlation Matrix](src/correlation_matrix.png)

Given the assets characteristics, a N number of simulations are randomly executed (6000 in the example) changing portfolio weights and positioning return and risk on a scatter chart:

![Portfolios Simulation](src/portfolios_simulation.png)

Given these portfolios, it is possible to know the optimized allocation (weights) to produce a specific result, the Minimum Risk Portfolio for example:

![Optimized Min Risk](src/optimized_minimum_risk.png)
![Portfolios with Min Risk](src/portfolios_with_min_risk.png)

The optimized allocation for a Maximum Sharpe portfolio would be:

![Optimized Max Sharpe](src/optimized_maximum_sharpe.png)
![Portfolios with Max Sharpe](src/portfolios_with_max_sharpe.png)

All the portfolio simulations so far considers CDI (fixed income) a Risk-Free rate, so it was removed from covariance model. Now we add CDI as Risk-Free Rate on portfolios chart, making it Complete on a capital allocation line point of view: (risk 0 although it has a little bit higher standard deviation returns, let's say, 2%)

![Complete Optimized Portfolio](src/complete_optimized_portfolio.png)

After that, I've included a feature in which you can simulate a portfolio (Your Portfolio) and check it's expected return and expected risk. Given your input weights for each asset class, the covariance matrix is considered on pondering it for each Average Return and Standard Deviation statistics. In my example, I've set the string '[0.35, 0.15, 0.25, 0.25]', that is:

- 35% IBOV
- 15% IVV
- 25% IFIX
- 25% CDI

![Custom Portfolio](src/custom_portfolio.png)






