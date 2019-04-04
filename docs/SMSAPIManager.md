# SMSAPIManager

Module to send SMS

!> In our system we can only send SMS to verifed phone number in Twilio account as a free trial

## Prerequisites

```bash
pip install twilio
```

and

Twilio account activated from https://twilio.com/console

## Functions 

### 1. sendSMSToSubscribers
```python
def sendSMSToSubscribers(incident):
```

Args:

incident (Dictionary): incident data dictionary from [FirebaseAPIManger](/FirebaseAPIManager?id=_4-getincidentfromfirebase)

Result:

Determine which subscribers to send sms depending on the region the incident is in and sends SMS

### 2. sendSMSToGovAgent
```python
def sendSMSToGovAgent(incident):
```

Args:

incident (Dictionary): incident data dictionary from [FirebaseAPIManger](/FirebaseAPIManager?id=_4-getincidentfromfirebase)

Result:

Sends SMS to Government Agent phone numbers regardless of the incident type/region