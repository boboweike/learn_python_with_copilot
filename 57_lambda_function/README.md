# Lambda 函数

```py
# 定义一个lambda函数double
double = lambda x: x * 2
print(double(5))

# 定义一个lambda函数multiply
multiply = lambda x, y: x * y
print(multiply(2, 3))

# 定义一个lambda函数add, 用于对三个数进行求和
add = lambda x, y, z: x + y + z
print(add(1, 2, 3))

# 定义一个lambda函数full_name, 用于拼接两个字符串
full_name = lambda first_name, last_name: first_name + ' ' + last_name
print(full_name('John', 'Doe'))

# 定义一个lambda函数age_check，用于判断年龄是否大于18岁
age_check = lambda age: True if age > 18 else False
print(age_check(20))
```
