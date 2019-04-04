# WeatherAPIManager

This module acts as a helper module to retrieve data provided by https://data.gov.sg/dataset/weather-forecast

## Prerequisites

```bash
pip install requests
```

## Functions 

### 1. getAllWeather
```python
def getAllWeather(time):
```

Args:

time (String): String in either one of the followings format

date and time:
YYYY-MM-DD[T]HH:mm:ss
Use this format to retrieve the latest forecast issued at that moment in time.

date:
YYYY-MM-DD
Use this format to retrieve all of the forecasts issued for a certain day.

Return:

A python object that contains weather forecasts for multiple areas in Singapore

```python
{
  "api_info": {
    "status": "healthy"
  },
  "area_metadata": [
    {
      "name": "string",
      "label_location": {
        "longitude": 0,
        "latitude": 0
      }
    }
  ],
  "items": [
    {
      "update_timestamp": "2019-03-07T07:56:25.548Z",
      "timestamp": "2019-03-07T07:56:25.548Z",
      "valid_period": {
        "start": "2019-03-07T07:56:25.548Z",
        "end": "2019-03-07T07:56:25.548Z"
      },
      "forecasts": [
        {
          "area": "string",
          "forecast": "string"
        }
      ]
    }
  ]
}
```

### 2. getWeatherByLocation
```python
def getWeatherByLocation(time, area):
```

Args:

time (String): String in either one of the followings format

date and time:
YYYY-MM-DD[T]HH:mm:ss
Use this format to retrieve the latest forecast issued at that moment in time.

date:
YYYY-MM-DD
Use this format to retrieve all of the forecasts issued for a certain day.

area (String): Area in Singapore

Return:

A python object that contains weather forecasts for a single area in Singapore

```python
{'AreaName': 'Forecast'}
```