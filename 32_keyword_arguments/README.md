# 关键字参数

## 什么是关键字参数[ask_copilot]

```py
# 定义一个hello函数, 有四个参数，greeting, title, first, last
def hello(greeting, title, first, last):
    print(f'{greeting}, {title} {first} {last}')


# 调用hello函数，传入参数
hello('Hello', title='Mr.', first='Gao', last='Yan')

# 使用for循环打印1～10，数字之间用空格隔开
for i in range(1, 11):
    print(i, end=' ')

# 打印输出'1' - '6'共六个字符，使用'-'进行分隔(使用sep参数)
print('1', '2', '3', '4', '5', '6', sep='-')


# 定义一个get_phone函数，支持4个参数，country_code, area_code, prefix, line_number
def get_phone(country_code, area_code, prefix, line_number):
    return f'+{country_code}({area_code})-{prefix}-{line_number}'


# 调用get_phone函数，传入带有关键字的参数
phone = get_phone(country_code=86, area_code=10, prefix=123, line_number=4567)
print(phone)
```
