# NotificationManager

Facade/Adapter functions To [FacebookAPIManger](FacebookAPIManager.md) and [TelegramAPIManager](TelegramAPIManager.md)

## Prerequisites

- [FacebookAPIManger](FacebookAPIManager.md)
- [TelegramAPIManager](TelegramAPIManager.md)

and

```bash
pip install Pillow
pip install requests
```

## Functions 

### 1. send_info_24hrs
```python
def send_info_24hrs():
```

Sends shelters and useful information to public via Facebook and Telegram using [FacebookAPIManger](FacebookAPIManager.md) and [TelegramAPIManager](TelegramAPIManager.md) respectively.

### 2. notify
```python
def notify(incident):
    #For CAT1 incidents, send immediately
    if incident_level == 'CAT1':
        facebookShare(message, image)
        telegram_post(message, url)
    #For CAT2, update when >= 6 hours from last CAT2 post
    elif incident_level == 'CAT2':
        check_update(incident_id)
```

