# 列表推到式(list compression)

```py
# 创建一个空列表squares
squares = []
# 循环遍历1-10,计算每个数的平方,并添加到squares列表中
for x in range(1, 11):
    squares.append(x**2)
# 输出squares列表
print(squares)


# 使用列表推到式实现上述功能
squares = [x**2 for x in range(1, 11)]

print(squares)


# 给出一个学生成绩列表students，其中包括10个学生的成绩，有少数学生的成绩不及格
students = [90, 78, 65, 45, 88, 99, 100, 55, 60, 70]
# 使用filter函数和lambda表达式过滤出及格的学生
passed_students = list(filter(lambda x: x >= 60, students))
# 输出及格的学生
print(passed_students)

# 使用列表推到式实现上述功能
passed_students = [x for x in students if x >= 60]
print(passed_students)

# 使用列表推到式实现上述功能，不及格学生的成绩显示为"不及格"
passed_students = [x if x >= 60 else "不及格" for x in students]
print(passed_students)
```
