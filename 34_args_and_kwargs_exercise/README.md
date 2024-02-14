# `*args 和**kwargs`综合应用

```py
# 定义一个函数shipping_label, 分别接受*args和**kwargs两种参数
# 位置参数包括title, first_name, last_name
# 关键字参数包括street, apt, city, state, zip_code
# 函数输出格式如下:
#     title first_name last_name
#     如果有apt，则输出：
#     street, apt
#     city, state zip_code
#     否则输出：
#     street
#     city, state zip_code
def shipping_label(*args, **kwargs):
    print(f"{args[0]} {args[1]} {args[2]}")
    if 'apt' in kwargs:
        print(f"{kwargs['street']}, {kwargs['apt']}")
    else:
        print(f"{kwargs['street']}")
    print(f"{kwargs['city']}, {kwargs['state']} {kwargs['zip_code']}")


# 调用函数shipping_label，不带apt参数
shipping_label('Mr.', 'John', 'Doe', street='123 Main St', city='New York', state='NY', zip_code='10001')
# 调用函数shipping_label，带apt参数
shipping_label('Ms.', 'Jane', 'Smith', street='456 Elm St', apt='2A', city='Los Angeles', state='CA', zip_code='90001')
```
