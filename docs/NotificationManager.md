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