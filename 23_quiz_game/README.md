# 小测验游戏(quiz game)

```
# 小测验游戏(quiz game)

# 1. 变量定义
# 1.1 定义一个问题元组questions，其中包括五个元素，五个问题分别是：
#     1.1.1 法国的首都是？
#     1.1.2 世界上最大的洲是？
#     1.1.3 空气中最多的元素是？
#     1.1.4 哪个动物下得蛋最大？
#     1.1.5 太阳系中最大的行星是？
# 1.2 定义一个二维选项元组options，其中包括五行，每一行有四个元素：
#     1.2.1 A. 巴黎, B. 伦敦, C. 柏林, D. 首尔
#     1.2.2 A. 亚洲, B. 非洲, C. 欧洲, D. 北美洲
#     1.2.3 A. 氧气, B. 氮气, C. 二氧化碳, D. 氩气
#     1.2.4 A. 鸵鸟, B. 鸭子, C. 鹅, D. 鸡
#     1.2.5 A. 木星, B. 土星, C. 天王星, D. 地球
# 1.3 定义一个正确答案元组answers，其中包括五个元素，分别是：
#     A A B A A
# 1.4 定义一个用户猜测列表guesses，初始化为空列表
# 1.5 定义一个成绩变量score，初始值为0
# 1.6 定义一个问题索引变量question_num，初始值为0

# 2. 问题循环
# 2.1 当question_num小于5时，执行循环
#     2.1.0 输出问题分隔符号“————第{question_num+1}题————”
#     2.1.1 输出和question_num对应的问题
#     2.1.2 输出和question_num对应的四个选项，每个选项占一行
#     2.1.3 获取用户输入的答案，转成大写，
#           如果用户输入的答案不是A、B、C、D中的一个，提示用户重新输入
#     2.1.4 将用户输入的答案添加到guesses列表中
#     2.1.5 如果用户输入的答案等于answers[question_num]，将score加1，并输出“正确！”
#           否则输出“错误！”，并输出正确答案是{answers[question_num]}
#     2.1.6 将question_num加1

# 3. 输出成绩
# 3.1 输出结果分隔符号“————结果————”
# 3.2 打印输出正确答案answers，输出为一行，每个答案之间用空格隔开
# 3.3 打印输出用户猜测guesses，输出为一行，每个答案之间用空格隔开
# 3.4 输出“你的成绩是{score}%分”，注意将score转换为百分数形式
```
