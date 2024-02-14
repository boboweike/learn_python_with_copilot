# 剪刀石头布游戏

```py
# 导入random模块
import random

# 定义一个选项options元组，包含剪刀、石头、布三个元素
options = ('剪刀', '石头', '布')
# 定义一个程序运行中变量running，用于判断程序是否继续运行
running = True

# 当running是True，执行循环
while running:
    # 通过random.choice()函数从options元组中随机选择一个元素
    computer_choice = random.choice(options)
    # 通过input()函数接收用户输入
    user_choice = input('请输入剪刀、石头或布：')
    # 通过if语句判断用户输入是否合法
    if user_choice in options:
        # 通过if语句判断用户和程序的选择，输出结果
        if user_choice == computer_choice:
            print('平局，程序选择了', computer_choice)
        elif ((user_choice == '剪刀' and computer_choice == '布') or
              (user_choice == '石头' and computer_choice == '剪刀') or
              (user_choice == '布' and computer_choice == '石头')):
            print('你赢了，程序选择了', computer_choice)
        else:
            print('你输了，程序选择了', computer_choice)
    else:
        print('输入错误，请重新输入')
    # 通过input()函数接收用户输入，判断是否继续运行
    running = input('是否继续？（yes/no）').lower() == 'yes'

# 输出: 欢迎再来玩！
print('欢迎再来玩！')
```
