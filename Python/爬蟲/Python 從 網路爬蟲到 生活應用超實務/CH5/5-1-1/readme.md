原程式碼 第七行 執行會有錯誤需先打以下指令或  
lxml >> xml
```
pip install lxml
```

```Python
import requests
from bs4 import BeautifulSoup 

url = "https://fchart.github.io/"
response = requests.get(url)
if response.status_code == 200:
    soup = BeautifulSoup(response.text, "lxml")
    tags = soup("a")
    for tag in tags:
        print(tag.get("href", None))
else:
    print("錯誤! HTTP請求失敗...")
```
