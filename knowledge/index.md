# SWC Knowledge Index

## Purpose
This index maps queries to relevant data sources and provides selection guidance for efficient progressive disclosure. Always consult this index before selecting files.

---

## Key Entities & Aliases

### People
- **Andrew Webley** (CEO): Andy, @asjwebley, asjwebley, Mr Webley, CEO, Andrew
- **Jesse Myers**: Croesus, @Croesus_BTC, Croesus_BTC, Jesse

### Companies
- **The Smarter Web Company**: SWC, Smarter Web, smarterwebuk, @smarterwebuk, The Smarter Web Company PLC
- **Stock Tickers:** AQUIS: SWC, OTCQB: TSWCF, FRA: 3M8
- **Tennyson Securities**: Tennyson, the broker, corporate adviser
- **Bitcoin Treasuries World**: BTW, Bitcoin Treasuries, the show

---

## Query-to-Category Mapping

| Query Type | Primary Source(s) | Secondary Source(s) | Code Execution? |
|------------|------------------|---------------------|-----------------|
| Financial metrics (current/latest) | `Smarter Web Data.csv` | RNS (for context) | Yes - filtering |
| Financial trends over time | `Smarter Web Data.csv` | - | Yes - plots/calculations |
| Bitcoin purchase announcements | RNS PDFs (filter by date/keyword) | CSV (quantitative), YouTube (CEO commentary) | Optional - date filtering |
| Share price movements | `Smarter Web Data.csv` | RNS (catalysts), YouTube (sentiment) | Yes - time series |
| mNAV calculations/projections | `Smarter Web Data.csv` | YouTube (mNAV updates), Tennyson (estimates) | Yes - calculations |
| Sats per share | `Smarter Web Data.csv` | - | Yes - filtering |
| CEO views/statements | `/Tweets/asjwebley/` JSONs, YouTube transcripts | - | Optional - keyword search |
| Company announcements | `/Tweets/smarterwebuk/` JSONs, RNS PDFs | - | Optional - date filtering |
| Independent analysis | `/Tweets/Croesus_BTC/` JSONs, Tennyson PDFs | - | Optional - keyword search |
| Regulatory filings | RNS PDFs (filter by date/type) | - | No |
| Broker research | Tennyson PDFs | CSV (for validation) | Optional - cross-check |
| Strategy discussions | YouTube transcripts, CEO tweets | RNS (official statements) | No |
| Historical context | Legacy media, early RNS/YouTube | - | No |
| Predictive/projection queries | CSV (trends) + explicit statements (RNS/YouTube/Tweets) | - | Yes - trend analysis |

---

## Data Source Details

### `/Smarter Web Data.csv` (Root)
**Purpose:** Core quantitative dataset
**Key Fields:** Date/Time, Share prices, BTC price (GBP), BTC balance, Bitcoin purchases, Share issuance, Market cap, mNAV, Sats per share, Cash, Yield metrics, Tennyson signals
**Time Range:** IPO (2025-04-25) onwards, hourly/daily granularity
**Selection Tips:**
- Use for any quantitative query
- Filter by date range for trend analysis
- Cross-reference with RNS for purchase dates
- Use code execution for filtering, aggregation, plots

### `/RNS/` (106 PDFs)
**Purpose:** Official regulatory announcements
**Date Range:** April 2025 - January 2026
**Key Types:**
- Bitcoin purchase announcements (filter by "Bitcoin" or "purchase")
- Share issuances (filter by "placing", "subscription", "bookbuild")
- Director appointments (filter by "director" or "appointment")
- Trading updates (filter by "trading update")
- Financial statements (filter by "results", "interim", "annual")
- TR1 notifications (filter by "TR1")
**Selection Tips:**
- Filenames contain dates (YYYY-MM-DD format)
- Use date-based selection for time-specific queries
- Keyword search in filenames for type-specific queries
- Cross-reference with CSV for quantitative validation

