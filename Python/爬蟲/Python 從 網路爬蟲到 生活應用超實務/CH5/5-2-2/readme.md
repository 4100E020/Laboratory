```Python
import re

str1 = "ZheZahng's email is wolf93758@gmail.com"
match = re.search(r"[\w.-]+@[A-Za-z0-9_.-]+", str1)
if match:
    print(match.group())
else:
    print("沒有找到符合的字串!")
```

```
wolf93758@gmail.com
```
