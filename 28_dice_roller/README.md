# 掷骰子游戏

```py
import random

# 生成一个1个点的骰子ascii码，通过一个五行元组实现
dice1 = ('+-------+', '|       |', '|   *   |', '|       |', '+-------+')
# 生成一个2个点的骰子ascii码，通过一个五行元组实现
dice2 = ('+-------+', '| *     |', '|       |', '|     * |', '+-------+')
# 生成一个3个点的骰子ascii码，通过一个五行元组实现
dice3 = ('+-------+', '| *     |', '|   *   |', '|     * |', '+-------+')
# 生成一个4个点的骰子ascii码，通过一个五行元组实现
dice4 = ('+-------+', '| *   * |', '|       |', '| *   * |', '+-------+')
# 生成一个5个点的骰子ascii码，通过一个五行元组实现
dice5 = ('+-------+', '| *   * |', '|   *   |', '| *   * |', '+-------+')
# 生成一个6个点的骰子ascii码，通过一个五行元组实现
dice6 = ('+-------+', '| *   * |', '| *   * |', '| *   * |', '+-------+')

# 定义dice_art字典，键为骰子点数，值为骰子的ascii码元组
dice_art = {1: dice1, 2: dice2, 3: dice3, 4: dice4, 5: dice5, 6: dice6}

# 定义一个dice空列表，用于存放用户掷骰子的点数
dice = []
# 定义total，初始化为0
total = 0
# 定义num_of_dice，提示用户：请输入要掷的骰子个数
num_of_dice = int(input('请输入要掷的骰子个数：'))
  # 通过for循环，掷num_of_dice个骰子
for i in range(num_of_dice):
    # 生成一个1到6的随机数，表示骰子点数
    dice.append(random.randint(1, 6))
    # 将骰子点数累加到total
    total += dice[i]

# 通过for循环，打印出掷骰子的结果，要求横向排列，使用两个for循环
for i in range(5):
    for j in range(num_of_dice):
        # 打印出第j个骰子的第i行ascii码
        print(dice_art[dice[j]][i], end=' ')
    # 换行
    print()

# 打印出掷骰子的总点数
print('总点数：', total)
```
