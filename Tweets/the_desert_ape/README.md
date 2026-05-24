# @the_desert_ape (Jamie Knowles) X.com Posts - Extracted Data

## Overview

This directory contains structured data extracted from @the_desert_ape's X.com timeline.

**Person:** Jamie Knowles — Head of Capital Markets, The Smarter Web Company
**Bio:** "Head of Capital Markets, The Smarter Web Company (@smarterwebuk) | Posting In A Personal Capacity"
**Source:** `Jamie Knowles (@the_desert_ape) _ lightbrd.html` (lightbrd snapshot, May 2026) + Playwright scrape via xcancel.com
**Extracted:** May 14, 2026
**Total Posts:** 2,853 (3,211 raw items; 215 retweets skipped; 143 filtered low-content)

## Statistics

### By Month
- **2026-05**: 98 posts
- **2026-04**: 202 posts
- **2026-03**: 55 posts
- **2026-02**: 71 posts
- **2026-01**: 36 posts
- **2025-12**: 7 posts
- **2025-11**: 7 posts
- **2025-10**: 33 posts
- **2025-09**: 132 posts
- **2025-08**: 180 posts
- **2025-07**: 634 posts
- **2025-06**: 728 posts
- **2025-05**: 547 posts
- **2025-04**: 161 posts

## Files

Monthly JSON files in format `posts-YYYY-MM.json`:
- `posts-2026-05.json` (98 posts)
- `posts-2026-04.json` (202 posts)
- `posts-2026-03.json` (55 posts)
- `posts-2026-02.json` (71 posts)
- `posts-2026-01.json` (36 posts)
- `posts-2025-12.json` (7 posts)
- `posts-2025-11.json` (7 posts)
- `posts-2025-10.json` (33 posts)
- `posts-2025-09.json` (132 posts)
- `posts-2025-08.json` (180 posts)
- `posts-2025-07.json` (634 posts)
- `posts-2025-06.json` (728 posts)
- `posts-2025-05.json` (547 posts)
- `posts-2025-04.json` (161 posts)

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
    "note": "These figures were correct as of May 14, 2026, 9:00 AM London time"
  },
  "media": [
    {"url": "https://pbs.twimg.com/...", "alt": ""}
  ],
  "permalink": "https://x.com/the_desert_ape/status/[post_id]"
}
```

## Content Filtering

Posts filtered to exclude:
- Pure retweets (no added commentary)
- Empty or whitespace-only content
- Single emoji replies (🙏, etc.)
- Minimal text ("lol", "yes", "no", "thanks")
- Replies with <10 characters or <2 words
- Original posts with <3 words and <15 characters

## Extraction Method

- **Primary source:** `Jamie Knowles (@the_desert_ape) _ lightbrd.html` — full lightbrd page snapshot parsed via BeautifulSoup4/lxml
- **Supplementary:** Playwright scrape via xcancel.com (Apr–May 2026 data already present, merged cleanly)
- **Text extraction:** Quoted tweet content removed before text extraction
- **Engagement data:** Snapshot from May 2026 (most figures 0 due to Nitter rate limiting)

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
