# Analysis-on-Securitized-Assets
Various analysis performed to predict the performance of stocks/commodities/indices.

# Assets under consideration:

* Small Cap, Mid Cap, Large Cap (Blue Chip) Equities.
* Crude Oil
* Gold
* Nifty Index

# Analysis:

### I : Rudimentary EDA

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

### III : Regression - Beta Calculation

1. Data ingestion, Profile report

2. Summary Stats

3. Histogram of the GOLD frame.

4. Regressed OHLC values with 'Pred' & 'new', with statsmodel.api

5. New column in main frame based on OLS regression values obtained.

6. Feature elimination based on correlation and P values

7. Polynomial feature preprocessing for quadratic

8. CAPM and Beta Calculation

9. Superimposing stock daily percentage changes with Nifty index.

10. Separate frame computed for monthly returns. Beta computed. Compared with daily returns.
