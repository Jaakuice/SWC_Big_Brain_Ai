# SWC-Ai Project File Structure

## Overview
This repository contains comprehensive data and documentation related to The Smarter Web Company (SWC), a UK-based web design company that adopted a Bitcoin treasury strategy and went public in April 2025.

---

## Directory Structure

### `/home/sam/Documents/SWC-Ai/`

#### **Root Level Files**

**`Start.md`**
- **Type:** Markdown documentation
- **Content:** System prompt for AI assistants (Claude Projects, Cursor IDE, etc.)
- **Purpose:** Provides structured guidance for querying the knowledge base

**`README.md`**
- **Type:** Markdown documentation
- **Content:** Repository overview, setup instructions, example queries
- **Purpose:** Main documentation and introduction to the dataset

**`FILE_STRUCTURE.md`**
- **Type:** Markdown documentation
- **Content:** Detailed file structure documentation (this file)
- **Purpose:** Comprehensive guide to repository organization

---

### **`/knowledge/`** (10 files: 9 MD + 1 CSV)
Contains knowledge management files for organizing and navigating the dataset.

#### **Index and Navigation Files**

**`index.md`**
- **Type:** Markdown documentation
- **Content:** Main knowledge index mapping query types to relevant file categories
- **Purpose:** Primary navigation guide for determining which files to consult for different query types

**`rns_index.md`**
- **Type:** Markdown documentation
- **Content:** Detailed categorization of RNS filings by type, date, and topic
- **Purpose:** Helps narrow down which RNS PDFs are relevant for specific queries

**`youtube_index.md`**
- **Type:** Markdown documentation
- **Content:** Breakdown of video series, episodes, and topic guide
- **Purpose:** Navigate YouTube transcripts by series, date, or topic

#### **Reference and Timeline Files**

**`useful_links.md`**
- **Type:** Markdown documentation
- **Content:** External links and resources related to SWC
- **Purpose:** Provides URLs to official company resources, exchanges, and external tools

**`share_count_timeline.md`**
- **Type:** Markdown documentation
- **Content:** Timeline of share issuances and dilution events
- **Purpose:** Track capital raises, fundraising history, and dilution over time

#### **Example Reference Files**

**`example_bitcoin_purchases.md`**
- **Type:** Markdown documentation
- **Content:** Reference examples for Bitcoin purchase queries
- **Purpose:** Template patterns for common Bitcoin purchase questions

**`example_ceo_statements.md`**
- **Type:** Markdown documentation
- **Content:** Reference examples for CEO statement queries
- **Purpose:** Template patterns for finding CEO commentary

**`example_financial_metrics.md`**
- **Type:** Markdown documentation
- **Content:** Reference examples for financial metric queries
- **Purpose:** Template patterns for quantitative analysis questions

**`example_timeline_events.md`**
- **Type:** Markdown documentation
- **Content:** Reference examples for timeline and event queries
- **Purpose:** Template patterns for chronological questions

#### **Financial Data File**

**`Smarter Web Data.csv`**
- **Type:** CSV data file
- **Content:** Historical time-series data tracking SWC's financial metrics
- **Key Fields:** Date/Time, Share prices (Open/Close/High/Low), Volume, BTC price (GBP), BTC balance, Bitcoin purchases, Share issuance, Market cap, mNAV (modified Net Asset Value), Sats per share, Cash, Yield metrics, Tennyson trading signals
- **Time Range:** From IPO date (2025-04-25) onwards with hourly/daily granularity
- **Purpose:** Core dataset for analyzing SWC's performance, Bitcoin accumulation, and share price movements
- **Note:** Previously located at root level, moved to knowledge/ directory for better organization

---

### **`/Legacy media/`**
Contains historical media coverage and appearances related to SWC.

#### **`/Legacy media/News articles/`** (9 files)
- **Type:** Text files (.txt)
- **Content:** News articles from various publications covering SWC's IPO, Bitcoin strategy, and growth
- **Sources:** Blockspace Media, Daily Mail Online, and other financial news outlets
- **Date Range:** March 2025 - September 2025
- **Topics:** IPO announcement, Bitcoin treasury strategy, share price performance, comparisons to MicroStrategy, FTSE 100 aspirations

