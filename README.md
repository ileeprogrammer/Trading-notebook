# Trading Notebook from Scratch

Welcome to my early algorithmic trading demonstration, which highlights my ability to optimize trading signals by utilizing technical indicators such as Bollinger Bands and Stochastic Oscillator. My objective is to simulate cumulative returns from the most recent historical data of Ethereum and USD Tether.

## The project was executed using Jupyter Notebooks, and is comprised of the following steps:

Data Acquisition - I scraped OHLC data of cryptocurrencies from the Coinbase Pro API to ensure that I had the necessary data for analysis and strategy development.
Trading Ideas - My work focused on simulating trading ideas from scratch. Specifically, I performed data analysis and employed technical indicators, including the tuning of the window sizes of technical indicators. I also created a simple order book to execute buy and sell orders using FIFO serving.
I have included the virtualenv requirements for the Python environment to make it easier to replicate my work.

## Parameters in this Notebook

1. Data - I set granularity to an hourly interval to ensure that the data was both comprehensive and detailed enough for analysis.
2. Bollinger Band window size - I set it to 18, with the upper and lower bands both set at 2 standard deviations from the moving average.
3. Stochastic Oscillator - I set the K period to 14 * 30 and the D period to 3 * 30 to optimize trading signals.
4. "My Signal" - I created a signal where the sell condition is when the price drops below the Bollinger lower band and %D (the slower simple moving average of the %K) is less than 20. The buy condition is when the price exceeds the Bollinger upper band and %K is greater than 80.
5. I used "1" as a buy signal and "-1" as a sell signal. The order book executed a market order using the closing price to ensure that it remained simple.
The order book in the simulation followed a FIFO system to ensure that the orders were executed efficiently.

## Results
The following data is from 2022-11-01 to 2023-02-09 of Ethereum-USD Tether pair.

### Bollinger Bands
Total number of trades: 212

![my image](https://github.com/ileeprogrammer/Trading-notebook/blob/main/Figures/1.png)

![my image](https://github.com/ileeprogrammer/Trading-notebook/blob/main/Figures/2.png)

![my image](https://github.com/ileeprogrammer/Trading-notebook/blob/main/Figures/8.png)

### Stochastic Oscillator
Total number of trades: 36

![my image](https://github.com/ileeprogrammer/Trading-notebook/blob/main/Figures/3.png)

![my image](https://github.com/ileeprogrammer/Trading-notebook/blob/main/Figures/4.png)

![my image](https://github.com/ileeprogrammer/Trading-notebook/blob/main/Figures/7.png)

### My signal
Total number of trades: 34

![my image](https://github.com/ileeprogrammer/Trading-notebook/blob/main/Figures/5.png)

![my image](https://github.com/ileeprogrammer/Trading-notebook/blob/main/Figures/6.png)

### Summary
The results of this project demonstrate promising outcomes, as both the stochastic oscillator and my trading signal generated capital gains.

## Limitations and Future Work

As an early prototyping the trading idea, the work was treated as a data analysis project mainly worked in jupyter notebooks. the code in this project needs to be cleaned up and reorganized to ensure modularity.

It's important to note that this project does not yet incorporate alpha signals, financial risk management, or portfolio optimization. As such, my future work will focus on developing a comprehensive and wholistic multi-strategy trading system that includes the following design elements:
1. Robust data acquisition and vetting, with supplementary statistics to fill any missing data.
2. System architecture design and version tracking.
3. Backtesting and alpha analysis to optimize the portfolio.
4. Integration with brokerages and order submission capabilities.
5. Portfolio allocation and analysis to better understand performance.

By implementing these strategies, I will build a sophisticated trading system that can generate higher returns while managing risk effectively.
