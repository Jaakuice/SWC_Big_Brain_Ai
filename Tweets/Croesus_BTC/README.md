# @Croesus_BTC X.com Posts - Extracted Data

## Overview

This directory contains structured data extracted from @Croesus_BTC's X.com timeline.

**Extracted:** January 27, 2026 at 01:18 PM
**Total Timeline Items:** 304
**Meaningful Posts:** 288
**Filtered Out:** 16

## Statistics

### By Post Type
- **original**: 197
- **quote**: 91

### By Month
- **2026-01**: 30 posts
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
- `posts-2026-01.json` (30 posts)
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
- **Engagement data:** Snapshot from January 27, 2026

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
