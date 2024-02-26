# 海象运算符(walrus operator)

```py
# 定义一个布尔变量happy，赋值为True，然后打印这个变量
# 使用海象运算符实现上述功能
print(happy := True)


# 定义一个列表foods，持续请求用户输入一种他喜欢的food，
# 将food添加到foods列表中，直到用户输入quit为止
# 不使用海象运算符实现上述功能
foods = []
while True:
    food = input("Enter a food you like: ")
    if food == "quit":
        break
    foods.append(food)
```