### `/Youtube/` (90 .txt files)
**Purpose:** Video transcripts with CEO insights and strategy discussions
**Date Range:** April 2025 - January 2026
**Key Series:**
- "A Week In The World Of SWC" (Episodes #3-21) - Weekly updates
- "Smarter Webley Wednesdays" - Regular CEO segments
- mNAV update videos - Quantitative updates
- Interviews and panel discussions
**Selection Tips:**
- Filenames start with date (YYYY-MM-DD)
- Filter by date range for time-specific queries
- Search titles for keywords (e.g., "mNAV", "Bitcoin", "strategy")
- Use for CEO perspective, qualitative insights, strategy discussions
- Cross-reference with CSV for quantitative validation

### `/Tweets/asjwebley/` (18 JSON files)
**Purpose:** CEO's direct communication and real-time commentary
**Date Range:** June 2024 - January 2026
**Format:** `posts-YYYY-MM.json`
**Statistics:** 861 meaningful posts
**Selection Tips:**
- Use monthly files for time-specific queries
- Load recent months (2026-01, 2025-12) for "latest" queries
- Use code execution for keyword filtering across multiple files
- Cross-reference with YouTube for consistency
- Use for personal views, real-time reactions, direct communication

### `/Tweets/smarterwebuk/` (11 JSON files)
**Purpose:** Official company announcements and updates
**Date Range:** March 2025 - January 2026
**Format:** `posts-YYYY-MM.json`
**Selection Tips:**
- Use for official company communication
- Cross-reference with RNS for formal announcements
- Use code execution for keyword/date filtering

### `/Tweets/Croesus_BTC/` (12 JSON files)
**Purpose:** Independent Bitcoin treasury company analysis
**Date Range:** February 2025 - January 2026
**Format:** `posts-YYYY-MM.json`
**Selection Tips:**
- Use for independent perspective on SWC
- Cross-reference with official sources for verification
- Use code execution for keyword filtering

### `/Tennyson/` (20 PDFs)
**Purpose:** Broker research and deal documentation
**Date Range:** May 2025 - October 2025
**Naming:** `DL_SWC_*.pdf` (Deal Letters), `RES_SWC_*.pdf` (Research Reports)
**Selection Tips:**
- Use for broker analysis and yield estimates
- Cross-reference with CSV for validation
- Filter by date for time-specific research
- Use for investment analysis and projections

### `/Smarter Web/` (9 text files)
**Purpose:** Company documents, governance, investor materials, research
**Key Files & Triggers:**
| File | Use When Query Mentions |
|------|------------------------|
| `16-01-2026-swc-prospectus.txt` | prospectus, LSE uplisting, FCA, risk factors, Main Market, Bitcoin treasury risks, regulatory |
| `AdmissionDocument.txt` | AQUIS, AQSE, IPO, how went public, listing, reverse takeover, shell company, history, founding |
| `smarterweb-investor-presentation.txt` | investor presentation, investment thesis, pitch deck, why invest, valuation, strategy |
| `2025-07-16-P-BYD-Ratio.txt` | P/BYD, valuation, Jesse Myers, how to value Bitcoin companies, yield, mNAV methodology |
| `2025-07-25-interim-results.txt` | interim results, H1 2025, financials, earnings, profit/loss, revenue, balance sheet |
| `Corporate governance...txt` | corporate governance, QCA Code, governance principles, board responsibilities, compliance |
| `Directors & advisers...txt` | board, directors, advisers, Tyler Evans, Sean Wade, Randal Casson, Martin Thomas, Albert Soleiman, CFO, chairman |
| `Equity snapshot...txt` | shares outstanding, warrants, shareholders, dilution, ownership, 210k Capital, Smarter Convert |
| `Who we are...txt` | company overview, team, employees, staff, Jesse Myers role, Alex Wrench, what does SWC do, web design |

**Multi-File Selection Guide (triggers overlap):**
- **Andrew Webley queries** → Directors & advisers (bio) + Who we are (role) + interim-results (CEO statement)
- **Jesse Myers queries** → Who we are (role) + P-BYD-Ratio (his research)
- **Board/directors queries** → Directors & advisers (bios) + Who we are (overview) + Corporate governance (duties)
- **Valuation queries** → P-BYD-Ratio (methodology) + investor-presentation (thesis) + prospectus (metrics)
- **Company history queries** → AdmissionDocument (full) + Who we are (summary)
- **Risk queries** → prospectus (official risks) + Corporate governance (risk management)

### `/Legacy media/` (10 files)
**Purpose:** Historical media coverage and external perspective
**Types:** News articles (.txt), TV appearances (.txt)
**Date Range:** March 2025 - September 2025
**Selection Tips:**
- Use for external perspective and historical context
- Cross-reference with official sources for accuracy

---

## Code Execution Opportunities

### When Code Execution Adds Value

1. **CSV Analysis:**
   - Filtering by date range
   - Calculating trends (moving averages, growth rates)
   - Aggregations (total purchases, average mNAV)
   - Plotting time series (share price, BTC balance, mNAV)
   - Projections based on historical trends

2. **Tweet Analysis:**
   - Keyword filtering across multiple JSON files
   - Date range filtering
   - Engagement metrics analysis
   - Sentiment patterns (if needed)

3. **Cross-Referencing:**
   - Matching RNS dates with CSV purchase data
   - Validating Tennyson estimates against CSV actuals
   - Correlating YouTube dates with share price movements

4. **Calculations:**
   - mNAV projections
   - Sats per share calculations
   - Yield calculations
   - ROI on Bitcoin purchases

### When NOT to Use Code Execution

- Simple lookups (e.g., "What did Andrew Webley say about X?")
- Reading single RNS files
- Reading single YouTube transcripts
- Basic date-based file selection

---

## Selection Strategy Examples

### Example 1: "What is the current sats per share?"
**Files:** `Smarter Web Data.csv` (1 file)
**Code:** Yes - filter for latest date, extract "BTC Sats Per Share"
**Justification:** Quantitative query requiring CSV data only

### Example 2: "Summarize Andrew Webley's view on Bitcoin treasury risks"
**Files:** 
- Recent YouTube transcripts (filter by date, "Andrew Webley")
- Recent tweet files (`posts-2026-01.json`, `posts-2025-12.json`)
**Code:** Optional - keyword search for "risk"
**Justification:** Qualitative query requiring CEO's direct statements

### Example 3: "How has share price reacted to major RNS announcements?"
**Files:**
- `Smarter Web Data.csv` (for share price data)
- RNS PDFs (filter by major announcements: "placing", "Bitcoin purchase", "results")
**Code:** Yes - match RNS dates with CSV dates, plot price movements
**Justification:** Requires quantitative analysis + date matching

### Example 4: "Project potential mNAV in 2027 if Bitcoin reaches $200,000"
**Files:**
- `Smarter Web Data.csv` (for historical trends and current BTC balance)
- RNS/YouTube (for explicit forward-looking statements)
**Code:** Yes - trend analysis and projection calculations
**Justification:** Predictive query requiring calculations + explicit statements

### Example 5: "Compare Tennyson Research yield estimates with actual CSV data"
**Files:**
- Tennyson PDFs (for estimates)
- `Smarter Web Data.csv` (for actuals)
**Code:** Yes - extract estimates, match dates, compare with CSV
**Justification:** Cross-verification requiring quantitative comparison

### Example 6: "What are the key risk factors disclosed in SWC's prospectus?"
**Files:** `/Smarter Web/16-01-2026-swc-prospectus.txt` (1 file)
**Code:** No - direct reading
**Justification:** Prospectus contains official FCA-approved risk disclosures

### Example 7: "Summarize SWC's investment thesis from their investor presentation"
**Files:** `/Smarter Web/smarterweb-investor-presentation.txt` (1 file)
**Code:** No - direct reading
**Justification:** Investor presentation contains official positioning and investment case

### Example 8: "How did SWC get listed on AQUIS?" / "What was the IPO process?"
**Files:** `/Smarter Web/AdmissionDocument.txt` (1 file)
**Code:** No - direct reading
**Justification:** AdmissionDocument contains full details of AQSE listing, reverse takeover structure, shell company history, and IPO mechanics

---

## Cross-Reference Suggestions

- **RNS Bitcoin purchases** → Cross with CSV for quantitative validation → Cross with YouTube for CEO commentary
- **Share price movements** → Cross with RNS for catalysts → Cross with YouTube for sentiment
- **CEO statements** → Cross YouTube with tweets for consistency
- **Broker estimates** → Cross Tennyson with CSV for validation
- **Company announcements** → Cross tweets with RNS for formal confirmation

---

## Date-Based Selection Tips

- **IPO Date:** 2025-04-25 (use as reference point)
- **Recent data:** Focus on 2026-01, 2025-12, 2025-11 for "latest" queries
- **Key periods:**
  - IPO period: April-May 2025
  - Growth period: June-July 2025
  - Recent period: November 2025 - January 2026

---

*Always start here before selecting files. This index ensures efficient, targeted retrieval.*
