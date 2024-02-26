# zip 函数

```py
# 定义一个usernames列表，包含3个用户名
usernames = ['张三', '李四', '王五']
# 定义一个passwords元组，包含3个密码
passwords = ('123', '456', '789')
# 使用zip函数将两个列表合并成一个users
users = zip(usernames, passwords)
# # 将users转换成列表
# users = list(users)
# 将users转换成字典
users = dict(users)

# 打印users的类型
print(type(users))

# 使用for循环遍历users
for key, value in users.items():
    print(key, value)

# 定义一个login_dates列表，包含3个登录时间
login_dates = ['2020-01-01', '2020-02-02', '2020-03-03']
# 使用zip函数将usernames, passwords和login_dates合并成一个users
users = zip(usernames, passwords, login_dates)
# 使用for循环遍历users
for user in users:
    print(user)
```
