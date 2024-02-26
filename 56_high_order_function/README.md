# 高阶函数(high order function)

```py
# 函数作为参数传递给另一个函数
def loud(text):
    return text.upper()


def quiet(text):
    return text.lower()


def hello(func, text):
    result = func(text)
    print(result)


hello(loud, 'Hello')
hello(quiet, 'Hello')


# 函数作为返回值
# divisor = 除数
# dividend = 被除数

def divisor(x):
    def dividend(y):
        return y / x
    return dividend


divide = divisor(2)
print(divide(10))
```
