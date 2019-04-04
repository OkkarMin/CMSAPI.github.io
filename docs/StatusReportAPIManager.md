# StatusReportAPIManager

Crafts email using [reportlab](https://www.reportlab.com/) and send by using [smtplib](https://docs.python.org/3/library/smtplib.html)

!> In our system we are sending email to cms3003report@gmail.com

## Prerequisites

- [FirebaseAPIManager](FirebaseAPIManager.md)
- Twilio account activated from https://twilio.com/console

```bash
pip install numpy
pip install pandas
pip install matplotlib
pip install reportlab
```

## Functions 

### 1. sendEmailToPMO
```python
def sendEmailToPMO():
```

Result:

Crafted email is send to `cms3003report@gmail.com`