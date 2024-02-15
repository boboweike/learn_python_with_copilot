# 模块(module)

## 在 Python 中，什么是模块(module)?[ask_copilot]

## 模块演示

```py
# 通过help查看modules的详细文档
# print(help('modules'))

# 查看math模块的详细文档
# print(help('math'))

# 导入math模块
# import math
# 导入math模块as m
# import math as m
# 通过from导入math模块的pi属性
# from math import pi

# 输出math模块的pi属性
# print(pi)

# 冲突演示
# 通过from导入math模块的e属性
from math import e

# 打印输出e
print(e)

# 定义a, b, c, d四个变量, 分别赋值为1, 2, 3, 4
a, b, c, d = 1, 2, 3, 4
# 打印输出a的e次方, b的e次方, c的e次方, d的e次方
print(a ** e, b ** e, c ** e, d ** e)

# 定义a, b, c, d, e五个变量, 分别赋值为1, 2, 3, 4，5
a, b, c, d, e = 1, 2, 3, 4, 5
# 打印输出e的a次方, b次方, c次方, d次方, e次方
print(e ** a, e ** b, e ** c, e ** d, e ** e)

# 导入math模块
import math

# 打印输出math.e的a次方, b次方, c次方, d次方, e次方
print(math.e ** a, math.e ** b, math.e ** c, math.e ** d, math.e ** e)
```

## 自定义模块 example

```py
# 定义一个变量pi, 赋值为3.14
pi = 3.14


# 定义一个函数square, 有一个参数x, 返回x的平方
def square(x):
    return x ** 2


# 定义一个函数cube, 有一个参数x, 返回x的立方
def cube(x):
    return x ** 3


# 定义一个函数circumference, 有一个参数r, 返回圆的周长
def circumference(r):
    return 2 * pi * r


# 定义一个函数area, 有一个参数r, 返回圆的面积
def area(r):
    return pi * square(r)
```

## 使用自定义模块

```py
# 导入example模块
import example

# 打印输出example模块的pi属性
print(example.pi)

# 调用example模块的square函数, 传入参数5
print(example.square(5))

# 调用example模块的cube函数, 传入参数5
print(example.cube(5))

# 调用example模块的circumference函数, 传入参数5
print(example.circumference(5))

# 调用example模块的area函数, 传入参数5
print(example.area(5))
```
