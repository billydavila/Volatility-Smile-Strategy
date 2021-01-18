#                                                  Trading-Volatility-Smile

## Objective: In this repository, we will create a trading strategy using the volatility smile on the BankNifty call options index data and analyze the output model results. 

# Background 
We know that the volatility smile curve is a function of implied volatilities versus different strike prices on the same underlying with the same expiration date. A trading strategy based on the volatility smile can be created based on the fact the implied volatilities for at the money options will be the lowest and should be strictly increasing as the options go out or in the money on the smile curve. If there is a point on either side of at the money options in the volatility smile curve , where this condition is violated we can take a trading position till the implied volatilities are back on track and follow the expected smile curve. The idea behind it comes from the fact the option price is directly proportional to volatility and if there is an unusual increase in the implied volatility then the option would be overpriced and after the bump is removed, the option will go back to its fair value. We can collect a higher premium at this anomaly on the smile curve and once the anomaly is gone, we pay a lower premium and therefore collecting a profit. For risk management purposes the trading position we took was a long butterfly spread around the kinks.    
# Financial Data
We fetch data from an excel file that contains call option data of BankNifty for dates from Nov-01-2017 to May-21-2018. All the option data
was collected from the website https://www1.nseindia.com/products/content/derivatives/equities/historical_fo.htm. This financial data was used to calculate the implied volatility for each strike price which is necessary for plotting the smile curve for each date. Once we got the smile curve, we can implement the trading strategy. However, we needed to include transaction costs. The brokerage cost was based on the rules of( https://zerodha.com/charges#tab-equities ). 

# Analysis Results
For the analysis, we only calculated the Hit Ratio, Sharpe Ratio, Cumulative PNL, positive trades, negative trades, and Drawdowns of the strategy. We did not calculate more sophisticated profitable return measurements.  