#### **`/Legacy media/Tv appearances/`** (1 file)
- **Type:** Text file (.txt)
- **Content:** Transcript from CNBC Squawk Box Europe appearance
- **Date:** July 3, 2025
- **Format:** Interview transcript

---

### **`/RNS/`** (106 files)
- **Type:** PDF documents
- **Content:** Regulatory News Service (RNS) announcements - official company filings and disclosures required by UK stock exchange regulations
- **Date Range:** April 2025 - January 2026
- **Key Document Types:**
  - IPO and admission documents
  - Bitcoin purchase announcements
  - Share issuance and fundraising (accelerated bookbuilds, subscriptions, placings)
  - Director appointments and changes
  - Corporate governance updates
  - Trading updates and TR1 notifications (significant shareholdings)
  - Interim results and financial statements
  - Corporate adviser changes
  - Prospectus documents
  - General meeting notices and results
- **Purpose:** Official regulatory record of all material company events and disclosures

---

### **`/Smarter Web/`**
Contains company-specific documents, presentations, and corporate information.

**Files:**
- **`16-01-2026-swc-prospectus.txt`** - FCA-approved prospectus for LSE Main Market uplisting, risk factors, official disclosures
- **`AdmissionDocument.txt`** - Original AQUIS/AQSE IPO admission document, reverse takeover details, shell company history
- **`smarterweb-investor-presentation.txt`** - Official investor presentation deck, investment thesis
- **`2025-07-16-P-BYD-Ratio.txt`** - Jesse Myers research on P/BYD (Price-to-Bitcoin-Yield-Dilution) valuation methodology
- **`2025-07-25-interim-results.txt`** - H1 2025 interim financial statements, CEO statement, balance sheet
- **`Corporate governance...txt`** - QCA Code compliance, 10 governance principles
- **`Directors & advisers...txt`** - Board of directors bios (Andrew Webley, Albert Soleiman, Sean Wade, Randal Casson, Martin Thomas, Tyler Evans), advisers list
- **`Equity snapshot...txt`** - Shares outstanding, warrants, major shareholders (210k Capital, Webley family), Smarter Convert
- **`Who we are...txt`** - Company overview, team members (Jesse Myers, Alex Wrench, Laura Stanton-Hobbs, Mario Visconti)

---

### **`/Tennyson/`** (20 files)
- **Type:** PDF documents
- **Content:** Research reports and deal letters from Tennyson Securities (corporate adviser/broker)
- **File Naming Convention:**
  - `DL_SWC_*.pdf` - Deal Letters (dates in DDMMYY format)
  - `RES_SWC_*.pdf` - Research Reports (dates in DDMMYY format)
- **Date Range:** May 2025 - October 2025
- **Purpose:** Broker research, deal documentation, and investment analysis

---

### **`/Tweets/`**
Contains structured social media data extracted from X.com (Twitter) accounts related to SWC.

#### **`/Tweets/asjwebley/`** (19 files: 18 JSON + 1 README)
- **Account:** @asjwebley (Andrew Webley, CEO of SWC)
- **Content:** Monthly JSON files containing structured post data
- **Date Range:** June 2024 - January 2026
- **File Format:** `posts-YYYY-MM.json`
- **Data Includes:** Post type (original/reply/quote/repost), text content, engagement metrics (likes, reposts, comments), timestamps, media attachments, permalinks
- **Statistics:** 865 meaningful posts from 1,330 total timeline items
- **README.md:** Contains extraction metadata, statistics, JSON schema documentation, and usage examples

#### **`/Tweets/Croesus_BTC/`** (13 files: 12 JSON + 1 README)
- **Account:** @Croesus_BTC
- **Content:** Monthly JSON files with structured post data
- **Date Range:** February 2025 - January 2026
- **File Format:** `posts-YYYY-MM.json`
- **Statistics:** 295 meaningful posts
- **Purpose:** Bitcoin treasury company analysis and commentary account

