# TwitterAPIManager

Post tweet to twitter

>! We are not integrating this module with our system anymore as we failed to obtain the Twitter DEV API Key. Twitter rejected our request

## Prerequisites

```bash
pip install tweepy
```

## Functions 

### 1. twitterShare
```python
def twitterShare(status_text):
```

Args:

status_text (String): Tweet to post to linked twitter account. Must be <= 140 characters

Result:

Tweet is posted to linked twitter account