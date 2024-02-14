# 函数(function)

## 在 python 中，什么是函数(function)[ask_copilot]

## 演示

```py
# 打印输出生日快乐歌
print("Happy Birthday to you!")
print("Happy Birthday to you!")
print("Happy Birthday, dear you!")
print("Happy Birthday to you!")


# 实现一个函数happy_birthday，打印输出生日快乐歌
def happy_birthday():
    print("Happy Birthday to you!")
    print("Happy Birthday to you!")
    print("Happy Birthday, dear you!")
    print("Happy Birthday to you!")
    print()


# 调用函数happy_birthday三次
happy_birthday()
happy_birthday()
happy_birthday()


# 函数参数
# 定义一个函数happy_birthday_with_name，打印输出生日快乐歌，其中you替换成name
def happy_birthday_with_name(name):
    print("Happy Birthday to you!")
    print("Happy Birthday to you!")
    print(f"Happy Birthday, dear {name}!")
    print("Happy Birthday to you!")
    print()


# 调用函数happy_birthday_with_name，传入参数"Tom"
happy_birthday_with_name("Tom")
# 调用函数happy_birthday_with_name，传入参数"Jerry"
happy_birthday_with_name("Jerry")
# 调用函数happy_birthday_with_name，传入参数"Jack"
happy_birthday_with_name("Jack")


# 接受两个参数
# 定义一个函数happy_birthday_with_name_and_age，打印输出生日快乐歌，其中you替换成name，age替换成age
def happy_birthday_with_name_and_age(name, age):
    print("Happy Birthday to you!")
    print("Happy Birthday to you!")
    print(f"Happy Birthday, dear {name}!")
    print(f"You are {age} years old!")
    print("Happy Birthday to you!")
    print()


# 调用函数happy_birthday_with_name_and_age，传入参数"Tom"和"18"
happy_birthday_with_name_and_age("Tom", 18)
# 调用函数happy_birthday_with_name_and_age，传入参数"Jerry"和"20"
happy_birthday_with_name_and_age("Jerry", 20)
# 调用函数happy_birthday_with_name_and_age，传入参数"Jack"和"22"
happy_birthday_with_name_and_age("Jack", 22)

# 穿入参数时，参数的顺序要和函数定义时的参数顺序一致
# 调用函数happy_birthday_with_name_and_age，传入参数"18"和"Tom"
happy_birthday_with_name_and_age(18, "Tom")


# 定义一个函数display_invoice，打印输出发票信息
# 参数：username, amount, due_date
def display_invoice(username, amount, due_date):
    print(f"Dear {username},")
    print(f"Your invoice amount is {amount}.")
    print(f"Please pay before {due_date}.")
    print()


# 调用函数display_invoice，传入参数"Tom", 100, "2021-12-31"
display_invoice("Tom", 100, "2021-12-31")


# 函数返回值
# 定义一个函数add/sub/mul/div，分别返回两个参数的和/差/积/商
def add(a, b):
    return a + b


def sub(a, b):
    return a - b


def mul(a, b):
    return a * b


def div(a, b):
    return a / b


# 调用函数add/sub/mul/div，传入参数1和2，打印函数返回值
print(add(1, 2))
print(sub(1, 2))
print(mul(1, 2))
print(div(1, 2))


def create_name(first, last):
    """
    This function takes two parameters, first and last, and returns the full name.
    :param first: first name
    :param last: last name
    :return: full name with first and last name capitalized
    """
    return first.capitalize() + " " + last.capitalize()


# 调用函数create_name，传入参数"tom"和"jerry"，打印函数返回值
print(create_name("tom", "jerry"))
```
