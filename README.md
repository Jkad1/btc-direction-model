# btc-direction-model
Predicting Bitcoin's Next-Day Direction

**Goal:** Test whether simple price-based features can predict if Bitcoin closes up or down the next day.

**Method:** Downloaded daily BTC-USD data (2019 to present) with yfinance. Built features: daily return, 7- and 30-day moving-average distance, and 7-day volatility. Trained logistic regression and a random forest, using a time-based split (oldest 80% train, newest 20% test) to avoid look-ahead bias.

**Results:** Logistic regression ~50.9%, random forest ~50.4%, versus a 49.5% "always guess up" baseline.

**Conclusion:** Both models beat the baseline by only about 1 point, so these features carry very little signal. Daily crypto moves are noisy, and this model should not be used for trading.

**Next steps:** Add trading volume, longer-term trend features, and test across different market periods.
