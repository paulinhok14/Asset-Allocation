#### Asset Allocation Model

I created this model for a personal purpose, but I believe it can be useful to anyone interested.

The asset allocation model consists of using libraries and APIs such as YahooFinance, GoogleFinance and also Brazilian Central Bank open data.

As soon as a Start and End Date is defined (01-01-2013 -> 20-10-2023 in the examples), price history data is calculated for 4 traditional asset classes, represented by indices:

1- Emerging Market Equities (IBOV), 2- Developed Economy Equities (IVV, which represents the S&P500 + the USD/BRL exchange rate variation), 3- Real Estate (IFIX) and 4- Fixed Income (CDI, also considered a "risk-free rate" for the study).

![Historical Quotation](src/historical_quotation.png)

In addition to the historical variation plot, the Average Returns, Standard Deviation, and also the Covariance between the 4 asset classes are calculated.

![Correlation Matrix](src/correlation_matrix.png)
