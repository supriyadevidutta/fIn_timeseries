
# Time Series Analysis and Prediction

This Repository Aims to observe Time series data and gain insights into the data and find patterns .It involves EDA for analyzing hypothesis and ML model building with data processed 
Company wise CSVs grouped by sector are analyzed 
The analysis is done sector wise to observe if companies within a sector follow a particular pattern 

EDA based observations:

1)Prepare the Data as a Dataframe and process further

2)Plot Candlestick for multiple time period 1 min, 5 min, 15 min, 1 Hr, 1 Day

3)Sectoral analysis in NIFTY 50 stocks

4)How each of the Stock price correlate with NIFTY 50 Index price movement , Statistical observation , Drawing Box plot, Heat map to understand the data

5)Can you verify that the Prices follows a cyclic trend during the trading hours between 9:30AM till 3:15PM

6)Do we see any weekly trend between Monday till Friday, what is the impact of Thursday weekly expiry on price movement

7)What is a right grouping of a trading week, Monday till Friday or Friday till Thursday

8)Do we see a correlation of high volume (MA20) influencing trend in the price.

9)What is the right distribution for price data, is it a stationary data, is it normally distributed

10)What is the right distribution for return data, is it a stationary data, is it normally distributed

11)Adding new features for time period data, 15 mins, 1 Hr, 1 Day etc.

12)Deriving additional statistical indicators MA, EMA, RSI, MACD, ADX, VWAP, TWAP

13)Optionally learning about open source platform like Quantopian, Alphalens,

##  [Consumer Goods](Consumer_Goods_EDA.ipynb):

Asian Paints, Britannia, Emami, Hindustan Unilever, ITC Ltd, Jubilant Food, Nestle India, Titan
are taken into consideration from this section 

first candlesticks are plotted for time frequencies of a day ,week, month and quarter to observe patterns 

    Asian paints : steady rise from 2017 to 2020 with peak at 2020 Jan 
    Britannia: considerable rise from july 2017 to july 2018 , sudden dip in first quarter of 2020
    Hindustan Unilever: steady and gradual rise from 2017 to 2020 
    ITC: relatively steady from 2017 to 2020 followed by sudden dip in 2020 first quarter 

Trend analysis based on price:

 plots ratio of given closing price with the initial price of data over past three years 
 Statistical indicator Moving average is taken up next , here moving average over 20,50 and 200 days are computed and plotted 


## [Gas and Oil](Gas&oil_EDA_Analysis.ipynb):
BPCL , Gail, IOC, ONGC, Reliance data is analyzed 

Candlestick representation of each of these dataset is plotted 

    BPCL: dipped from 2017 to 2019 ,peaked in 2020 and dipped again
    GAIL: remains in range 100-200 from 2017 to 2020 and then dips Jan 2020
    ONGC: small rise and falls till major fall in 2020
    RELIANCE: overall rise from 2017 to 2020

Trend analysis based on price is performed and closing price of all companies are plotted in a single frame for comparison 

Trend analysis of these closing prices is then plotted against nifty50 stock for looking for stock correlations 
Pairplot is plotted to show pairwise variation and heatmap to visualize correlation , it is observed nifty50 and reliance 
has high correlation with 0.72 score 

## [IT companies](IT_EDA_Analysis.ipynb):

 HCL , Infosys, TCS, Tech Mahindra, WIPRO are taken into consideration from this sector 

 candlestick for representing price movement is plotted first 

    HCL:steady rise till 2020 fall in first quarter
    INFOSYS: significant rise from 2017 to 2018 followed by rise and fall
    TCS and TECHMAHINDRA can be seen to be following a similar trend 

similar to EDA in oil and gas the closing prices are plotted 

next the volume trend is compared for all companies 

Similar to oil and gas sector Trend analysis of these closing prices is then plotted against nifty50 stock for 
looking for stock correlations,then distplot, pairplot and heatmap is plotted 
it is observed that here there is a high correlation of nifty50 with all companies compared 

In the EDA performed day of week based stock price trend is also looked into, here though there isn’t a sure trend we can observe that the returns on tuesday are lower than monday in most cases observed. 