#### **`/Tweets/smarterwebuk/`** (12 files: 11 JSON + 1 README)
- **Account:** @smarterwebuk (Official SWC company account)
- **Content:** Monthly JSON files with structured post data
- **Date Range:** March 2025 - January 2026
- **File Format:** `posts-YYYY-MM.json`
- **Statistics:** 136 meaningful posts
- **Purpose:** Official company announcements and updates

---

### **`/Youtube/`** (90 files)
- **Type:** Text files (.txt)
- **Content:** Transcripts and summaries of YouTube videos featuring SWC, Andrew Webley, or related Bitcoin treasury content
- **Date Range:** April 2025 - January 2026
- **Video Types:**
  - "A Week In The World Of SWC" weekly series (Episodes #3-21)
  - "Smarter Webley Wednesdays" regular segments on Bitcoin Treasuries World
  - Interviews with Andrew Webley on various channels
  - Bitcoin treasury analysis videos
  - mNAV (modified Net Asset Value) update videos
  - Investor presentations and livestreams
  - Conference appearances and panel discussions
- **Key Channels/Shows:**
  - Bitcoin Treasuries World
  - True North Now
  - IG Interviews
  - Various crypto/bitcoin YouTube channels
- **File Naming:** `YYYY-MM-DD_Video Title.txt`
- **Content Format:** Includes video metadata (date, video ID, URL, duration, channel, host, guest), key topics summary, and full transcript

---

## Data Relationships

### Timeline Coverage
- **IPO Date:** April 25, 2025
- **Data Collection:** Comprehensive coverage from pre-IPO (March 2025) through January 2026
- **Update Frequency:**
  - RNS: Real-time regulatory filings
  - YouTube: Regular weekly/bi-weekly content
  - Tweets: Continuous social media activity
  - CSV Data: Hourly/daily financial metrics

### Cross-Reference Opportunities
- **RNS announcements** can be cross-referenced with **YouTube transcripts** for CEO commentary
- **Tweet data** provides real-time reactions and updates between formal announcements
- **CSV data** tracks quantitative metrics that correlate with **RNS filings** (Bitcoin purchases, share issuances)
- **News articles** provide external perspective on events documented in **RNS filings**

---

## File Count Summary

| Directory | File Count | File Types |
|-----------|------------|------------|
| Root | 3 | MD |
| knowledge | 10 | MD, CSV |
| Legacy media/News articles | 9 | TXT |
| Legacy media/Tv appearances | 1 | TXT |
| RNS | 106 | PDF |
| Smarter Web | 9 | TXT |
| Tennyson | 20 | PDF |
| Tweets/asjwebley | 19 | JSON, MD |
| Tweets/Croesus_BTC | 13 | JSON, MD |
| Tweets/smarterwebuk | 12 | JSON, MD |
| Youtube | 90 | TXT |
| **TOTAL** | **~294 files** | |

---

## Usage Notes

### For Analysis
- Use `knowledge/Smarter Web Data.csv` as the primary quantitative dataset
- Consult `knowledge/index.md` to map query types to relevant file categories
- Cross-reference RNS PDFs for official announcements
- YouTube transcripts provide qualitative context and CEO insights
- Tweet data offers real-time sentiment and engagement metrics

### For Research
- Start with RNS filings for official company statements
- Review YouTube transcripts for detailed explanations and strategy discussions
- Check news articles for external media coverage and market perception
- Analyze tweet patterns for communication strategy and community engagement

### Data Quality
- RNS files are official regulatory documents (highest reliability)
- CSV data appears to be manually compiled or scraped (verify sources)
- YouTube transcripts are extracted/transcribed (may contain errors)
- Tweet data is extracted from X.com (engagement metrics are snapshots)

---

*Last Updated: January 2026*
*Project Focus: The Smarter Web Company (SWC) - UK Bitcoin Treasury Company Analysis*
