# SWC Knowledge Index

## Purpose
This index maps queries to relevant data sources and provides selection guidance for efficient progressive disclosure. Always consult this index before selecting files.

---

## Key Entities & Aliases

### People
- **Andrew Webley** (CEO): Andy, @asjwebley, asjwebley, Mr Webley, CEO, Andrew
- **Jesse Myers**: Croesus, @Croesus_BTC, Croesus_BTC, Jesse
- **@the_desert_ape**: the_desert_ape, desert ape (SWC employee)

### Companies
- **The Smarter Web Company**: SWC, Smarter Web, smarterwebuk, @smarterwebuk, The Smarter Web Company PLC
- **Stock Tickers:** LSE Main Market: SWC, OTCQB: TSWCF, FRA: 3M8 (ISIN: GB00BPJHZ015)
- **Tennyson Securities**: Tennyson, the broker, lead broker
- **Strand Hanson**: Strand Hanson, financial adviser
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
| Employee commentary (@the_desert_ape) | `/Tweets/the_desert_ape/` JSONs | RNS, YouTube | Optional - keyword search |
| Regulatory filings | RNS PDFs (filter by date/type) | - | No |
| Broker research | Tennyson PDFs | CSV (for validation) | Optional - cross-check |
| Strategy discussions | YouTube transcripts, CEO tweets | RNS (official statements) | No |
| Historical context | Legacy media, early RNS/YouTube | - | No |
| Predictive/projection queries | CSV (trends) + explicit statements (RNS/YouTube/Tweets) | - | Yes - trend analysis |
| Useful links, dashboards, communities | `knowledge/useful_links.md` | - | No |

---

## Data Source Details

### `/Smarter Web Data.csv` (Root)
**Purpose:** Core quantitative dataset
**Key Fields:** Date/Time, Share prices, BTC price (GBP), BTC balance, Bitcoin purchases, Share issuance, Market cap, mNAV, Sats per share, Cash, Yield metrics, Debt, Tennyson signals
**Time Range:** IPO (2025-04-25) onwards, hourly/daily granularity
**Triggers:** share price, BTC balance, Bitcoin holdings, mNAV, sats per share, market cap, volume, yield, how much Bitcoin, current price, historical data, trends, graph, plot, chart, calculate, projection, performance, returns, dilution, shares outstanding, cash position, debt, leverage, ATH, price history
**Selection Tips:**
- Use for any quantitative query
- Filter by date range for trend analysis
- Cross-reference with RNS for purchase dates
- Use code execution for filtering, aggregation, plots

### `/RNS/` (158 files)
**Purpose:** Official regulatory announcements
**Date Range:** Apr 2025 - Jun 2026
**Triggers:** RNS, regulatory, official announcement, Bitcoin purchase announcement, placing, fundraise, bookbuild, subscription, director appointment, TR1, major shareholder, trading update, AGM, general meeting, results, official filing, when did SWC buy Bitcoin, how much did they raise, new director
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

