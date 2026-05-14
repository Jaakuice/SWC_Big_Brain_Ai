# @the_desert_ape X.com Posts - Extracted Data

## Overview

This directory contains structured data extracted from @the_desert_ape's X.com timeline.

**Role:** SWC employee
**Source:** Scraped via Playwright + xcancel.com (Nitter frontend)
**Extracted:** May 14, 2026 — 15 scroll pages, with replies
**Total Posts:** 262 (316 raw, 54 filtered)

## Statistics

### By Month
- **2026-05**: 60 posts
- **2026-04**: 202 posts

## Files

Monthly JSON files in format `posts-YYYY-MM.json`:
- `posts-2026-05.json` (60 posts)
- `posts-2026-04.json` (202 posts)

## JSON Schema

Each post object contains:

```json
{
  "type": "original|reply|quote|repost_with_comment",
  "post_id": "unique_id_string",
  "date_time": "May 12, 2026 · 8:49 AM UTC",
  "text": "Full text content by @the_desert_ape",
  "is_reply": true,
  "is_thread_starter": false,
  "engagement": {
    "comments": 0,
    "reposts": 0,
    "likes": 0,
    "note": "These figures were correct as of May 14, 2026, 7:08 AM London time"
  },
  "media": [
    {"url": "https://...", "alt": ""}
  ],
  "permalink": "https://x.com/the_desert_ape/status/[post_id]"
}
```

## Content Filtering

Posts filtered to exclude:
- Empty or whitespace-only content
- Single emoji replies (🙏, etc.)
- Minimal text ("lol", "yes", "no", "thanks")
- Replies with <10 characters or <2 words
- Original posts with <3 words and <15 characters
- Pure retweets

## Extraction Method

- **Source:** xcancel.com (Nitter frontend) via Playwright stealth browser
- **Script:** `scripts/scrape_x.py` + `scripts/tweet_updater.py`
- **Scrolls:** 15 pages loaded (Tweets & Replies tab)
- **Text extraction:** Excludes quoted content from quote tweets
- **Engagement data:** Snapshot from May 14, 2026

## Usage

```python
import json
from pathlib import Path

# Load specific month
with open('posts-2026-05.json', 'r') as f:
    may_posts = json.load(f)

# Load all posts
all_posts = []
for json_file in sorted(Path('.').glob('posts-*.json')):
    with open(json_file, 'r') as f:
        all_posts.extend(json.load(f))
```
