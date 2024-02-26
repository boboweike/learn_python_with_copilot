# reduce 函数的用法

```py
# 导入functools模块
import functools

# 定义一个字符列表letters，其中包含"H", "E", "L", "L", "O"五个字符
letters = ["H", "E", "L", "L", "O"]
# 使用reduce函数将letters列表中的字符连接起来
result = functools.reduce(lambda x, y: x + y, letters)
# 打印结果
print(result)


# 定义一个数字列表numbers，其中包含1, 2, 3, 4, 5五个数字
numbers = [1, 2, 3, 4, 5]
# 使用reduce函数将numbers列表中的数字相加
result = functools.reduce(lambda x, y: x + y, numbers)
# 打印结果
print(result)
```
