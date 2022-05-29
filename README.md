# Securitized-Asset-Analysis
Various analysis performed to predict the performance of stocks/commodities/indices
(Citigroup Virtual Internship)

# Assets under consideration:

* Small Cap, Mid Cap, Large Cap (Blue Chip) Equities.
* Crude Oil
* Gold
* Nifty Index

# Executive Summary:

### I : Rudimentary EDA

1. Imported and analyzed the data using basic pandas functionality and pandas profile reporting
2. Segregated the data for the past 3 months alone, to get a focused view
3. Formatted Data column to datetime64[ns] dtype for future convenience
4. Calculated the monthwise VWAP (Volume Weighted Average Price ) of the stock
5. Tabulated Average closing price and P/L percentage for each date
6. Tabulated additional column with daily percent change values of closing price
7. Appended trend metadata (bull run, bear drop, positive, negative, et al.) based on the daily percentage values
8. Calculated average and median values of traded volumes grouped by trend metadata

### II : Data Visualization

1. Importing the dataset containing the price action data for one stock, and converting the Date column to datetime64[ns] format
2. Stem plots retain their data value from the raw data to at least two digits. Ideal for plotting daywise data, it was used to display the daily percentage change in stock price
3. Plotted and superimposed the chart for daily volumes on top of daily percentage change values
4. Plotted pie chart containing specifics of the trend metadata which was calculated in the previous part
5. Computed mean and median of total traded volume grouped by trend metadata
6. Plotted a histogram of daily return percentages with frequencies of various values of percentage change
7. Imported price action data for 5 stocks, extracted close price for each, and created a separate dataframe
8. Used seaborn to plot the correlogram for the data
9. The 7 day rolling average of the percent change was calculated. Standard deviation was calculated and plotted, thus deriving volatility
10. Volatility of NIFTY50 index was calculated, and the plot was superimposed to the volatility plot of the previously chosen stock
11. 21 and 34 day moving averages were calculated and plotted. Trade call should be BUY whenever the smaller moving average (21) crosses over longer moving average (34) and the call should be SELL whenever smaller moving average crosses under longer moving average
12. Bollinger Bands were plotted using 14 day rolling averages and std deviations

### III : Regression - Beta Calculation

1. Data ingestion, Profile report, Summary Stats
2. Histogram of the GOLD dataframe
3. Regressed OHLC values with 'Pred' & 'new', with statsmodels library.
4. New column in main frame based on OLS regression values obtained
5. Feature elimination based on correlation and P values
6. Polynomial feature preprocessing
7. CAPM and Beta Calculation
8. Superimposed stock daily percentage changes with Nifty index
9. Separate frame computed for monthly returns. Beta computed. Compared with daily returns

### IV : Algorithmic Trading using Classification

1. Summary Statistics and Profile Report
2. Computed Bollinger Bands for the given Security
3. New column for Trade Call based on conditionals on the previously computed bands
4. Defined features and labels and did a train/test split
5. Implemented several classification algorithms, namely: Logistic Regression, Naive Bayes, Stochastic Gradient Descent, KNN, Decision Tree, Random Forest, and Support Vector Machine
6. Computed evaluation metrics, such as: accuracy score, classification report, confusion matrix, and ROC curve; for all the above
7. Created new columns based on 5 day roling mean & standard deviation, and percentage change in OHLC values
8. Hyperparameter Tuning using RandomizedSearchCV and GridSearchCV for better ROC AUC score

### V : Efficient Frontier

1. Calculated daily returns based on the percentage chage in adjusted close price
2. Computed annualized mean, standard deviation, and the sharpe ratio
3. Created a mixed portfolio of mid and large cap equities
4. Computed mean daily returns, covariance matrix, and volatility
5. Assigned a random weight for each equity and compute portfolio return, portfolio volatility and porfolio sharpe ratio
6. Created a frame based on the above computation
7. Finding the optimal values of maximum sharpe ratio and minimum volatility
8. Scatter plotted the Efficient Frontier
9. Assigned a percentage value of occupancy of the portfolio for each equity

### VI : Clustering for Diversification

1. Using the Glob library to consolidate the datasets for the equity portfolio
2. Summary Statistics using Pandas Profiling
3. Plotting the Spearman and Pearson Correlation Maps
4. Calculating Returns and Volatility for the portfolio
5. Computing Optimal k value for KMeans Clustering using the Elbow Method
6. Applying KMeans Algorithm to cluster the portfolio
