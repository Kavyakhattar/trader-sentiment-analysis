# Trader Behavior vs Market Sentiment Analysis

## Objective
Analyze how market sentiment (Fear vs Greed) influences trader behavior and performance using Hyperliquid trading data.

---

## Dataset
- Bitcoin Market Sentiment (Fear/Greed Index)
- Historical Trader Data (Hyperliquid)

---

## Methodology

### 1. Data Preparation
- Cleaned and standardized timestamps
- Converted sentiment into binary (Fear / Greed)
- Merged datasets on daily date level
- Handled missing values and ensured proper alignment

---

### 2. Feature Engineering
- Created `win` indicator (profitable trade or not)
- Aggregated daily PnL
- Derived behavioral metrics:
  - Trade frequency
  - Average position size (risk proxy)
  - PnL distribution

---

## Analysis & Findings

### 1. Performance Comparison
- Mean PnL is similar across Fear and Greed
- Win rate is nearly identical (~41%)
- However:
  - Greed shows **larger downside losses**
  - Fear shows **higher upside potential**

---

### 2. Behavioral Differences

- **Position Size:**
  - Higher in Fear → traders take larger risks (~7182 USD vs ~4635 USD)

- **Trade Frequency:**
  - Higher in Greed → overtrading behavior

- **Volatility:**
  - Fear markets show higher PnL variance

---

### 3. Key Insights

1. **Risk differs more than profitability**
   - Similar win rates but different risk exposure

2. **Fear → high risk, high reward**
   - Larger positions and higher volatility

3. **Greed → overtrading**
   - More activity without better outcomes

---

## Segmentation Analysis

- Frequent vs Infrequent traders
- Winners vs Losers
- High vs Low position size traders

Findings:
- Frequent traders underperform during volatile periods
- Consistent winners are less affected by sentiment
- High position traders gain more in Fear but face higher risk

---

## Strategy Recommendations

### Strategy 1: Risk Control in Greed
- Reduce position size
- Apply strict stop-loss rules
- Avoid overtrading

---

### Strategy 2: Opportunity in Fear
- Allow larger but selective trades
- Focus on high-conviction setups

---

### Strategy 3: Behavior-Based Strategy
- Frequent traders should reduce activity in volatile markets
- Consistent traders can maintain strategy across regimes

---

## Tools & Technologies
- Python
- Pandas, NumPy
- Matplotlib, Seaborn
- Scikit-learn (optional modeling)

---

## How to Run

```bash
pip install -r requirements.txt
jupyter notebook