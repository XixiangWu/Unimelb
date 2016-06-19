### What is being transmitted?
* XML = eXtensible Markup Language

### Javascript
* "lightweight" **client-side** programming language

### Using JSON in Python

```python
from urllib2 import urlopen
import json

url = 'https://data.melbourne.vic.gov.au/api/views/ru3z-44we/rows.json?accessType=DOWNLOAD'

stream = urlopen(url)
data = json.load(stream)
data["data"][0][8:11]

for row in data["data"]:
    print row[8:11]
```