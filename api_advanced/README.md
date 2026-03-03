# API Advanced

## Description
This project focuses on querying the Reddit API using Python. It covers how to read API documentation, handle pagination, make recursive API calls, and sort results. These are common skills tested in technical interviews.

## Requirements
- Python 3.4.3
- Ubuntu 14.04 LTS
- `requests` module
- PEP 8 style

## Installation
```bash
pip install requests
```

## Files

| File | Description |
|------|-------------|
| `0-subs.py` | Returns the number of subscribers for a given subreddit |
| `1-top_ten.py` | Prints the top 10 hot posts for a given subreddit |
| `2-recurse.py` | Recursively returns all hot article titles for a given subreddit |
| `3-count.py` | Recursively counts and prints sorted keyword occurrences in hot posts |

## Usage

### Task 0 - Number of Subscribers
```bash
python3 0-main.py programming
# Output: 756024

python3 0-main.py this_is_a_fake_subreddit
# Output: 0
```

### Task 1 - Top Ten Posts
```bash
python3 1-main.py programming
# Output: prints titles of top 10 hot posts

python3 1-main.py this_is_a_fake_subreddit
# Output: None
```

### Task 2 - Recurse
```bash
python3 2-main.py programming
# Output: 932

python3 2-main.py this_is_a_fake_subreddit
# Output: None
```

### Task 3 - Count Keywords
```bash
python3 3-main.py programming 'python java javascript'
# Output:
# java: 27
# javascript: 20
# python: 17

python3 3-main.py not_a_valid_subreddit 'python java'
# Output: (nothing)
```

## Key Concepts
- **API pagination**: Reddit splits results into pages using an `after` parameter
- **Recursive functions**: Used to fetch all pages without loops
- **allow_redirects=False**: Prevents following redirects from invalid subreddits to search results
- **Custom User-Agent**: Required by Reddit API to avoid rate limiting


