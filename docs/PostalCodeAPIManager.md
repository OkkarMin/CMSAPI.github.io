# PostalCodeAPIManager

Helper module to convert postal code to anyother useful representation for location

## Prerequisites

`postalcoes.json` file found in `/baseapp/APImodules/postalcodes.json`

## Functions 

### 1. postal_code_to_latlong
```python
def postal_code_to_latlong(postal_code):
```

Args:

postal_code (String): a valid postal code in Singapore

Return:

latitude (String), longitude (String) representation of the postal code

```python
lat, long = postal_code_to_latlong('123456')
```

### 2. postal_code_to_region
```python
def postal_code_to_region(postal_code):
```

Args:

postal_code (String): a valid postal code in Singapore

Return:

region in Singapore

```python
regions = ['south_west', 'north_west', 'central', 'north_east', 'south_east']
```

```python
region = postal_code_to_latlong('142035')
assert(region == 'central')
```

### 3. postal_code_to_area
```python
def postal_code_to_area(postal_code):
```

Args:

postal_code (String): a valid postal code in Singapore

Return:

area in Singapore from district_to_area_dict

```python
district_to_area_dict = {
  "Raffles Place": "01",
  "Anson": "02",
  "Bukit Merah": "03",
  "Telok Blangah": "04",
  "Pasir Panjang": "05",
  "High Street": "06",
  "Middle Road": "07",
  "Little India": "08",
  "Orchard": "09",
  "Ardmore": "10",
  "Watten Estate": "11",
  "Balestier": "12",
  "Macpherson": "13",
  "Geyland": "14",
  "Katong": "15",
  "Bedok": "16",
  "Loyang": "17",
  "Simei": "18",
  "Serangoon Garden": "19",
  "Bishan": "20",
  "Upper Bukit Timah": "21",
  "Jurong": "22",
  "Hillview": "23",
  "Lim Chu Kang": "24",
  "Kranji": "25",
  "Upper Thomson": "26",
  "Yishun": "27",
  "Seletar": "28"
}
```

```python
region = postal_code_to_latlong('142035')
assert(region == 'central')
```
