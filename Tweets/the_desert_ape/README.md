# @the_desert_ape X.com Posts - Extracted Data

## Overview

This directory contains structured data extracted from @the_desert_ape's X.com timeline.

**Role:** SWC employee
**Source:** Manual extraction from X.com timeline
**Extraction started:** May 2026
**Total Posts:** 0 (archive pending population)

## Files

Monthly JSON files in format `posts-YYYY-MM.json`:
- `posts-2026-05.json` (0 posts — placeholder, populate from X.com)

## JSON Schema

Each post object contains:

```json
{
  "type": "original|reply|quote|repost_with_comment",
  "post_id": "unique_id_string",
  "date_time": "May 14, 2026 · 10:00 AM UTC",
  "text": "Full text content by @the_desert_ape",
  "is_reply": true,
  "is_thread_starter": false,
  "engagement": {
    "comments": 0,
    "reposts": 0,
    "likes": 0,
    "note": "These figures were correct as of [date], [time] London time"
  },
  "media": [],
  "permalink": "https://x.com/the_desert_ape/status/[post_id]"
}
```

## Content Filtering

Posts should be filtered to exclude:
- Empty or whitespace-only content
- Single emoji replies (🙏, etc.)
- Minimal text ("lol", "yes", "no", "thanks")
- Replies with <10 characters or <2 words
- Original posts with <3 words and <15 characters

## Extraction Method

- **Source:** X.com / Nitter / lightbrd HTML snapshots
- **Parser:** BeautifulSoup4 with lxml (see asjwebley folder for reference scripts)
- **Text extraction:** Excludes quoted content from quote tweets
- **Engagement data:** Snapshot from extraction date

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
