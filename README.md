<img width="1300" height="800" alt="bScreenshot_20260129_135215" src="https://github.com/user-attachments/assets/2ce5a260-2ebe-424b-a9b8-c883bf2b7c5b" />

> **A comprehensive dataset for analyzing the first UK-listed company with a Bitcoin treasury strategy**

[![Data](https://img.shields.io/badge/Data-313%20files-blue)](https://github.com/Jaakuice/SWC_Big_Brain_Ai)
[![YouTube](https://img.shields.io/badge/YouTube-96%20transcripts-red)](https://github.com/Jaakuice/SWC_Big_Brain_Ai)
[![Tweets](https://img.shields.io/badge/Tweets-1,472%20posts-1DA1F2)](https://github.com/Jaakuice/SWC_Big_Brain_Ai)

---

## 📑 Table of Contents

- [Description](#description)
- [Data Overview](#data-overview)
- [Example Queries](#example-queries)
- [Setup for AI Analysis](#setup-for-ai-analysis)
  - [Complete Beginner's Guide](#-new-to-ai-assistants-or-coding)
- [Data Quality and Sources](#data-quality-and-sources)
- [Disclaimer](#disclaimer)
- [Contributing](#contributing)
- [Project Structure](#project-structure)
- [About the Creator](#about-the-creator)
- [Acknowledgments](#acknowledgments)

---

## Description

This repository contains a comprehensive, structured dataset for analyzing **The Smarter Web Company (SWC)**, a UK-based web design company that adopted a Bitcoin treasury strategy and went public on the Aquis Stock Exchange in April 2025. SWC represents a unique case study as the first UK-listed company to go public with Bitcoin on its balance sheet, making it an ideal subject for financial analysis, strategy evaluation, and Bitcoin treasury research.

### What Makes This Dataset Valuable

- **First-of-its-kind:** First UK-listed company with Bitcoin treasury strategy
- **Comprehensive coverage:** 96+ YouTube transcripts, 113 regulatory filings, financial time-series data, and social media archives
- **Multi-source analysis:** Combines official regulatory data (RNS), quantitative metrics (CSV), CEO commentary (tweets/YouTube), and independent analysis
- **Time-series depth:** Data spans from pre-IPO (March 2025) through February 2026, capturing the complete journey from IPO to growth
- **AI-ready:** Optimized for use with AI tools like Claude Projects, enabling progressive disclosure and intelligent querying

### Analysis Capabilities

This dataset enables deep analysis across multiple dimensions:

- **Financial Trends:** Track share price movements, mNAV (modified Net Asset Value), sats per share, yield metrics, and Bitcoin accumulation
- **Strategy Evolution:** Analyze how SWC's Bitcoin treasury strategy developed through CEO statements, regulatory filings, and market commentary
- **Sentiment Analysis:** Examine CEO and company communication patterns, market reactions, and community engagement
- **Cross-verification:** Compare official announcements (RNS) with quantitative data (CSV) and qualitative commentary (YouTube/Tweets)
- **Predictive Modeling:** Use historical trends and explicit forward-looking statements for projections and scenario analysis

---

## 📊 Data Overview

| Category | Count | Description | Date Range |
|----------|-------|-------------|------------|
| **YouTube Transcripts** | 96 | Video content (~40-45 hours) | Apr 2025 - Feb 2026 |
| **CEO Tweets** | 894 | @asjwebley curated posts | Jun 2024 - Feb 2026 |
| **Company Tweets** | 148 | @smarterwebuk curated posts | Mar 2025 - Feb 2026 |
| **HoBS Tweets** | 430 | @Croesus_BTC curated posts | Feb 2025 - Feb 2026 |
| **RNS Filings** | 113 | Regulatory filings | Apr 2025 - Feb 2026 |
| **Research Reports** | 20 | Tennyson broker analysis | May 2025 - Oct 2025 |
| **Financial Data** | 1 | CSV time-series (hourly/daily) | Apr 2025+ |
| **Company Docs** | 11 | Prospectus, admission docs, annual report | Various |
| **Media Articles** | 13 | News coverage, TV appearances | Mar 2025 - Feb 2026 |
| **TOTAL** | **~313 files** | | |

---

## 💡 Example Queries

This dataset is ideal for use with AI tools like **Claude Projects** (progressive disclosure setups). Here are example prompts you could ask an AI with this knowledge base uploaded:

### 1. "What is the current sats per share and how has it changed since IPO?"

<details>
<summary>Click to view example response</summary>

Based on the financial data in the CSV file, here's how SWC's sats per share has evolved since IPO:                                                           
                                                                                                                                                               
  Current Status:                                                                                                                                               
  The current sats per share stands at 677 sats as of January 30, 2026. This represents a remarkable increase from the IPO level of just 1 sat per share on April 25, 2025.    
  
  Change Since IPO:                                                                                                                                             
  - Absolute increase: +676 sats per share                                                                                                                      
  - Percentage increase: +71,413%                                                                                                                               
  - Time period: 280 days                                                                                                                                       
                                                                                                                                                             
  Key Drivers:                                                                                                                                                  
  The dramatic increase in sats per share reflects SWC's aggressive Bitcoin treasury strategy execution:                                                        
                                                                                                                                                   
  1. Bitcoin Accumulation: The company has grown its Bitcoin holdings from 2.30 BTC at IPO to 2,674 BTC currently—a 1,162x increase in absolute Bitcoin holdings.
  2. Share Dilution Impact: While total shares outstanding increased from 146.9 million to 350.2 million (138% dilution), the Bitcoin accumulation significantly outpaced this dilution, resulting in the strong sats per share growth.                                                                                       
  3. Capital Deployment: The company has used capital raises (reflected in the share issuance) to aggressively acquire Bitcoin, with the Bitcoin accumulation rate far exceeding the share dilution rate. 
                                                                                                                                                           
  [Data source: knowledge/Smarter Web Data.csv - rows for 2025-04-25 (IPO) and 2026-01-30 (latest)]  

> ⚠️ This analysis is based on publicly available data and should not be considered financial advice. Past performance is not indicative of future results.

</details>

### 2. "Summarize Andrew Webley's view on Bitcoin treasury risks from his latest YouTube appearances."

<details>
<summary>Click to view example response</summary>

**Summary: Andrew Webley's Views on Bitcoin Treasury Risks**

From recent YouTube appearances (November 2025–January 2026), Andrew Webley's views on Bitcoin treasury risks:

1. **Risk of Selling Bitcoin**  
   Webley emphasizes: *"The worst thing you can do as an individual or as a public company is to sell your Bitcoin."* He would only consider selling if the company traded at a significant MNAV discount for an extended period, and even then would resist.

2. **Cash Buffer and Operating Costs**  
   He notes that insufficient cash can force selling Bitcoin. He aims to maintain a cash buffer to cover operating costs without selling Bitcoin, while balancing against cash devaluation.

3. **Debt and Leverage Risks**  
   Webley is cautious about traditional debt. He prefers Bitcoin-denominated debt (like Smarter Convert) because it aligns interests and avoids margin calls.

4. **Custody and Security Risks**  
   He opposes self-custody for a Bitcoin treasury company: *"The risk to the people that work at the company is just not acceptable."* He emphasizes using professional custodians with strong security.

5. **Volatility and Sentiment Risks**  
   He acknowledges volatility as inherent and views it as a wave pattern tied to Bitcoin sentiment and the company's ability to raise capital.

6. **Convertible Debt Risks**  
   He avoids traditional convertible debt, calling it *"far too one-sided for the convertible holders"* and harmful to shareholders.

7. **Market Structure Risks**  
   He notes that "paper Bitcoin" (derivatives/options) can create issues as Bitcoin becomes more established.

8. **Execution and Governance Risks**  
   He emphasizes strong governance, experienced directors, and avoiding unnecessary risks.

**Overall Risk Philosophy:** Webley's approach prioritizes long-term sustainability over short-term gains, focusing on building a resilient structure that can withstand volatility.

**Sources:** `2026-01-19_Bitcoin Treasuries World #56.txt`, `2026-01-14_A Week In The World Of SWC Episode #21.txt`, `2025-12-03_Bitcoin Treasuries World #54.txt`, `2025-11-28_THE SMARTER WEB COMPANY_ GETTING STRONGER THROUGH VOLATILITY.txt`

> ⚠️ This analysis is based on publicly available data and should not be considered financial advice. Past performance is not indicative of future results.

</details>

### 3. "Think like Andy Webley: write a tweet explaining the latest Bitcoin purchase of 1337."

<details>
<summary>Click to view example response</summary>

**Tweet in Andrew Webley's voice:**

> RNS released: The Smarter Web Company has purchased 1,337 Bitcoin as part of our ongoing Bitcoin treasury strategy under "The 10 Year Plan."
> 
> This purchase brings our total holdings to 4,001 Bitcoin, strengthening our position as the UK's largest publicly traded Bitcoin treasury company. At current prices, this represents a significant deployment of capital to continue building Bitcoin per share for our shareholders.
> 
> We remain focused on disciplined capital allocation and executing our strategy to grow our treasury position. Every Bitcoin we add compounds over time, and we believe this purchase further positions us well for the future.
> 
> The Smarter Web Company (AQUIS: #SWC | OTCQB: $TSWCF | FRA: $3M8)

**Note:** Written in Andrew Webley's authentic voice based on his actual tweet style from `posts-2025-08.json`, `posts-2025-11.json`, and other examples.

> ⚠️ This analysis is based on publicly available data and should not be considered financial advice.

</details>

### 4. "Project potential mNAV in 2027 if Bitcoin reaches $200,000, based only on historical trends and explicit statements."

<details>
<summary>Click to view example response</summary>

**Projected mNAV in 2027 if Bitcoin Reaches $200,000**

**Current State (January 22, 2026):**
- BTC Balance: 2,664 BTC
- Shares Outstanding: 297,980,144
- BTC Per Share: 0.00000894 BTC/share
- Current BTC Price: £65,897
- Current mNAV: 0.84

**Projection Scenarios:**

| Scenario | BTC Growth | Shares Growth | Projected BTC | Projected Shares | Projected mNAV |
|----------|------------|---------------|---------------|------------------|----------------|
| **Conservative** | 30%/year | 25%/year | 3,408 BTC | 367,446,279 | **1.47** |
| **Moderate** | 50%/year | 35%/year | 3,899 BTC | 394,985,842 | **1.56** |
| **Aggressive** | 75%/year | 50%/year | 4,506 BTC | 436,065,373 | **1.64** |

**Explicit Forward-Looking Statements:**
- *"2025 was a year focused on laying strong foundations, and in 2026 we intend to build decisively upon them."*
- *"Our long-term objective of growing Bitcoin per share."*
- Reference to "The 10 Year Plan" as the ongoing Bitcoin treasury strategy

**Conclusion:** Based on historical trends and explicit statements, if Bitcoin reaches $200,000 by 2027, projected mNAV ranges from **1.47 to 1.64**, with a moderate scenario estimate of **1.56**.

**Sources:** `Smarter Web Data.csv` (historical trends), `posts-2026-01.json` (explicit forward-looking statements), YouTube transcripts (strategy discussions)

> ⚠️ **Important:** These projections are speculative and based on assumptions that may not materialize. Past performance does not guarantee future results. This analysis is based on publicly available data and should not be considered financial advice.

</details>

### 5. "Create a timeline graph of all Bitcoin purchases announced by SWC. Save as a .png"

<details>
<summary>Click to view example response</summary>

**Timeline Graph Created:** `swc_bitcoin_purchases_timeline.png`

**Graph Summary:**

The visualization includes:

**Top Panel:**
- Bar chart showing BTC purchased per transaction (26 purchases from April 2025 to November 2025)
- Red line showing cumulative Bitcoin balance over time
- Annotations marking key milestones:
  - First Purchase (3.44 BTC on April 30, 2025)
  - Largest Purchase (74.27 BTC on June 13, 2025)
  - Major Purchase (295 BTC on August 5, 2025)
  - Latest Purchase (4.00 BTC on November 4, 2025)

**Bottom Panel:**
- Bar chart showing purchase cost in £M for each transaction

**Summary Statistics Box:**
- Total Purchases: 26
- Total BTC Acquired: 2,661.70 BTC
- Total Cost: £220.6M
- Average Price: £82,857/BTC

<img width="4175" height="2985" alt="swc_bitcoin_purchases_timeline" src="https://github.com/user-attachments/assets/96f47f93-3dfe-41e5-ad6e-2516e1e5856a" />

The graph is saved at 300 DPI resolution (4175 x 2985 pixels) and shows the progression of SWC's Bitcoin accumulation strategy from IPO through November 2025.

**Source:** `Smarter Web Data.csv` - All Bitcoin purchase events where New BTC > 0

> ⚠️ This analysis is based on publicly available data and should not be considered financial advice. Past performance is not indicative of future results.

</details>

### 6. "What are the key risk factors in SWC's latest prospectus?"

<details>
<summary>Click to view example response</summary>

**Key Risk Factors from SWC's Prospectus (16 January 2026)**

**Business Risks**

1. **Competition** — Faces larger, better-resourced competitors in web design; increasingly competing with firms using AI tools without having their own bespoke AI solution.
2. **Key man risk** — Heavily dependent on Andrew Webley (CEO/founder) who has key client relationships.
3. **Technology/platform risk** — Reliance on proprietary CMS; any technical failure could disrupt business and damage reputation.
4. **DIY website builders** — Platforms like Wix, Squarespace, and WordPress are eroding demand for professional web design services.
5. **Short-term contracts** — No client contracts exceed 12 months with one-month termination notice.

**Bitcoin Treasury Risks (Major Focus)**

6. **Bitcoin volatility** — Holdings of 2,664 Bitcoin (avg. purchase price £82,858) exposed to significant price swings. As of 9 Jan 2026, Bitcoin had lost ~25% in 3 months with £40.3m unrealised loss.
7. **Custodian risk** — Bitcoin held by third-party custodians (Fidelity, Coinbase, Kraken); insolvency could result in loss or inaccessibility. Bankruptcy law is undeveloped for digital assets.
8. **Unproven treasury strategy** — Bitcoin as corporate treasury reserve remains largely untested across economic cycles.
9. **Concentration risk** — Significant assets concentrated in a single volatile asset class.
10. **Liquidity risk** — Market stress or technical issues could prevent converting Bitcoin to fiat when needed.
11. **Currency exposure** — Bitcoin traded in USD but costs/reporting in GBP; no hedging in place.
12. **51% attack risk** — Potential for malicious actors to manipulate Bitcoin network.
13. **Stakeholder perception** — Some partners/financiers may refuse to deal with the Group due to Bitcoin exposure.

**Regulatory & Legal Risks**

14. **Regulatory reclassification** — Risk of being classified as an alternative investment fund requiring FCA authorisation.
15. **Reverse takeover rules** — Bitcoin purchases could trigger reverse takeover thresholds, causing delisting.
16. **Accounting treatment divergence** — Different treatment of Bitcoin under IFRS vs US GAAP creates comparison difficulties.
17. **US litigation exposure** — OTCQB listing exposes company to US securities class actions.
18. **AML risks** — Potential for purchased Bitcoin to have criminal origins.

**Share-Specific Risks**

19. **Significant dilution** — 105.7m warrants plus convertible notes could dilute shareholders by ~24%; 1.65bn shares remain in non-pre-emptive headroom.
20. **No dividends** — No intention to pay dividends in the foreseeable future.

**Source:** `Smarter Web/16-01-2026-swc-prospectus.pdf`

> ⚠️ This analysis is based on publicly available data and should not be considered financial advice. Past performance is not indicative of future results.

</details>

---

### Setup for AI Analysis

> **👋 New to AI assistants or coding?** Check out our **[Complete Beginner's Guide](BEGINNER_GUIDE.md)** - it walks you through everything step-by-step, from download to asking your first question. No technical knowledge required!

#### Quick Start

### 1. Clone or Download the Repository
```bash
git clone https://github.com/Jaakuice/SWC_Big_Brain_Ai
cd SWC_Big_Brain_Ai
```

Or download and extract the repository to your workspace.

### 2. Open in Your IDE

#### Cursor IDE
1. Open Cursor IDE
2. File → Open Folder → Select the `SWC_Big_Brain_Ai` directory
3. The AI assistant will automatically have access to all files in the workspace
4. Insert `Start.md` in to the prompt and enter

#### Claude Code
1. Open Claude Code
2. Open the `SWC_Big_Brain_Ai` folder as your workspace
3. Files are now accessible for AI queries and code execution
4. Insert `Start.md` in to the prompt and enter

#### Codex
1. Open Codex
2. File → Open Folder (or equivalent) → Select the `SWC_Big_Brain_Ai` directory
3. The AI will have access to the workspace for queries and code execution
4. Insert `Start.md` in to the prompt and enter

#### Other IDEs
1. Open your IDE
2. Open the `SWC_Big_Brain_Ai` folder as your workspace
3. Files are now accessible for AI queries and code execution
4. Insert `Start.md` in to the prompt and enter

---

## 📋 Data Quality and Sources

### Reliability Hierarchy
1. **RNSs:** Official regulatory documents (highest reliability)
2. **CSV Data:** Manually compiled/scraped quantitative data (verify sources)
3. **YouTube Transcripts:** Extracted/transcribed (may contain errors)
4. **Tweet Data:** Extracted from X.com (engagement metrics are snapshots)

### Data Collection Notes
- All data is publicly sourced
- No private or confidential information included
- Tweet engagement metrics reflect snapshots from extraction date
- YouTube transcripts may contain transcription errors
- CSV data should be validated against official RNS filings

---

## ⚠️ Disclaimer

> **This dataset is for research and educational purposes only.**

- ✅ All data is publicly available information
- ✅ No private or confidential information is included
- ❌ **This is not financial advice**
- ❌ Past performance is not indicative of future results
- ❌ Any analysis or projections are speculative and should not be used for investment decisions
- ✅ Always verify data against official sources (RNS filings, company announcements)

---

## 🤝 Contributing

Contributions are welcome! This dataset can be enhanced with:

- 📹 **Additional data sources:** More transcripts, news articles, or analysis
- ✅ **Data validation:** Cross-checking CSV data against official sources. Reading and fixing transcript errors.
- 🔄 **Updates:** Keeping the dataset current with new RNS filings, tweets, and videos

### How to Contribute
- Message me with links to missing YouTube videos, news articles, or analysis.

---

## 📁 Project Structure

```
SWC-Ai/
├── README.md                    # This file
├── FILE_STRUCTURE.md            # Detailed file structure documentation
├── Start.md                    # System prompt for Claude Projects
├── knowledge/                   # Knowledge management files (10 files)
│   ├── index.md                 # Main knowledge index
│   ├── rns_index.md             # RNS document index
│   ├── youtube_index.md         # YouTube transcript index
│   ├── useful_links.md          # External links and resources
│   ├── share_count_timeline.md  # Share dilution timeline
│   ├── example_bitcoin_purchases.md    # Reference examples
│   ├── example_ceo_statements.md       # Reference examples
│   ├── example_financial_metrics.md    # Reference examples
│   ├── example_timeline_events.md      # Reference examples
│   └── Smarter Web Data.csv     # Core financial time-series data
├── RNS/                         # Regulatory News Service filings (113 files)
├── Youtube/                     # YouTube transcripts (96 TXT files)
├── Tweets/                      # Social media archives
│   ├── asjwebley/               # CEO tweets (894 posts)
│   ├── smarterwebuk/            # Company tweets (148 posts)
│   └── Croesus_BTC/             # Analyst tweets (430 posts)
├── Tennyson/                    # Broker research (20 PDFs)
├── Smarter Web/                 # Company documents (11 files)
└── Legacy media/                # Historical coverage (13 TXT files)
```

---

## 👤 About the Creator

This dataset was gathered and is maintained by **[@DivBy21](https://x.com/DivBy21)**.

The repository represents:
- Data collection and extraction from multiple sources
- Transcript processing and organization
- Building structured knowledge management systems
- Creating AI-optimized documentation and indexing

This project aims to provide the most comprehensive publicly available dataset on the Bitcoin treasury company The Smarter Web Company.

**Connect:**
- Twitter/X: [@DivBy21](https://x.com/DivBy21)
- GitHub: This repository

---

## 🙏 Acknowledgments

- All data sources are publicly available
- Transcripts and data extraction performed for research purposes
- Special thanks to the SWC and SWC community for being great guys and gals

---

**Last Updated:** February 2026

> This repository provides a comprehensive knowledge base for analyzing The Smarter Web Company's unique journey as the first UK-listed company with a Bitcoin treasury strategy.