## [Financial Services](Financial_services.ipynb):
The following EDA is performed for this sector:

* A kernel density estimate (KDE) plot is a method for visualizing the distribution of observations in a dataset, analagous to a histogram. KDE represents the data using a continuous probability density curve in one or more dimensions.
  probability density vs the closing prices of first 10 nifty50 data is plotted

*  A graph containing the closing prices vs the timestamp of first 250000 data in nifty50,nifty100,nifty500,niftyauto,niftybank,niftycommod,niftyenergy,niftyfin is plotted and the difference in the range of prices is observed

* A Q-Q plot provide an indication of univariate normality of the dataset.

* for the nifty50 data's clsoing price it is observed that the data does not follow a normal distribution and the data is heavy tailed.

*  A dickey fuller test indictes if a data is stationanry or not.here it is observed for the nifty50 data that the data is not stationary.

* An additive and multplicative decomposition analysis is done for the closing prices of niftybank data


## [Cement and Cement products](Weekly_trend.ipynb):
* Backtesting:
Ultratech data is taken into consideration here.
Mean of opening values for continuous periods of 9 and 21 rows are taken and plotted against each other to find the changes in stock price.
The return and start_return columns are plotted in the same frame to find if long holding of the stocks give any positive returns.

* Extensive on Ultratech:
Here Ultratech data is analysed.
Using a heat map to find the columns correlating with volume. Decomposing the time series data by year, month and week.
Plotting the total volume of stock traded and total stock closing price separately grouped year wise, month wise and weekday wise. Also using pie charts to plot volume traded for each year. Each month’s volume traded is summed with the same month in all years , as the same with weekday and the volume traded per month and weekday in cumulative is displayed as pie chart.

* Nifty 50 comparison:
Here both Ultratech and Grasim data are analysed.
The closing stock prices go nifty 50, Grasim and Ultratech are plotted against each other to find the variation in price. The same is done after normalising the values in the dataset using log.
The 3 stock prices are compared in distplot and pair plot to analyse them better.
A heat map is also drawn to see whether the prices are correlating to each other.

* Sectorial Analysis:
Here both Ultratech and Grasim data are analysed.
They are compared using pair plot. The 21 and 63 day price is found and they are plotted to gain a general understanding of how the stock price varies over a period of time. The values are standardised and plotted again. The closing value and rsi value of each stock are drawn. Then rolling window and intraday volatility is calculated.
The price of stocks only in Fridays are extracted and displayed. And days where the price fluctuation is large are also specifically got and displayed.



## [Simple moving average and exponential moving average](MA20_EDA.ipynb) : 
 The SMA calculates the average of the price data, but the EMA gives more weight to the actual data. 
 The latest price  data has a large impact on the moving average, and the old price data has a less impact.
  EMA weights new data more than old data, making it more responsive to the last price changes than SMA. 
  This will give you a more timely view of your EMA results and explain why  EMA is the preferred average for many traders. 
  

# Time Series Forecasting


Time Series Forecasting :


Given the task at hand is to predict y for a future x in a time series data ,ideally we can make use of AR model, MA model or ARMA model which are as explained below :

## AR model :
 Autoregression model, where we are trying to predict something based on its past value , it tries to capture pattern in the history of values recorded.
 We will consider only those lags of PACF which have direct effect either positive or negative with the value required and ignore those close to zero




## MA model: 
Moving average model , modelled as y= mean+ theta* error t-1 

## ARMA model:

Combining the equation of above two gives ARMA.


However , all these models require the data to be stationary 

## What makes a time series stationary : 
* mean is constant
* std deviation is constant: same fluctuation throughout timeline 
* no seasonality: periodic behaviour


To make a given series stationary we apply a differencing method where t-1 is subtracted from t , this is first order differencing , if this doesn’t result in stationary time series we repeat it to get second order differencing.


## [Arima](Arima-New.ipynb)
ARIMA equation has 3 terms:

P,d,q where p is order of AR, q of MA and d is the number of differencing required to make the series stationary , step one towards applying ARIMA is making the series stationary 
For this we subtract t-1 value from t value , the parameter d is the number of differencing required to make the series stationary.


