# 移动(move)文件

## 在 Python 中，如何移动(move)文件？[ask_copilot]

```py
import os

src = "test.txt"
dest = "/Users/boboweike/Desktop/test.txt"

try:
  if os.path.exists(dest):
    print(dest+"文件已经存在！")
  else:
    os.replace(src, dest)
    print(src+"被移到了"+dest)
except FileNotFoundError:
  print(src+"未找到")
```
