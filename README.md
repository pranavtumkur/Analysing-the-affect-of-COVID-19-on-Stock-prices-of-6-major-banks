# Analysing-the-affect-of-COVID-19-on-Stock-prices-of-6-major-banks

This is an analysis of the LIVE stock prices (as on 12/06/2020) of how COVID-19 impacted the stock prices. We try to find out the banks with biggest losses and analyse which banks would the riskiest to invest in. We will also do a corelation analysis to see which banks have been performing exceptionally well or exceptionally bad compared to the performance of other banks, to determine if there has been any other factor apart from the economy for the dip/rise.

![rsz_960x0](https://user-images.githubusercontent.com/65482013/85416360-fd1f7400-b58b-11ea-8b24-5868ea676e46.jpg)

We do this analysis for 6 major banks, viz.:
*  Bank of America
* CitiGroup
* Goldman Sachs
* JPMorgan Chase
* Morgan Stanley
* Wells Fargo

## The Data

We will analyse 2.5 years' data, i.e from 01<sup>st</sup> Jan 2018 to date (12<sup>th</sup> Jun 2020). The souce of this is the [Stooq Index Data](https://pandas-datareader.readthedocs.io/en/latest/remote_data.html) This site essentially mirrors the Google Finance API data which gives a minute-to-minute live data of all stocks. We follow the following steps to grab data from the Stooq site API:
1. Use the required date range to set start and end datetime objects.
2. Query the stooq API using the ticker symbol for each of the 6 banks.
3. Use the DataReader method from pandas_datareader library to grab data from the API
4. Store the info in separate Dataframes and concatenate all the info into a useable format

## EDA

We transform the data to explore various aspects and to gain useful insights from it. We also create a new empty DataFrame using a UDF which contains the returns for each bank's stock. Today's Returns are typically defined as the percent change in Closing stock price today compared to the Closing stock price yesterday.

## Questions which we try to answer

1. What has the effect of COVID-19 been on stock price?
2. Has it affected some banks more than others? If yes, then whom and by how much?
3. When did the banks have the worst day? Why?
4. When did the banks have the best day? Why?
5. Which are the riskiest banks (historically) to invest in?
6. Which are the riskiest banks to invest in as of now?
7. How corelated are the bank performances? Has there been any other factor apart from the economy for the dip?

## Conclusions
### Some conclusions that can be drawn from the project (these are as per my knowledge of the stock market and are only valid as on 12/06/2020):

• **All relative plots from 2018-2020 look grossly normal. This tells us that whatever ups and downs were seen in the market were seen across all banks**

• **5 out of 6 banks had the worst day on 12-03-2020.**
This was the day the COVID-19 was reported as an epidemic and a major scare had spread especially in the US. More info can be found in this CNBC news article: https://www.cnbc.com/2020/03/12/stock-market-today-live.html

• **5 out of 6 banks had the best day on 13-03-2020.**
There was nothing jolly about this day; the previous day dip was so large that even a shred of returning to normalcy seems like the best gain. More info can be found in this CNBC news article: https://www.cnbc.com/2020/03/13/stock-market-today-live.html

• **Citigroup would be the riskiest if we consider the entire 2018-2020 (albeit by a small margin)**

• **In 2020 the riskiest would definitely be Citigroup! by a large margin**

• **WFC has the weakest corelation with the other banks. This means that the closing values of other banks and WFC are not very similar. This is because WFC has consistently held better closing values**