To determine the value of d we keep performing differencing and check If the autocorrelations are positive for many number of lags (10 or more), then the series needs further differencing else if the lag 1 autocorrelation itself is too negative, then the series is probably over-differenced.
To determine value of p i.e. the AR term we evaluate the PACF plot , PACF can be considered the correlation of series and its lag w/o considering the values in between we initially take AR term to be equal to as many lags that crosses the significance limit in the PACF plot.
Similarly q is determined by plotting the ACF plot and counting lags that cross significant limit in the same.

Normally in an ARIMA model, we make use of either the AR term or the MA term. We use both of these terms only on rare occasions. We use the ACF plot to decide which one of these terms we would use for our time series, If there is a Positive autocorrelation at lag 1 then we use the AR model ,If there is a Negative autocorrelation at lag 1 then we use the MA model

Use AR terms in the model when the:
* ACF plots show autocorrelation decaying towards zero
* PACF plot cuts off quickly towards zero
* ACF of a stationary series shows positive at lag-1

Use MA terms in the model when the model is:
* Negatively Autocorrelated at Lag — 1
* ACF that drops sharply after a few lags
* PACF decreases more gradually

Using these parameters the ARIMA model is build and plot_predict can be used to check the predictions against real value, Out-of-Time cross validation gives the real test for the prediction for which we create train and test data but do not randomly sample it as the time series should be intact for prediction. 
The commonly used accuracy metrics to judge forecasts are:
1.	Mean Absolute Percentage Error (MAPE)
2.	Mean Error (ME)
3.	Mean Absolute Error (MAE)
4.	Mean Percentage Error (MPE)
5.	Root Mean Squared Error (RMSE)
6.	Lag 1 Autocorrelation of Error (ACF1)
7.	Correlation between the Actual and the Forecast (corr)
8.	Min-Max Error (minmax)

auto_arima uses a stepwise approach to search multiple combinations of p,d,q parameters and chooses the best model that has the least AIC.



## [Auto Arima](Auto_Arima.ipynb):

Auto arima model generates the optimal values of p,d,q suitable for the dataset for better forecasting 


In the Auto ARIMA model,  small p,d,q values represent non-seasonal components, and capital P, D, Q represent seasonal components. It works similarly like hyper tuning techniques to find the optimal value of p, d, and q with different combinations and the final values would be determined with the lower AIC, BIC parameters taken into consideration.


# [CANDLESTICK PATTERNS FOR CHART RECOGNITION](Chart_Algo.ipynb):

## Bullish Bearish:

Bullish patterns indicate that the price is likely to rise, while bearish patterns indicate that the price is likely to fall.

green: opening price > closing price 
red: closing price> opening price 

## Bearish Abandoned Baby:

●	A bearish abandoned baby is a rare pattern that has a fairly strong track record for forecasting a short-term downward trend.

●	The key item of the bearish abandoned baby is the middle day, which should have a gap in front of it and following it, and which should close the session with price unchanged.

●	The bullish variation of the pattern is the bullish abandoned baby which is equally rare and also has a good track record for forecasting a reversal towards an upward trend.


Doji is a name for a session in which the candlestick for a security has an open and close that virtually equal and are often components in patterns.


## Bullish Abandoned Baby:

●	The bullish abandoned baby is a three-bar pattern following a downtrend. 

●	It consists of a strong down candle, a gapped down doji, and then a strong bullish candle that gaps up.

●	This pattern signals the potential end of a downtrend and the start of a price move higher.

●	Some traders allow for slight variation. There may be more than one doji, or gaps may not be present after the first or second candle. But the overall psychology of the pattern should still be present.

## Hanging man:

●	The hanging man is a type of candlestick pattern and refers to the candle's shape and appearance, representing a potential reversal in an uptrend.

●	Candlesticks display a security's high, low, opening, and closing prices for a specific time frame and reflect the impact of investors' emotions on prices.

●	The hanging man occurs when two criteria are present: an asset has been in an uptrend, and the candle has a small real body and a long lower shadow.



