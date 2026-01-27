# @asjwebley X.com Posts - Extracted Data

## Overview

This directory contains structured data extracted from @asjwebley's X.com timeline.

**Source:** `@asjwebley_X.html` (saved Nitter frontend page)
**Extracted:** January 27, 2026 at 12:05 PM
**Total Timeline Items:** 1330
**Meaningful Posts:** 861
**Filtered Out:** 469

## Statistics

### By Post Type
- **original**: 225
- **quote**: 91
- **reply**: 527
- **repost_with_comment**: 18

### By Month
- **2026-01**: 36 posts
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
- `posts-2026-01.json` (36 posts)
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
