# PostalCodeAPIManager

Helper module to convert postal code to anyother useful representation for location

For postal codes in Singapore, the first 2 digits in the 6 digit postal code represents the district it is within. 
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
# First 2 digits of postal code => district number
post_to_district_dict = {
	"01": ["01", "02", "03", "04", "05", "06"], 
  "02": ["07", "08"], 
  "03": ["14", "15", "16"], 
  "04": ["09", "10"], 
  "05": ["11", "12", "13"], 
  "06": ["17"], 
  "07": ["18", "19"],
  "08": ["20", "21"], 
  "09": ["22", "23"], 
  "10": ["24", "25", "26", "27"], 
  "11": ["28", "29", "30"],
  "12": ["31", "32", "33"], 
  "13": ["34", "35", "36", "37"], 
  "14": ["38", "39", "40", "41"], 
  "15": ["42", "43", "44", "45"], 
  "16": ["46", "47", "48"], 
  "17": ["49", "50", "81"], 
  "18": ["51", "52"], 
  "19": ["53", "54", "55", "82"],
  "20": ["56", "57"], 
  "21": ["58", "59"], 
  "22": ["60", "61", "62", "63", "64"], 
  "23": ["65", "66", "67", "68"], 
  "24": ["69", "70", "71"], 
  "25": ["72", "73"], 
  "26": ["77", "78"],
  "27": ["75", "76"],
  "28": ["79", "80"]
  }
# District no. to district
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
