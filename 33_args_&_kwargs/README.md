# `*args & **kwargs`参数

```py
# 定义一个add函数，可以接收任意个参数*args
def add(*args):
    print(type(args))
    print(args)
    sum = 0
    for arg in args:
        sum += arg
    return sum


# 调用add函数，传入1个参数，2个参数，5个参数，10个参数
print(add(1))
print(add(1, 2))
print(add(1, 2, 3, 4, 5))
print(add(1, 2, 3, 4, 5, 6, 7, 8, 9, 10))


# 定义一个print_address函数，可以接收关键字参数**kwargs
def print_address(**kwargs):
    print(type(kwargs))
    print(kwargs)
    for key, value in kwargs.items():
        print(f'{key}: {value}')


# 调用print_address函数, 传入多个参数包括street, city, state, zip
# 再添加一个参数apt
print_address(street='123 Main St', city='Anytown', state='AS', zip='12345', apt='1A')
```
