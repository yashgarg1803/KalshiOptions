# "Arbitrage" between Kalshi and NYSE S&P Options

Kalshi is an online events contact trading exchange.

One event that is traded is the weekly closing price of the S&P.

This is similar to a SPY option with an expiration date in a week.

We find the difference in the implied probability distribution function between the two exchanges.

We then buy or sell contracts on Kalshi depending on whether it is over or underpriced compared to SPY options on the market.

The rationale is that
1. Volume is lower on Kalshi, so the market is probably not as efficient.
2. There may be a larger recreational investors or people who bet "for fun", which could create inefficiencies.

We find that the strategy appears to be profitable over the tested time period, but
- there is a long time period of being on the verge of breakeven and then
- there is an unusual spike towards the end of the period.

Possible explanations for this:
- some change to kalshi markets themselves
- the source of options data is more accurate for recent months
- the S&P went down 16% in these months
- variance (350 markets, 2100 time periods, 25 expirations)

Some limitations of the model:
- Fee structure of Kalshi was not included (which could explain any inefficiency)
- Should calculate risk free rate, especially for longer term options
- Options data (which was free) was not the most precise

Check out the graphs in [the notebook](cdf.ipynb) for implied probability distribution/cumulative functions.