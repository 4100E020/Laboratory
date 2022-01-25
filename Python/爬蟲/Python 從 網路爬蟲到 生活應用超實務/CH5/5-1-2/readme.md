```Python
import requests 
from bs4 import BeautifulSoup

url = "https://fchart.github.io/"
response = requests.get(url)
soup = BeautifulSoup(response.text, "lxml")
tags = soup("a")
tag = tags[12]
print("URL網址: ", tag.get("href", None))
print("標籤內容: ", tag.text)
print("target屬性: ", tag["target"])
tags = soup("img")
tag = tags[1]
print("圖片網址: ", tag.get("src", None))
print("alt屬性: ", tag["alt"])
print("屬性: ", tag.attrs)
```
```
URL網址:  http://blockly.is-best.net/
標籤內容:  ESP8266 Blockly for MicroPython 英文線上版
target屬性:  _blank
圖片網址:  img/fchart01.png
alt屬性:  fChart直譯器圖例
屬性:  {'class': ['img-fluid', 'rounded', 'mb-3', 'mb-md-0'], 'src': 'img/fchart01.png', 'alt': 'fChart直譯器圖例'}
```
