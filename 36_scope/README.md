# 变量作用域(scope)和作用域解析 LEGB

## 什么是变量作用域(scope)？什么是作用域解析(LEGB)?[ask_copilot]


```py
# 局部(Local)作用域

# def fun1():
#     a = 10
#     print(a)
#
#
#
# def fun2():
#     a = 20
#     print(a)
#
#
# def fun1():
#     x = 10
#     print(x)
#
#
# def fun2():
#     x = 20
#     print(x)
#
#
# fun1()
# fun2()
#
# Enclosing 作用域
#
# def func1():
#     x = 10
#
#     def func2():
#         print(x)
#
#     func2()
#
# func1()

# 全局(Global)作用域
# def func1():
#     print(x)
#
#
# def func2():
#     print(x)
#
#
# x = 10
#
# func1()
# func2()

# 内置(Built-in)作用域

# from math import e
#
#
# def func1():
#     print(e)
#
#
# e = 10
#
# func1()
```
