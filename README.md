# Analysis-on-Securitized-Assets
Various analysis performed to predict the performance of stocks/commodities/indices.

# Assets under consideration:

Small Cap

Small cap is a term used to classify companies with a relatively small market capitalization. A company's market capitalization is the market value of its outstanding shares. In India, normally a company below market capitalization of (USD 1 Billion) is classified as small cap company. One can expect a relatively high volatility in Small Cap companies.

Mid Cap

A mid-cap company is a company with market capitalization above (USD 1 Billion) and less than (USD 4 Billion) . As the name implies, a mid-cap company falls in the middle of the pack between large-cap and small-cap companies, considered to be a safer investment than small cap companies at the cost larger possible gains.

Large Cap (Blue Chip)

Large cap is a shortened version of the term “large market capitalization.” In India, normally companies with the market capitalization higher than USD 4 Billion are considered as Large cap companies. Considered to be the safest of all equities, with very rare 'big' moves.

	
Crude Oil

Crude oil is one of the most important commodities in the world. It's an unrefined petroleum product composed of hydrocarbon deposits and other organic materials that can be refined to produce usable products such as gasoline, diesel and various types of petrochemicals. Also known as the 'Black Gold'.

Gold

Gold is respected throughout the world for its value and rich history, which has been interwoven into cultures for thousands of years. Coins containing gold appeared around 800 B.C., and the first pure gold coins were struck during the rein of King Croesus of Lydia about 300 years later. Throughout the centuries, people have continued to hold gold for various reasons. more recently so for investment purposes.

	
Nifty

Nifty is the reference index which is referred to by the investors on a daily basis. The direction of Nifty represents the trend of the market and most stocks tend to move in its direction. In short, Nifty is a benchmark index which comprises of 50 companies from 13 different sectors. These 50 companies are among the largest companies in India and are a proxy for the performance of Indian economy


# Analysis:

### I : Rudimentary exploration of the dataset using pandas.

1. Imported and analyzed the data using basic pandas functionality and pandas profile reporting.

2. Segregated the data for the past 3 month alone, to get a focused view.

3. Formatted Data column to datetime64[ns] dtype for future convenience.

4. Calculated the monthwise VWAP (Volume Weighted Average Price ) of the stock.

5. Tabulated Average closing price and P/L percentage for each date.

6. Tabulated additional column with daily percent change values of closing price.

7. Appended trend metadata (bull run, bear drop, positive, negative, et al.) based on the daily percentage values.

8. Calculated average and median values of traded volumes grouped by trend metadata.

### II : Data Visualization

1. Importing the dataset containing the price action data for one stock, and converting the Date column to datetime64[ns] format.

2. Stem plots retain their data value from the raw data to at least two digits. Ideal for plotting daywise data, it was used to display the daily percentage change in stock price.

3. Plotted and superimposed the chart for daily volumes on top of daily percentage change values.

4. Plotted pie chart containing specifics of the trend metadata which was calculated in the previous part.

5. Computed mean and median of total traded volume grouped by trend metadata.

6. Plotted a histogram of daily return percentages with frequencies of various values of percentage change.

7. Imported price action data for 5 stocks, extracted close price for each, and created a separate dataframe.

8. Used seaborn to plot the correlogram for the data.

9. The 7 day rolling average of the percentage change was calculated, thus deriving volatility. Standard deviation was calculated and plotted.

10. Volatility of NIFTY50 index was calculated, and the plot was superimposed to the volatility plot of the previously chosen stock.

11. 21 and 34 day moving averages were calculated and plotted. Trade call should be BUY whenever the smaller moving average (21) crosses over longer moving average (34) and the call should be SELL whenever smaller moving average crosses under longer moving average.

12. Bollinger Bands were plotted using 14 day rolling averages and std deviations. 
