# @asjwebley X.com Posts - Extracted Data

## Overview

This directory contains structured data extracted from @asjwebley's X.com timeline.

**Source:** `@asjwebley_X.html` (saved Nitter frontend page); `Andrew Webley (@asjwebley) _ lightbrd.html` (lightbrd snapshot).
**Extracted:** January 27, 2026 at 12:05 PM; **updated** January 30, 2026 with missing tweets from lightbrd HTML; **updated** February 19, 2026 with Jan/Feb 2026 tweets from lightbrd HTML.
**Total Timeline Items:** 1330+
**Meaningful Posts:** 894
**Filtered Out:** 469+

## Statistics

### By Post Type
- **original**: 239
- **quote**: 101
- **reply**: 536
- **repost_with_comment**: 18

### By Month
- **2026-02**: 26 posts
- **2026-01**: 43 posts
- **2025-12**: 46 posts
- **2025-11**: 56 posts
- **2025-10**: 55 posts
- **2025-09**: 39 posts
- **2025-08**: 51 posts
- **2025-07**: 76 posts
- **2025-06**: 118 posts
- **2025-05**: 190 posts
- **2025-04**: 182 posts
- **2025-03**: 2 posts
- **2025-02**: 2 posts
- **2024-12**: 2 posts
- **2024-11**: 1 posts
- **2024-10**: 1 posts
- **2024-09**: 1 posts
- **2024-08**: 2 posts
- **2024-06**: 1 posts

## Files

Monthly JSON files in format `posts-YYYY-MM.json`:
- `posts-2026-02.json` (26 posts)
- `posts-2026-01.json` (43 posts)
- `posts-2025-12.json` (46 posts)
- `posts-2025-11.json` (56 posts)
- `posts-2025-10.json` (55 posts)
- `posts-2025-09.json` (39 posts)
- `posts-2025-08.json` (51 posts)
- `posts-2025-07.json` (76 posts)
- `posts-2025-06.json` (118 posts)
- `posts-2025-05.json` (190 posts)
- `posts-2025-04.json` (182 posts)
- `posts-2025-03.json` (2 posts)
- `posts-2025-02.json` (2 posts)
- `posts-2024-12.json` (2 posts)
- `posts-2024-11.json` (1 posts)
- `posts-2024-10.json` (1 posts)
- `posts-2024-09.json` (1 posts)
- `posts-2024-08.json` (2 posts)
- `posts-2024-06.json` (1 posts)

## JSON Schema

Each post object contains:

```json
{
  "type": "original|reply|quote|repost_with_comment",
  "post_id": "2011173003997188386",
  "date_time": "Jan 13, 2026 · 8:26 PM UTC",
  "text": "Full text content by @asjwebley",
  "is_reply": true/false,
  "is_thread_starter": true/false,
  "engagement": {
    "comments": 5,
    "reposts": 3,
    "likes": 45,
    "note": "These figures were correct as of January 27, 2026, 10:30 AM London time"
  },
  "media": [
    {"url": "https://...", "alt": "Alt text"}
  ],
  "permalink": "https://x.com/asjwebley/status/2011173003997188386"
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
- **Source elements:** `<div class="timeline-item" data-username="asjwebley">`
- **Text extraction:** Excludes quoted content from quote tweets
- **Engagement data:** Snapshot from January 27, 2026; February 2026 data from February 19, 2026

## January 2026 update (lightbrd HTML)

Four missing tweets were added to `posts-2026-01.json` from `Andrew Webley (@asjwebley) _ lightbrd.html`:
- **2017143724858286103** (Jan 30) — Original: Bitcoin as store of value / corporate treasury (personal view).
- **2016764105114181898** (Jan 29) — Original: Speaking at MadBitcoin_2026, Madrid, May 2026.
- **2016782854198321312** (Jan 29) — Reply: Event agenda timing, invite to say hello.
- **2016566382045884614** (Jan 28) — Reply: Aquis to LSE / AIM to Main Market examples.

Media arrays were left empty (no media URLs added) per archive policy.

## February 2026 update (lightbrd HTML)

January 2026 updated with 3 additional tweets (40 → 43 posts) and February 2026 added (26 posts) from `Andrew Webley (@asjwebley) _ lightbrd.html` snapshot taken February 19, 2026.

New January posts:
- **2017704095847465158** (Jan 31) — Original: Follow-up on Bitcoin price action.
- **2017515205794631930** (Jan 31) — Reply: Attending an event.
- **2017473893502505241** (Jan 31) — Quote: Weekly update on Aquis listing anniversary week.

February 2026 (26 posts): LSE listing day, Strategy World announcement, weekly updates, Bitcoin purchase announcements, stamp duty inquiry, unconference promotion. 14 low-content replies filtered out.

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