## Doji star pattern: 
The appearance of a Bearish Doji Star candlestick pattern in a strong uptrend indicates that buyers are losing control and the market is deadlocked between buyers and sellers.  The deadlock seen in the Bearish Doji Star may be as a result of diminishing buying pressure or an increase in the selling force. Whatever the reason is, the Bearish Doji Star tells us that the strength of uptrend is now dissipating and the market is vulnerable to a setback. Technical analysts use bullish Doji Star candlestick to determine the reversal of the long current downtrend in the market. The experts consider bullish Doji Star Patterns as signals to buy. They also use it to watch time to avoid selling the assets. It mostly appears at the bottom of the chart. This act as a bell to inform that arrival of the bulls is imminent after a long bearish phase.

## Dark Cloud Cover:

●	Dark Cloud Cover is a candlestick pattern that shows a shift in momentum to the downside following a price rise.

●	The pattern is composed of a bearish candle that opens above but then closes below the midpoint of the prior bullish candle.

●	Both candles should be relatively large, showing strong participation by traders and investors. When the pattern occurs with small candles it is typically less significant.

●	Traders typically see if the candle following the bearish candle also shows declining prices. A further price decline following the bearish candle is called confirmation.

The Dark Cloud Cover pattern involves a large black candle forming a "dark cloud" over the preceding up candle. As with a bearish engulfing pattern, buyers push the price higher at the open, but sellers take over later in the session and push the price sharply lower. This shift from buying to selling indicates that a price reversal to the downside could be forthcoming.

## Gravestone DOJI:
Gravestone Doji is formed when the prices open and shoot higher instantly indicating new buying interest and strong bulls , but as the day comes to an end, the buying interest not just diminished but profit booking takes the prices back to the low or the opening price and finally closing where it opening, at or near the low.
The upper wick is very long but it has a very small lower shadow or ideally no lower shadow at all.

## Dragonfly DOji:
Whereas a Dragonfly Doji is formed when the prices open and heavy selling drags the price lower and lower until the selling vaporizes and the prices are low enough such that fresh buying interest and short covering take the prices higher and back to the opening price near the high.

## Bearish Engulfing Pattern:
A bearish engulfing pattern is seen at the end of some upward price moves. It is marked by the first candle of upward momentum being overtaken, or engulfed, by a larger second candle indicating a shift toward lower prices. The pattern has greater reliability when the open price of the engulfing candle is well above the close of the first candle, and when the close of the engulfing candle is well below the open of the first candle.

●	A bearish engulfing pattern can occur anywhere, but it is more significant if it occurs after a price advance. This could be an uptrend or a pullback to the upside with a larger downtrend.

●	Ideally, both candles are of substantial size relative to the price bars around them. Two very small bars may create an engulfing pattern, but it is far less significant than if both candles are large.

●	The real body—the difference between the open and close price of the candlesticks is what matters. The real body of the down candle must engulf the up candle.

●	The pattern has far less significance in choppy markets.

## Bullish Engulfing Pattern:
The bullish engulfing candle signals reversal of a downtrend and indicates a rise in buying pressure when it appears at the bottom of a downtrend.
This pattern reverses the ongoing trend as more buyers enter the market and move the prices up further.
The pattern involves two candles, with the second green candle that is completely engulfing the body of the previous red candle.

●	A bullish engulfing pattern is a candlestick pattern that forms when a small black candlestick is followed the next day by a large white candlestick, the body of which completely overlaps or engulfs the body of the previous day’s candlestick.

●	Bullish engulfing patterns are more likely to signal reversals when they are preceded by four or more black candlesticks.

●	Investors should look not only to the two candlesticks which form the bullish engulfing pattern but also to the preceding candlesticks.

## Evening Doji Star:
Evening star patterns are associated with the top of a price uptrend, signifying that the uptrend  is nearing its end. 

●	An evening star is a candlestick pattern used by technical analysts to predict future price reversals to the downside.

●	Although it is rare, the evening star pattern is considered by traders to be a reliable technical indicator.

●	The evening star is the opposite of the morning star pattern. The two are bearish and bullish indicators, respectively.

