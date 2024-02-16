# 文件检测

```py
# 假设路径path为：/Users/boboweike/Desktop/test.txt
# 检测路径是否存在: 如果存在输出路径存在，如果路径不存在输出路径不存在
# 再检测路径是文件还是目录：如果路径是文件则输出路径是文件，如果路径是目录则输出路径是目录

import os

path = '/Users/boboweike/Desktop/test.txt'

if os.path.exists(path):
    print('路径存在')
    if os.path.isfile(path):
        print('路径是文件')
    else:
        print('路径是目录')
else:
    print('路径不存在')
```
