# Exploring Trader-Performance-vs-Market-Sentiment-Analysis
# Overview

This project explores how trader performance changes with the market’s emotional backdrop — the Bitcoin Fear & Greed Index.
Instead of only looking at profit and loss, the idea was to step back and ask:
“Do traders win more when the market is fearful, or when it’s greedy?”
By merging raw trading data with sentiment scores, I tried to uncover patterns that could inspire smarter trading strategies.

#  Datasets

1. Historical Trader Data (Hyperliquid)
  * Trade-level details: account, symbol, side, execution price, size, leverage, PnL, and timestamps.
  * Over 200,000 rows of raw trades.

2. Bitcoin Fear & Greed Index
  * Daily scores (0–100) converted into categories: Extreme Fear, Fear, Neutral, Greed, Extreme Greed.
  * Acts as the market’s “mood”.

# Approach
The work followed a step-by-step process:

1. Cleaning & Preparation
  * Converted raw timestamps into proper datetimes.
  * Standardized PnL and position size into numeric formats.
  * Labeled trades as win/loss and buy/sell.

2. Daily Aggregation
  * Condensed trades into daily summaries: total PnL, win rate, average PnL, and trade counts.

3. Merging with Sentiment
  * Matched daily trader performance with the sentiment of that exact day.
  * Found ~449 days of overlap to analyze.

4. Analysis & Visualization
  * Compared average returns and win rates across sentiment categories.
  * Created boxplots and time-series charts to visualize how PnL shifts between Fear, Neutral, and Greed.
  * Tested differences with simple statistics (e.g., t-tests).

# Key Insights

* Fear periods → high risk, high reward. Traders experienced much higher variance in PnL.
* Greed periods → steadier but often lower returns.
* Neutral days → tended to flatten performance, offering no strong edge.
"Market sentiment isn’t just background noise — it shapes trader performance in meaningful ways."

# Deliverables
* Python scripts / notebooks for data prep and analysis.
* Cleaned + merged dataset (daily performance + sentiment).
* Visualizations (boxplots, time-series).
* Report (.docx) written in a storytelling style.

# Next Steps
* If extended further, I’d explore:
* Segmenting traders (some may thrive in Fear, others in Greed).
* Analyzing how sudden sentiment shifts impact trading.
* Backtesting strategies that adapt position sizing based on sentiment.
