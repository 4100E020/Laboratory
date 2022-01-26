安裝selenium
```
pip install selenium
```
安裝 Chormediver
```
https://chromedriver.chromium.org/home
選擇相應版本並安裝
```


```Python
from selenium import webdriver
from bs4 import BeautifulSoup

driver = webdriver.Chorme()
driver.implicitly_wait(10)
driver.get("https://fchart.github.io/Example.html")
print(driver.title)
soup = BeautifulSoup(driver.page_source, "lxml")
tag_ol = soup.find("ol", {"id":"list"})
tags_li = tag_ol.find_all("li", class_="line")
for tag in tags_li:
    print(tag.text)
driver.quit()
```
