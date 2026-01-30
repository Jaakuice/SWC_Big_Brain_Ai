---
title: Key Financial Metrics Reference
type: reference
category: financial
source_files:
  - Smarter Web Data.csv
  - /RNS/*results*.pdf
  - /Tennyson/RES_SWC_*.pdf
last_updated: 2026-01-29
---

# Key Financial Metrics Reference

## Purpose
Quick reference for key financial metrics tracked in the dataset, with data sources and selection guidance.

## Primary Data Source
**`Smarter Web Data.csv`** - Core quantitative dataset with hourly/daily granularity from IPO (2025-04-25) onwards.

## Key Metrics

### Share Price Metrics
- **Columns:** Open Price, Close Price, High Price, Low Price
- **Use Case:** Share price movements, volatility analysis
- **Code Execution:** Yes - time series plots, trend analysis

### Bitcoin Treasury Metrics
- **Columns:** BTC Balance, Bitcoin Buy, New BTC, New BTC Cost, BTC AV (average)
- **Use Case:** Bitcoin accumulation, purchase tracking
- **Code Execution:** Yes - filtering, aggregation, trend analysis

### Valuation Metrics
- **Columns:** Market Cap, Actual MNAV, Adjusted MNAV
- **Use Case:** Company valuation, mNAV tracking
- **Code Execution:** Yes - calculations, projections

### Sats Per Share
- **Columns:** BTC Sats Per Share, Sats Per Share Value
- **Use Case:** Bitcoin exposure per share
- **Code Execution:** Yes - filtering for latest value, trend analysis

### Share Structure
- **Columns:** Total Shares Outstanding, Share Issue, New Shares
- **Use Case:** Dilution tracking, share count changes
- **Code Execution:** Yes - matching with RNS dates

### Yield Metrics
- **Columns:** Yield To Date, Yield Daily
- **Use Case:** Performance tracking
- **Code Execution:** Yes - calculations, comparisons

### Cash
- **Column:** Cash
- **Use Case:** Cash position tracking
- **Code Execution:** Yes - filtering, trend analysis

## Secondary Sources

### RNS Financial Statements
- **Location:** `/RNS/` PDFs with "results", "interim", "annual" keywords
- **Use Case:** Official financial statements, validation
- **Known File:** `2025-07-25-interim-results.pdf`

### Tennyson Research
- **Location:** `/Tennyson/RES_SWC_*.pdf`
- **Use Case:** Broker estimates, yield projections
- **Cross-Reference:** Validate estimates against CSV actuals

## Selection Guidance

### Current/Latest Values
- Filter CSV for latest date (max "Date Time")
- Extract specific metric column

### Trends Over Time
- Filter CSV by date range
- Use code execution for plots and trend calculations

### Specific Events
- Match RNS dates with CSV dates
- Extract metrics around event dates

## Code Execution Examples

### Get Latest mNAV
```python
import pandas as pd
df = pd.read_csv('Smarter Web Data.csv')
latest = df.loc[df['Date Time'].idxmax()]
print(f"Latest mNAV: {latest['Actual MNAV']}")
```

### Plot Share Price Trend
```python
import pandas as pd
import matplotlib.pyplot as plt
df = pd.read_csv('Smarter Web Data.csv')
df['Date Time'] = pd.to_datetime(df['Date Time'])
df.plot(x='Date Time', y='Close Price')
plt.title('SWC Share Price Trend')
```

---

*This is a reference file. Always retrieve actual data from CSV for specific queries.*
