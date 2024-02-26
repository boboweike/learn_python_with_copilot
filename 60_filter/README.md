# filter 函数的使用

```py
# 定义一个friends列表，列表中的5个元素，它们都是元组，包括姓名和年龄两个元素
# 其中年龄有大于18和小于18两种情况
friends = [('Jerry', 22), ('Tom', 19), ('Mickey', 16), ('Donald', 20), ('Minnie', 17)]

# 使用filter函数，过滤出年龄大于18的元素，赋值给列表adult_friends
adult_friends = list(filter(lambda x: x[1] > 18, friends))

# 循环输出adult_friends列表中的元素
for friend in adult_friends:
    print(friend)
```
