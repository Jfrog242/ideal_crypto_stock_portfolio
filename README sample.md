# Custom portfolio Risk / Return Calculator

### About The Project




![dashboard]()




### Team 1 Group Members:

* [Jon Iadonisi](https://github.com/Jfrog242)
* [Fai Kongchai](https://github.com/jkongchai)
* [Daniel Faulks](https://github.com/Danebob86)
* [Brock Freeman](https://github.com/Bfree22)



### As cryptocurrency becomes more mainstream and investors and institutions allocate more of their money, it becomes even more important to understand the risks of investing in crypto long term. Our risk calculator and custom portfolio analysis allows you to compare the risk and return of a diversified portfolio with cryptocurrency and stock assets. Using this technique, retail traders or crypto analyst can easily run a simulation and portfolio analysis over the stocks or digital assets they choose.


## Questions asked

* How could we make crypto investing less risky for the average person?
* How accurate would our risk / return calcualtions and simulations be?
* How do we get the data?
* Why did we include more crypto assets than stocks?
* Is this program easy enough for the average retail trader to use and understand?
* How were we going to perform the analysis? Which modules would best show the portfolio returns and risk?


### We thought these questions were most important when performing our analysis and calculations because our main objective was to help retail investors see the risk / return of their own portfolio with an easy to use dashboard to see the results on. We thought choosing 6 crypto assets and 3 stock indeces was the best way to show the potential volatility of a diversified portfolio. Our risk slider, and input functions makes it easy for the user select their investment amount, investment time period, while also adjusting their risk level using the risk slider.






## Questions & Data

* To find our data we used the yfinance library to retrieve the historical price data from the selected cryptocurrencies and stock indeces. 

![library-gif]()

* Import yfinance
  ```
  import yfinance as yf
  ```
  
  ## Data Cleaning
  
  * We cleaned the data by getting the prices from yfinance API, and using Pandas library to drop null values and sort the index by datetime. While cleaning the data, we noticed that most of the cryptos had null values due to them being around 2-3 years old. Some insights when getting the data were the correlation between the price changes going back to 5 years. Many cryptocurrencies have related price action. 
  
  
  

  [drop_values](2021-06-08_19.47.08.gif) 



  
## Data Analysis

#### The following analysis modules were performed to calculate the volatility, correlation, annual returns, and projected simulated returns of the custom portfolio.

  * Correlation (Heatmap)
  * Volatility
  * Covariance
  * Sharpe Ratio
  * Weighted Portfolio
  * Monte Carlo Simulation
  


### Correlation (Heatmap)



![heatmap]()


#### According to the heatmap above, our findings resulted in showing the correlation between the crypto and stock assets. You can see that a majority of crypto assets seem to be closely correlated, while the stock indeces are no where near correlation with the crypto assets.




### Volatility (Histogram)


[histogram](Screen%20Shot%202021-06-07%20at%204.59.51%20PM.png)


#### We can plot out the price returns on a histogram chart. The wider the distribution the more volatile it is. You can see that sp500 is mostly within the mean distribution. But cardano spreads widely across the x-axis. Sometimes the returns can be 10%,15% or 20%. But you will never see a day sp500 up 15%.

#### The full portfolio shows that the volatility of the selected assets are diversified showing crypto assets as the most volatile assets in the portfolio. We can see the volatility level of the crypto assets based on the wideness of the histogram.





### Covariance


[covariance](Screen%20Shot%202021-06-07%20at%205.53.53%20PM.png)



#### Covariance tells us the relationship between the variables. We are trying to find if there is a linear relationship between assets. For example, if bitcoin gains 5%, how do the returns of sp500 correspond to it? Does it also gain 5%? Or does it show no response to it? That is one way to think about covariance. Let’s see their annual. The variance of sp500 is 0.036586. The variance of bitcoin is 0.5960695. The covariance between bitcoin and sp500 is 0.024520 At this point in time, we can only tell that a positive covariance value means there is a positive linear relationship. In order to find the strength of the relationship, we used the correlation function

#### You might ask, why do we need to calculate the covariance or correlation? This is because the volatility of one’s portfolio depends on three things.

* The standard deviation of the individual assets
* Weight of the assets
* Covariance between the assets

#### Hence, the covariance value is one of the inputs that we need to calculate portfolio volatility. The lower the covariance between the two assets, the lower the volatility. This is because they do not move in tandem. Generally speaking, a portfolio of assets that have a high correlation or covariance between one another usually has higher volatility.


### Sharpe Ratio


[Sharpe Ratio](Screen%20Shot%202021-06-07%20at%206.07.11%20PM.png)



#### By finding the sharpe ratio, we were able to find the point where the adjusted-risk return is the highest. The chart above shows a sharpe ratio of 1.22 for a portfolio with 82% Nasdaq and 18% Cardano. 

Discussion
  * Discuss your findings. Did you find what you expected to find? If not, why not? What inferences or general conclusions can you draw from your analysis?
* Postmortem
  * Discuss any difficulties that arose, and how you dealt with them.
  * Discuss any additional questions that came up, but which you didn't have time to answer: What would you research next, if you had two more weeks?
* Questions








## Libraries Used

### Prerequisites

Make sure to install the following libraries and packages before proceeding.

* Import yfinance
  ```
  import yfinance as yf
  ```
  
* Import dash
``` 
import dash
```
* Import pandas
```
import pandas as pd
```
* Import interact
```
from panel.interact import interact
```


### Tools Used

The 5-year historical prices for the selected cryptocurrencies and stock indeces were pulled from the following API's.

* [Yahoo Finance](https://finance.yahoo.com)
* [MCForecastTools]()






## Usage

This project is a great tool for someone wanting to know how to get cryptocurrency or stock price data from an API to build their own dashboard. This project also allows you to compare stocks and crypto assets. The Monte Carlo simulation and Regression modules are some of the most accurate ways of showing potential returns and outcomes for the selected assets. Below you can see the Monte Carlo simulation showing a predicted outcome of your portfolio.



## Contact

Jon -- 202-403-4115 © jon.iadonisi@gmail.com
Fai -- (469) 560-0102 jkongchai@gmail.com 
Daniel - (214)-738-3112 danielfaulks@gmail.com,
Brock -- (806)-790-0683 brockfreeman7@gmail.com 


Project Link: 
[https://github.com/Danebob86/team1_project1](https://github.com/Danebob86/team1_project1)



## Acknowledgements






## Q and A

### Open to questions! 


