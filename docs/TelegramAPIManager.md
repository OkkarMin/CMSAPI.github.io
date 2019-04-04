# TelegramAPIManager

Post message to Telegram channel. Posted message can contain text and photo

## Prerequisites

```bash
pip install requests
```

and

Following procedures:
1. create a bot
2. get its token and ksys
3. enter https://api.telegram.org/bot798092482:AAEYOmSAs1rL1ejwfWF5ZbkRaTWeQY11jzw as the base url
5. set this bot as administrator of the channel, private channel_id: -100xxxxxxxxx->in the link of your channel
4. https://api.telegram.org/bot798092482:AAEYOmSAs1rL1ejwfWF5ZbkRaTWeQY11jzw sendMessage?text="text_you_want_to_send"&chat_id=-100xxxxxxxxx

## Functions 

### 1. telegram_post
```python
def telegram_post(text, photo_url, chat = "-1001475571282"):
```

Args:

text (String): Text message to post to Telegram channel group

photo_url (String): URL of photo to post to Telegram channel group

Result:

Text and Photo is posted onto Telegram channel.