The evening star pattern is considered a very strong indicator of future price declines. Its pattern forms over a period of three days:
1.	The first day consists of a large white candle signifying a continued rise in prices.
2.	The second day consists of a smaller candle that shows a more modest increase in price.
3.	The third day shows a large red candle that opens at a price below the previous day and then closes near the middle of the first day.
The Evening Doji Star is a bearish reversal pattern, being very similar to the Evening The only difference is that the Evening Doji Star  needs to have a doji candle on the second line. 
Falling Window Bearish Pattern:
Falling Window is a two-candle bearish continuation pattern that forms during a downtrend. Both candles in the pattern can be of any type, with the exception of the Four-Price Doji. The most important characteristic of the pattern is a price gap between the first candle's low and the second candle's high. The existence of this gap (window) means that the bearish trend is expected to continue.

## Gravestone doji bearish Pattern:
●	A gravestone doji is a bearish pattern that suggests a reversal followed by a downtrend in the price action. 

●	A gravestone pattern can be used as a sign to take profits on a bullish position or enter a bearish trade.

●	The opposite of a gravestone doji is a dragonfly doji.


## Hammer Candlestick:
●	Hammer candlesticks typically occur after a price decline. They have a small real body and a long lower shadow.

●	The hammer candlestick occurs when sellers enter the market during a price decline. By the time of market close, buyers absorb selling pressure and push the market price near the opening price.

●	The close can be above or below the opening price, although the close should be near the open in order for the real body of the candlestick to remain small.

●	The lower shadow should be at least two times the height of the real body.

●	Hammer candlesticks indicate a potential price reversal to the upside.

## Bearish Harami:

●	A bearish harami is a candlestick chart indicator for reversal in a bull price movement.

●	It is generally indicated by a small decrease in price (signified by a black candle) that can be contained within the given equity's upward price movement (signified by white candles) from the past day or two.

●	Traders can use technical indicators, such as the relative strength index (RSI) and the stochastic oscillator with a bearish harami to increase the chance of a successful trade.

## Bullish Harami:
●	 bullish harami is a candlestick chart indicator used for spotting reversals in a bear trend.

●	It is generally indicated by a small increase in price (signified by a white candle) that can be contained within the given equity's downward price movement (signified by black candles) from the past couple of days.

## Harami Cross:
A harami cross is a Japanese candlestick pattern that consists of a large candlestick that moves in the direction of the trend, followed by a small doji candlestick. The doji is completely contained within the prior candlestick’s body. The harami cross pattern suggests that the previous trend may be about to reverse. The pattern can be either bullish or bearish. The bullish pattern signals a possible price reversal to the upside, while the bearish pattern signals a possible price reversal to the downside.

## Inverted Hammer candlestick:
Inverted Hammer is a single candle which appears when a stock is in a downtrend It’s an important candle because it can potentially reverse the entire trend – from downtrend to uptrend ,That is why it is called a ‘bullish reversal’ candlestick pattern.On the chart, since the candle looks like a hammer turned upside down – it’s called a ‘inverted hammer’.
Long Lower Shadow:
Long Lower Shadow is a bullish candlestick pattern. To indicate seller domination of the first part of a session, candlesticks will present with long lower shadows and short upper shadows, consequently lowering prices. 

## Long Upper Shadow:
Long Upper Shadow is a bearish candlestick pattern. To indicate buyer domination of the first part of a session, candlesticks will present with long upper shadows, as well as short lower shadows, consequently raising bidding prices.

## Marubozu candlestick:
A Marubozu is a hard to miss candlestick with a full long body and barely any shadows.This solid body indicates a strong movement in any particular direction may it be upside or downside.When a bullish (green/white) Marubozu is formed, it indicates that the moment the price opened, they traded higher and higher finally closing in the mid of an attempt to rise further. In simple term, the day’s low is formed at the opening price itself and the day’s high is formed when the trading session ends.Similarly, in a Bearish (Red or Black ) version, the opening and high price are the same where the closing occurs at the close of the day.
Morning Doji star pattern:
The Morning Doji Star is a bullish reversal pattern, being very similar to the Morning Star. The only difference is that the Morning Doji Star needs to have a doji  candle on the second line. The doji candle (second line) should not be preceded by or followed by a price gap. If a lower shadow of a doji candle would be placed below the first and the second line shadow we would deal with the Bullish Abandoned Baby pattern.It happens that two first candles are forming the Bullish doji star pattern.

