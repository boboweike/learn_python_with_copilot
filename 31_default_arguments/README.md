# 函数的缺省参数

# 什么是函数的缺省参数[ask_copilot]

```py
# 定义一个函数net_price, 有三个参数，分别是price, discount, tax
# 计算公式为：price * (1 - discount) * (1 + tax)
# discount和tax是缺省参数，分别为0和0.05
def net_price(price, discount=0.0, tax=0.05):
    return price * (1 - discount) * (1 + tax)


# 调用函数net_price
print(net_price(100))  # 105.0
print(net_price(100, 0.1))  # 94.5
print(net_price(100, 0.1, 0.1))  # 99.0


import time


# 定义一个count_up函数，有两个参数，分别是start和end
# 每输出一个数字，就将睡眠1秒，最后输出：结束！
# start的缺省参数为1
def count_up(end, start=1):
    while start <= end:
        print(start)
        start += 1
        time.sleep(1)
    print('结束！')


# 调用函数count_up
count_up(5)
count_up(5, 3)
```
