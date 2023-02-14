# Trading-notebook from scratch

This is a preliminary demonstration of my early algorithmic trading ideas, focused on optimizing trading signals using technical indicators such as bollinger bands and stochastic oscillator, with the goal of simulating cumulative returns from the most recent historical data of Ethereum and USD Tether.

## The project used jupyter notebooks:
1. Data Acquisition - Using the Coinbase Pro API to scrape the OHLC data of cryptocurrencies.
2. Trading Ideas -  Simulating the ideas of trading from scratch, data analysis, implementation of technical indicators, tuning of the window sizes of the technical indicators, a simple order books executing the buy and sell order in FIFO serving.
3. I have included the virtualenv requirements for python environment.

## Parameters in this notebooks
1. Data - granualarity is set to hourly interval.
2. Bollinger band window size is set to 18, upper band and lower band are both 2 standard deviation from the moving average.
3. Stochastic oscillator - K period = 14 * 30, - D period = 3 * 30.
4. The "my signal" is a signal I created, where the sell condition is when the price drop below bolllinger lower band and %D (slower simple moving average of the %K) < 20, the buy condition is when the price exceeds the bollinger upper band and %K > 80.

## Results
The cryptocurreny is an volatile asset.

## Limitations

1. This project was intended for learning.
2. It is worth noting that I am not yet implement alpha signal or portfolio optimisation in this particular project.
