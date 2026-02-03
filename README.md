# primetrade_assignment
# Trader Performance vs Market Sentiment Analysis

## Objective
The objective of this project is to analyze how Bitcoin market sentiment
(Fear, Extreme Fear, Neutral, Greed, Extreme Greed) relates to trader behavior
and performance on the Hyperliquid platform. The goal is to uncover patterns
that can inform smarter, sentiment-aware trading strategies.

---

## Datasets
1. **Bitcoin Fear & Greed Index**
   - Daily market sentiment classification
   - Columns: timestamp, value, classification, date

2. **Hyperliquid Historical Trader Data**
   - Transaction-level trading data
   - Includes account details, trade direction, size, timestamps, and PnL

---

## Methodology
- Loaded and inspected both datasets for missing values and duplicates
- Converted timestamps to datetime format and aligned data at a daily level
- Merged trader activity with corresponding market sentiment
- Engineered key performance and behavioral metrics:
  - Daily PnL per trader
  - Win rate
  - Trade frequency
  - Exposure proxy using Start Position
  - Long/Short (Buy/Sell) ratio
- Performed sentiment-based analysis and trader segmentation

---

## Key Insights
1. Trader performance shows higher volatility and lower median PnL during
   Fear and Extreme Fear regimes.
2. Trade frequency and exposure tend to increase during negative sentiment,
   indicating more reactive trading behavior.
3. Traders exhibit contrarian behavior during Extreme Fear (long bias),
   while Extreme Greed periods show a strong short bias.
4. High-exposure traders underperform during Fear regimes, whereas
   low-exposure traders maintain more stable performance.

---

## Actionable Strategies
- **Risk Reduction During Fear Regimes:**  
  High-exposure traders should reduce position sizes during Fear and Extreme Fear
  periods to limit drawdowns and volatility.

- **Selective Activity During Greed Regimes:**  
  Increased trade frequency during Greed periods should be limited to traders
  with historically consistent performance, as infrequent traders do not
  significantly benefit.

---

## Future Work
Future extensions could include predictive modeling of next-day trader
profitability using sentiment and behavioral features, or clustering traders
into behavioral archetypes for personalized strategy recommendations.

---

## How to Run
1. Place both CSV files in the same directory as the notebook
2. Open the notebook and run all cells sequentially
3. All analysis and visualizations will be generated within the notebook