## Morning star Bullish:
●	A morning star is a visual pattern made up of a tall black candlestick, a smaller black or white candlestick with a short body and long wicks, and a third tall white candlestick.

●	The middle candle of the morning star captures a moment of market indecision where the bears begin to give way to bulls. The third candle confirms the reversal and can mark a new uptrend.

●	The opposite pattern to a morning star is the evening star,which signals a reversal of an uptrend into a downtrend.


## On neck pattern:
The on neck  is a two line bearish continuation pattern. The first line is a candle having a black body, appearing as a long line. The second line is a candle with a white body, but its upper and lower shadows length cannot exceed more than twice the body length.
The closing price of the second candle is at the level of the first candle's low price.
The pattern appears in a downtrend and predicts its continuation. It should be confirmed on the following candles by a candle closing below the opening price of the second line.

## Piercing Pattern:
●	The piercing pattern is a two-day candle pattern that implies a potential reversal from a downward trend to an upward trend.

●	This candle pattern typically only forecasts about five days out. 

●	Three characteristics of this pattern include a downward trend before the pattern, a gap after the first day, and a strong reversal as the second candle in the pattern.

## Rising window:
The rising window is a candlestick pattern that consists of two bullish candlesticks with a gap between them. The gap is a space between the high and low of two candlesticks. it occurs due to high trading volatility. There must be space between the real bodies of two candles to form a Window (whether rising or falling); in fact, even their shadows should not overlap. During an uptrend, a Rising Window is a price gap that forms.The space between the candles represents the distance between the high of the previous candle and the low of the current candle. This trend indicates that the bulls are in control, and we can expect them to keep pushing the price higher. Examine the size of the gap to acquire a better understanding of the pattern’s message. For example, a high gap denotes a significant price increase, whereas a small gap denotes a modest (and unimportant) price change.

## Shooting star pattern:
A shooting star is a type of candlestick pattern which forms when the price of the security opens,rises 
significantly, but then closes near the open price.The distance between the highest price 
of the day and the opening price should be more than twice as large as the shooting star’s body.
It occurs at the end of uptrend and signals bearish reversal.

## Spinning top Candlestick:
●	A spinning top is a candlestick pattern that has a short real body that's vertically centered between long upper and lower shadows.

●	The real body should be small, showing little difference between the open and close prices.

●	Since buyers and sellers both pushed the price, but couldn't maintain it, the pattern shows indecision and that more sideways movement could follow.


## Tristar candlestick:
●	A tri-star is a three line candlestick pattern that can signal a possible reversal in the current trend, be it bullish or bearish.

●	Tri-star patterns form when three consecutive doji candlesticks appear at the end of a prolonged trend.

●	A tri-star pattern near a significant support or resistance level increases the probability of a successful trade.


## Tweezer Top pattern:
The Tweezer Top pattern is a bearish reversal candlestick pattern that is formed at the end of an uptrend.It consists of two candlesticks, the first one being bullish and the second one being bearish candlestick.Both the tweezer candlestick make almost or the same high.

## Tweezer Bottom pattern:
The bullish reversal candlestick pattern known as the Tweezer Bottom forms at the bottom of a downtrend. It is made up of two candlesticks, the first of which is bearish and the second of which is bullish.

Using these patterns attributes were added to mark the pattern each datapoint belongs to and these attributes were used to train a [LSTM model](ChartAlgoTrend.ipynb) to predict if today's return is greater than or less than the previous day's. 

## Results of models:
The above candlestick pattern based data was fed to a LSTM model for return prediction which gave
an accuracy of 50%
[SVM](SVM.ipynb):
SVM model predicts both P_Result and Volume labels.
Reliance dataset:
accuracy-52%
HDFC dataset:
accuracy-49%
3:24
[Neural Networks](Neural_Networks.ipynb):
Neural Network model predicts both P_Result and Volume label
Reliance dataset:
accuracy-53%
After grouping dataset by frequency of 60 Minutes:
accuracy-52