### `/Youtube/` (169 .txt files)
**Purpose:** Video transcripts with CEO insights and strategy discussions
**Date Range:** Apr 2025 - Jul 2026
**Triggers:** YouTube, video, interview, podcast, transcript, what did Andrew say, CEO commentary, strategy discussion, Bitcoin Treasuries World, BTW, Week In The World, mNAV update, investor call, presentation, panel, conference, True North Now, IG interview
**Key Series:**
- "A Week In The World Of SWC" (Episodes #3-22) - Weekly updates
- "Smarter Webley Wednesdays" - Regular CEO segments
- mNAV update videos - Quantitative updates
- Interviews and panel discussions
**Selection Tips:**
- Filenames start with date (YYYY-MM-DD)
- Filter by date range for time-specific queries
- Search titles for keywords (e.g., "mNAV", "Bitcoin", "strategy")
- Use for CEO perspective, qualitative insights, strategy discussions
- Cross-reference with CSV for quantitative validation

### `/Tweets/asjwebley/` (24 JSON files)
**Purpose:** CEO's direct communication and real-time commentary
**Date Range:** Jun 2024 - Jul 2026
**Format:** `posts-YYYY-MM.json`
**Statistics:** 1255 meaningful posts
**Triggers:** Andrew Webley, Andy, @asjwebley, CEO tweets, what did Andrew tweet, Andrew's view, CEO opinion, Webley said, think like Andy, Andrew's perspective, CEO social media
**Selection Tips:**
- Use monthly files for time-specific queries
- Load recent months (2026-01, 2025-12) for "latest" queries
- Use code execution for keyword filtering across multiple files
- Cross-reference with YouTube for consistency
- Use for personal views, real-time reactions, direct communication

### `/Tweets/smarterwebuk/` (17 JSON files)
**Purpose:** Official company announcements and updates
**Date Range:** Mar 2025 - Jul 2026
**Format:** `posts-YYYY-MM.json`
**Triggers:** @smarterwebuk, company tweets, official Twitter/X, SWC social media, company announcement tweet, what did SWC tweet, corporate social media
**Selection Tips:**
- Use for official company communication
- Cross-reference with RNS for formal announcements
- Use code execution for keyword/date filtering

### `/Tweets/Croesus_BTC/` (18 JSON files)
**Purpose:** Independent Bitcoin treasury company analysis
**Date Range:** Feb 2025 - Jul 2026
**Format:** `posts-YYYY-MM.json`
**Triggers:** Croesus, @Croesus_BTC, Jesse Myers tweets, Bitcoin treasury analysis, independent analysis, what did Croesus say, market commentary, think like Croesus
**Selection Tips:**
- Use for independent perspective on SWC
- Cross-reference with official sources for verification
- Use code execution for keyword filtering

### `/Tweets/the_desert_ape/` (15 JSON files)
**Purpose:** Jamie Knowles (Head of Capital Markets) tweets and investor relations commentary
**Date Range:** Apr 2025 - May 2026 (2,853 posts)
**Format:** `posts-YYYY-MM.json`
**Triggers:** the_desert_ape, desert ape, @the_desert_ape, Jamie Knowles, Jamie, Head of Capital Markets, what did Jamie say, what did the_desert_ape say
**Selection Tips:**
- Full history from IPO (Apr 2025) — extracted from lightbrd HTML snapshot
- Very active poster: 634 posts in Jul 2025, 728 in Jun 2025 — covers the entire capital raise period in detail
- Strong on investor relations: replies to shareholders, treasury strategy commentary, BTC purchase explanations
- Posting in personal capacity — cross-reference with RNS/asjwebley for anything material

### `/Tennyson/` (20 PDFs)
**Purpose:** Broker research and deal documentation
**Date Range:** May 2025 - October 2025
**Naming:** `DL_SWC_*.pdf` (Deal Letters), `RES_SWC_*.pdf` (Research Reports)
**Triggers:** Tennyson, broker research, broker note, deal letter, research report, analyst estimate, price target, broker analysis, yield estimate, Tennyson Securities, broker recommendation, investment research
**Selection Tips:**
- Use for broker analysis and yield estimates
- Cross-reference with CSV for validation
- Filter by date for time-specific research
- Use for investment analysis and projections

### `/Smarter Web/` (40 files — text + PDFs)
**Purpose:** Company documents, governance, investor materials, research, historical accounts
**Key Files & Triggers:**

**Investor Materials & Strategy**
| File | Use When Query Mentions |
|------|------------------------|
| `smarter-web-investor-presentation-May-2026.txt` | latest investor presentation, May 2026 deck, current pitch deck, investment thesis |
| `smarterweb-investor-presentation Digital. Capital. Designed._February 2026.txt` | Feb 2026 investor deck, Digital Capital Designed |
| `smarterweb-investor-presentation.txt` | older investor presentation, original pitch |
| `2025-07-16-P-BYD-Ratio.txt` | P/BYD, valuation, Jesse Myers, how to value Bitcoin companies, yield, mNAV methodology |

**Financial Reports**
| File | Use When Query Mentions |
|------|------------------------|
| `2026-02-20-SWC-Annual-Report.txt` | annual report, full year results, FY2025 (year to Oct 2025), annual accounts, yearly financials |
| `2025-07-25-interim-results.txt` | interim results, H1 2025, half year, financials, earnings, profit/loss, revenue, balance sheet |
| `Annual-Report-FY2022-PLC.txt` | 2022 accounts, FY2022, historical financials, pre-IPO performance, year ended Oct 2022 |
| `Annual-Report-FY2023-PLC.txt` | 2023 accounts, FY2023, historical financials, year ended Oct 2023 |
| `Annual-Report-FY2024-PLC.txt` | 2024 accounts, FY2024, historical financials, year ended Oct 2024 |
| `Operations-Accounts-FY2022.txt` | Operations Ltd accounts 2022, subsidiary financials, Dec 2022 year end |
| `Operations-Accounts-FY2023.txt` | Operations Ltd accounts 2023, subsidiary financials, Dec 2023 year end |
| `Operations-Accounts-FY2024.txt` | Operations Ltd accounts 2024, subsidiary financials, Dec 2024 year end |
| `16-01-2026-auditor-consent-letter.txt` | auditor, PKF Littlejohn, audit consent, prospectus supporting documents |

**Legal & Constitutional Documents**
| File | Use When Query Mentions |
|------|------------------------|
| `16-01-2026-swc-prospectus.txt` | prospectus, LSE uplisting, FCA, risk factors, Main Market, Bitcoin treasury risks, regulatory |
| `AdmissionDocument.txt` | AQUIS, AQSE, IPO, how went public, listing, reverse takeover, shell company, history, founding |
| `2026-03-20-articles-of-association.txt` | articles of association, current AoA, March 2026 AoA, company constitution (LATEST) |
| `2026-02-20-SWC-Proposed-New-Articles.txt` | proposed articles Feb 2026, AoA changes, AGM resolution |
| `2025-12-02-articles-of-association.txt` | articles Dec 2025, previous AoA |
| `2025-11-13-SWC-Proposed-New-Articles.txt` | proposed articles Nov 2025 |
| `articles-of-association-original-aquis-2025.txt` | original Aquis AoA, April 2025 articles, IPO constitution |

**General Meetings & Circulars**
| File | Use When Query Mentions |
|------|------------------------|
| `2026-02-23-notice-of-annual-general-meeting.txt` | AGM notice, annual general meeting 2026, notice of meeting, shareholder vote |
| `2026-01-12-SWC-Circular.txt` | January 2026 circular, general meeting Jan 2026 |
| `2025-11-13-SWC-Circular.txt` | November 2025 circular, general meeting Nov 2025 |

**Corporate Governance**
| File | Use When Query Mentions |
|------|------------------------|
| `Corporate governance _ A Market Leader...txt` | corporate governance, governance principles, board responsibilities, compliance, QCA Code |
| `corporate-governance/Terms-of-Reference-Nominations-Committee.txt` | nominations committee, board appointments, succession planning, Sean Wade committee |
| `corporate-governance/Terms-of-Reference-Remuneration-Committee.txt` | remuneration committee, executive pay, compensation, Randal Casson committee |
| `corporate-governance/Terms-of-Reference-Audit-and-Risk-Committee.txt` | audit committee, risk committee, financial oversight, PKF Littlejohn, Randal Casson |

**People & Company Profile**
| File | Use When Query Mentions |
|------|------------------------|
| `Directors & advisers _ Meet our board...txt` | board, directors, advisers, Tyler Evans, Sean Wade, Randal Casson, Martin Thomas, Andrew Webley, legal advisers, Strand Hanson, Hill Dickinson, PKF Littlejohn |
| `Who we are _ UK web design...txt` | company overview, team, employees, staff, Jesse Myers, Alex Wrench, Oliver Hewett, Mario Visconti, Laura Stanton-Hobbs, Jamie Knowles, Jon Bird, Nick Bird, Squarebird, what does SWC do, web design, company history |
| `Equity snapshot _ UK web design...txt` | shares outstanding, warrants, shareholders, dilution, ownership, 210k Capital, Smarter Convert, share count, director holdings (updated May 2026) |
| `Presentations, research & media _ The Smarter Web Company.txt` | media page, presentations list, research documents, YouTube links |

**Multi-File Selection Guide (triggers overlap):**
- **Andrew Webley queries** → Directors & advisers (bio) + Who we are (role) + interim-results (CEO statement)
- **Jesse Myers queries** → Who we are (role) + P-BYD-Ratio (his research)
- **Board/directors queries** → Directors & advisers (bios) + Who we are (overview) + Corporate governance (duties) + ToR files
- **Valuation queries** → P-BYD-Ratio (methodology) + investor-presentation May 2026 (thesis) + prospectus (metrics)
- **Company history queries** → AdmissionDocument (full) + Who we are (summary) + FY2022/23/24 annual reports
- **Risk queries** → prospectus (official risks) + Audit & Risk Committee ToR
- **Constitution/legal structure** → 2026-03-20-articles-of-association (current) is the authoritative version
- **Historical financials** → FY2022/23/24 PLC + Operations Ltd accounts for pre-IPO financial history
- **Squarebird/acquisition** → Who we are (team bios) + 2026-02-23 RNS

### `/Legacy media/` (13 files)
**Purpose:** Historical media coverage and external perspective
**Types:** News articles (.txt), TV appearances (.txt)
**Date Range:** Mar 2025 - Feb 2026
**Key Files & Triggers:**
| Subdirectory | Use When Query Mentions |
|--------------|------------------------|
| `/News articles/` (12 files) | news, press, media, Daily Mail, Blockspace, external perspective, MicroStrategy comparison, FTSE 100, JD Wetherspoon, public perception |
| `/Tv appearances/` (1 file) | CNBC, Squawk Box, TV interview, television appearance, Andrew Webley interview |

**Selection Tips:**
- Use for external/third-party perspective on SWC
- Use when asking "what did the press say" or "how was SWC covered"
- Cross-reference with official sources (RNS, prospectus) for accuracy

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

- **IPO Date (Aquis):** 2025-04-25
- **LSE Main Market admission:** 2026-02-03
- **FTSE All-Share / SmallCap inclusion:** 2026-03-23
- **Recent data:** Focus on 2026-04, 2026-05 for "latest" queries
- **Key periods:**
  - IPO period: April-May 2025
  - Capital raise & growth: June-August 2025
  - LSE uplisting: January-February 2026
  - FTSE inclusion: March 2026
  - Squarebird acquisition announced: 2026-02-23
  - Current (as of May 2026): BTC ~2,830, share price ~38p, mNAV ~0.98x

---

---

## Specialized Index Files (in `/knowledge/`)

These files provide additional guidance for specific query types:

| File | Use When | Triggers |
|------|----------|----------|
| **`useful_links.md`** | Need official site, dashboards, or community links | useful links, company website, SWC dashboard, DivBy21, BitcoinBee21, community, Discord, Telegram, X community, thesmarterdashboard, swc-dash |
| `rns_index.md` | Need to find specific RNS types | RNS categories, which RNS to use, RNS types |
| `youtube_index.md` | Need to find specific YouTube videos | video series, episode list, which YouTube to use |
| `example_bitcoin_purchases.md` | Bitcoin purchase timeline reference | purchase timeline, BTC acquisitions |
| `example_ceo_statements.md` | CEO statement patterns | CEO quotes, what Andrew said |
| `example_financial_metrics.md` | Financial metric guidance | which metrics, how to calculate |
| `example_timeline_events.md` | Key event timeline | timeline, key dates, milestones |

**Tip:** Use these specialized indexes when the main index points you to a large category (RNS, YouTube) and you need help narrowing down to specific files.

---

*Always start here before selecting files. This index ensures efficient, targeted retrieval.*
