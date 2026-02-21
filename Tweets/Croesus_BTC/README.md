# @Croesus_BTC X.com Posts - Extracted Data

## Overview

This directory contains structured data extracted from @Croesus_BTC's X.com timeline.

**Extracted:** January 27, 2026 at 01:18 PM; **updated** with missing tweets from lightbrd HTML snapshot; **updated** February 19, 2026 with Jan/Feb 2026 tweets from lightbrd HTML.
**Total Timeline Items:** 304+
**Meaningful Posts:** 430
**Filtered Out:** 16+

## Statistics

### By Post Type
- **original**: 261
- **quote**: 99
- **reply**: 70

### By Month
- **2026-02**: 59 posts
- **2026-01**: 113 posts
- **2025-12**: 1 posts
- **2025-11**: 11 posts
- **2025-10**: 19 posts
- **2025-09**: 8 posts
- **2025-08**: 13 posts
- **2025-07**: 49 posts
- **2025-06**: 14 posts
- **2025-05**: 27 posts
- **2025-04**: 45 posts
- **2025-03**: 69 posts
- **2025-02**: 2 posts

## Files

Monthly JSON files in format `posts-YYYY-MM.json`:
- `posts-2026-02.json` (59 posts)
- `posts-2026-01.json` (113 posts)
- `posts-2025-12.json` (1 posts)
- `posts-2025-11.json` (11 posts)
- `posts-2025-10.json` (19 posts)
- `posts-2025-09.json` (8 posts)
- `posts-2025-08.json` (13 posts)
- `posts-2025-07.json` (49 posts)
- `posts-2025-06.json` (14 posts)
- `posts-2025-05.json` (27 posts)
- `posts-2025-04.json` (45 posts)
- `posts-2025-03.json` (69 posts)
- `posts-2025-02.json` (2 posts)

## JSON Schema

Each post object contains:

```json
{
  "type": "original|reply|quote|repost_with_comment",
  "post_id": "2011173003997188386",
  "date_time": "Jan 13, 2026 · 8:26 PM UTC",
  "text": "Full text content by @Croesus_BTC",
  "is_reply": true/false,
  "is_thread_starter": true/false,
  "engagement": {
    "comments": 5,
    "reposts": 3,
    "likes": 45,
    "note": "These figures were correct as of January 27, 2026, 12:00 PM London time"
  },
  "media": [
    {"url": "https://...", "alt": "Alt text"}
  ],
  "permalink": "https://x.com/Croesus_BTC/status/2011173003997188386"
}
```

## Content Filtering

Posts were filtered to exclude:
- Empty or whitespace-only content
- Single emoji replies (🙏, etc.)
- Minimal text ("lol", "yes", "no", "thanks")
- Replies with <10 characters or <2 words
- Original posts with <3 words and <15 characters

## Extraction Method

- **Parser:** BeautifulSoup4 with lxml
- **Source elements:** `<div class="timeline-item" data-username="Croesus_BTC">`
- **Text extraction:** Excludes quoted content from quote tweets
- **Engagement data:** Snapshot from January 27, 2026; February 2026 data from February 19, 2026

## January 2026 update (lightbrd HTML)

Seven missing tweets were added to `posts-2026-01.json` from `Jesse Myers (Croesus 🔴) (@Croesus_BTC) _ lightbrd.html`:
- **2017248257714381094** (Jan 30) — Quote: Silver -18% since posting (follow-up to Silver video).
- **2016942069386822026** (Jan 29) — Original: Silver +283%, history says it will end poorly.
- **2016883864241582189** (Jan 29) — Original: Two outcomes — Saylor runs out of capital or Bitcoin bid to incredible heights.
- **2016537677911183385** (Jan 28) — Quote: SWC on track for LSE uplist; quoted @Toffeebdm.
- **2016520476919578927** (Jan 28) — Original: Strategy accumulation; 10% of all BTC?
- **2016237848953839718** (Jan 27) — Original: Gold vs dollar (dollar going down in value).
- **2016201868230177176** (Jan 27) — Original: The Bitcoin Standard / Silver rally (thread starter).

Media arrays were left empty (no media URLs added) per archive policy.

## February 2026 update (lightbrd HTML)

January 2026 updated with 76 additional tweets (37 → 113 posts) and February 2026 added (59 posts) from `Jesse Myers (@Croesus_BTC) _ lightbrd.html` snapshot taken February 19, 2026.

The lightbrd HTML contained significantly more tweets & replies than the original Nitter extraction. New January posts include silver analysis thread replies, Strategy accumulation debate, Bitcoin Standard discussion, and SWC/LSE commentary.

February 2026 (59 posts): LSE listing day celebration (572 likes), "Dumb enough to be bullish" (692 likes), Bitcoin 20M supply milestone (2,135 likes), Strategy unsustainability thread (2,542 likes), SWC Bitcoin Treasuries Unconference speakers, livestream with Andrew, bear market sentiment commentary.

## Usage

Load posts programmatically:

```python
import json
from pathlib import Path

# Load specific month
with open('posts-2026-01.json', 'r') as f:
    january_posts = json.load(f)

# Or load all posts
all_posts = []
for json_file in Path('.').glob('posts-*.json'):
    with open(json_file, 'r') as f:
        all_posts.extend(json.load(f))
```
