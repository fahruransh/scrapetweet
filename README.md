# scrapetweet

Search recent tweets by keyword using the X API, with automatic retry on rate limits.

## How it works

`scrapetweet.py` uses [Tweepy](https://www.tweepy.org/) to call the X API v2 recent-search
endpoint. You enter a search query and how many tweets to fetch (10–100); matching tweets are
printed to the terminal. If the API rate limit is hit, the script backs off exponentially and
retries (up to 5 times).

## Requirements

- Python 3
- A [X Developer](https://developer.x.com/en/portal) Bearer Token

## Setup

```bash
pip install tweepy
```

Set your token as an environment variable (don't paste it into the script):

```bash
export X_BEARER_TOKEN="your_bearer_token"
```

## Usage

```bash
python scrapetweet.py
```

Then enter your search query and the number of tweets to retrieve (10–100, default 10).

Example:

```
Enter your search query: kopi
Enter the number of tweets to retrieve (10-100): 3

Retrieved Tweets:
1. Ngopi pagi dulu sebelum mulai kerja.
2. Kopi susu gula aren masih juara sih.
3. Ada rekomendasi kedai kopi di Magelang?
```

## Tech

- Python
- Tweepy (X API v2 client)
