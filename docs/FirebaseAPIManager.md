# FirebaseAPIManager

A client for interacting with Firebase cloud commands from Python

## Prerequisites

```bash
pip install --upgrade firebase-admin
```

and

Set up development environment <https://firebase.google.com/docs/firestore/quickstart>

## Functions

### 1\. saveIncidentToFirebase(request)

```python
def saveIncidentToFirebase(request):
```

Args:

request (HTTPRequest): POST request containing incident data made by client

Return:

Python dictionary object containing incidents data

```python
data = {
  'incident_id': incident_id,
  'incident_type': incident_type,
  'incident_managedBy': incident_managedBy,
  'incident_area': incident_area,
  'incident_region': incident_region,
  'incident_status': incident_status,
  'incident_level': incident_level,
  'incident_created_at_date': incident_created_at_date,
  'incident_created_at_time': incident_created_at_time,
  'incident_address': incident_address,
  'incident_postalcode': incident_postalcode,
  'incident_lat': incident_lat,
  'incident_lng': incident_lng,
  'incident_description': incident_description
}
```

### 2\. saveIncidentToFirebase

```python
def saveReportToFirebase(incident_id, request):
```

Args:

incident_id (String): ID of Incident that report data is related to\
request (HTTPRequest): POST request containing report data made by client

Return:

Python dictionary object containing incidents data

```python
data = {
  'report_num_of_casualties': report_num_of_casualties,
  'report_assistance_requested': report_assistance_requested,
  'report_assistance_dispatch_id': report_assistance_dispatch_id,
  'report_num_ambulance': report_num_ambulance,
  'report_num_firetruck': report_num_firetruck,
  'report_num_police': report_num_police,
  'report_num_gasleak': report_num_gasleak,
  'report_reporter_name': report_reporter_name,
  'report_reporter_number': report_reporter_number,
  'report_description': report_description,
  'report_status': report_status
}
```

### 3\. saveSubscriberToFirebase


```python
def saveSubscriberToFirebase(request):
```

Args:

request (HTTPRequest): POST request containing subscriber data made by client

### 4\. getIncidentFromFirebase

```python
def getIncidentFromFirebase(incident_id):
```

Args:

incident_id (String): ID of incident to get data

Return:

Python dictionary object containing incidents data

```python
data = {
  'incident_id': incident_id,
  'incident_type': incident_type,
  'incident_managedBy': incident_managedBy,
  'incident_area': incident_area,
  'incident_region': incident_region,
  'incident_status': incident_status,
  'incident_level': incident_level,
  'incident_created_at_date': incident_created_at_date,
  'incident_created_at_time': incident_created_at_time,
  'incident_address': incident_address,
  'incident_postalcode': incident_postalcode,
  'incident_lat': incident_lat,
  'incident_lng': incident_lng,
  'incident_description': incident_description
}
```

### 5\. getReportFromFirebase

```python
def getReportsFromFirebase(incident_id):
```

Args:

incident_id (String): ID of incident that reports data are linked to

Return:

Nested python dictionary object containing report data

```python
data = {
  '1' : {
  'report_num_of_casualties': report_num_of_casualties,
  'report_assistance_requested': report_assistance_requested,
  'report_assistance_dispatch_id': report_assistance_dispatch_id,
  'report_num_ambulance': report_num_ambulance,
  'report_num_firetruck': report_num_firetruck,
  'report_num_police': report_num_police,
  'report_num_gasleak': report_num_gasleak,
  'report_reporter_name': report_reporter_name,
  'report_reporter_number': report_reporter_number,
  'report_description': report_description,
  'report_status': report_status
  },
  '2' : {
  'report_num_of_casualties': report_num_of_casualties,
  'report_assistance_requested': report_assistance_requested,
  'report_assistance_dispatch_id': report_assistance_dispatch_id,
  'report_num_ambulance': report_num_ambulance,
  'report_num_firetruck': report_num_firetruck,
  'report_num_police': report_num_police,
  'report_num_gasleak': report_num_gasleak,
  'report_reporter_name': report_reporter_name,
  'report_reporter_number': report_reporter_number,
  'report_description': report_description,
  'report_status': report_status
  }
  .
  .
  .
}
```

### 6\. getAllSubscribers

```python
def getAllSubscribers():
```

Return:

Nested python dictionary object containing subscribers

```python
data = {
  '1' : {
    'subscriber_name': subscriber_name,
    'subscriber_number': subscriber_number,
    'subscriber_region': subscriber_region,
  },
  '2' : {
    'subscriber_name': subscriber_name,
    'subscriber_number': subscriber_number,
    'subscriber_region': subscriber_region,
  }
  .
  .
  .
}
```

### 7\. getSubscribersByRegion

```python
def getSubscribersByRegion(region):
```

Args:

region (String): region to get Subscribers data from

```python
regions = ['south_west', 'north_west', 'central', 'north_east', 'south_east']
```

Return:

Nested python dictionary object containing subscribers that are in given region

```python
data = {
  '1' : {
    'subscriber_name': subscriber_name,
    'subscriber_number': subscriber_number,
    'subscriber_region': subscriber_region,
  },
  '2' : {
    'subscriber_name': subscriber_name,
    'subscriber_number': subscriber_number,
    'subscriber_region': subscriber_region,
  }
  .
  .
  .
}
```