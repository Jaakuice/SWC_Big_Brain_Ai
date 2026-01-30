# @smarterwebuk X.com Posts - Extracted Data

## Overview

This directory contains structured data extracted from @smarterwebuk's X.com timeline.

**Extracted:** January 27, 2026 at 12:30 PM; **updated** with missing tweets from lightbrd HTML snapshot.
**Total Timeline Items:** 134
**Meaningful Posts:** 136 (including 4 added from lightbrd snapshot)
**Filtered Out:** 2

## Statistics

### By Post Type
- **original**: 133
- **quote**: 3

### By Month
- **2026-01**: 24 posts
- **2025-12**: 12 posts
- **2025-11**: 8 posts
- **2025-10**: 8 posts
- **2025-09**: 9 posts
- **2025-08**: 10 posts
- **2025-07**: 18 posts
- **2025-06**: 17 posts
- **2025-05**: 20 posts
- **2025-04**: 6 posts
- **2025-03**: 4 posts

## Files

Monthly JSON files in format `posts-YYYY-MM.json`:
- `posts-2026-01.json` (24 posts)
- `posts-2025-12.json` (12 posts)
- `posts-2025-11.json` (8 posts)
- `posts-2025-10.json` (8 posts)
- `posts-2025-09.json` (9 posts)
- `posts-2025-08.json` (10 posts)
- `posts-2025-07.json` (18 posts)
- `posts-2025-06.json` (17 posts)
- `posts-2025-05.json` (20 posts)
- `posts-2025-04.json` (6 posts)
- `posts-2025-03.json` (4 posts)

## JSON Schema

Each post object contains:

```json
{
  "type": "original|reply|quote|repost_with_comment",
  "post_id": "2011173003997188386",
  "date_time": "Jan 13, 2026 · 8:26 PM UTC",
  "text": "Full text content by @smarterwebuk",
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
  "permalink": "https://x.com/smarterwebuk/status/2011173003997188386"
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
- **Source elements:** `<div class="timeline-item" data-username="smarterwebuk">`
- **Text extraction:** Excludes quoted content from quote tweets
- **Engagement data:** Snapshot from January 27, 2026

## January 2026 update (lightbrd HTML)

Four missing tweets were added to `posts-2026-01.json` from `The Smarter Web Company (@smarterwebuk) _ lightbrd.html`:
- **2016487226209689736** (Jan 28) — Original: RNS Result of General Meeting (resolution passed on a poll); thread starter.
- **2016487244635205843** (Jan 28) — Original: Thread reply with link to RNS on website.
- **2014058448447574245** (Jan 21) — Original: Livestream Friday with @asjwebley & @Croesus_BTC (LSE uplist, prospectus, 2026); 23 Jan 2pm UK.
- **2013144566128414786** (Jan 19) — Original: Announcement Bitcoin Treasuries Unconference UK (Bristol, one-day event, link in comments).

Media arrays were left empty (no media URLs added) per archive policy.

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
