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
