# 加解密程序

```py
# 导入random和string模块
import random
import string

# 定义一个字符川变量chars，其中包含了所有的大小写字母，数字，标点符号和空格
chars = string.ascii_letters + string.digits + string.punctuation + ' '
# 将chars转换为列表
chars = list(chars)
# 打印chars列表
print('chars列表是：', chars)
# 将chars列表copy一份，保存到变量key中
key = chars.copy()
# 使用random.shuffle()函数打乱key列表中的元素
random.shuffle(key)
# 打印key列表
print('key列表是：  ', key)

# 开始加密
# 请用户输入一个要加密的字符串plain_text
plain_text = input('请输入要加密的字符串：')
# 定义一个空字符串变量cipher_text，用来保存加密后的字符串
cipher_text = ''

# 遍历plain_text中的每一个字符
for c in plain_text:
    # 如果c在chars中
    if c in chars:
        # 获取c在chars中的索引
        index = chars.index(c)
        # 将key[index]添加到cipher_text中
        cipher_text += key[index]

# 输出加密后的字符串
print('加密后的字符串是：', cipher_text)

# 开始解密
# 请用户输入一个要解密的字符串cipher_text
cipher_text = input('请输入要解密的字符串：')
# 定义一个空字符串变量plain_text，用来保存解密后的字符串
plain_text = ''
# 遍历cipher_text中的每一个字符
for c in cipher_text:
    # 如果c在key中
    if c in key:
        # 获取c在key中的索引
        index = key.index(c)
        # 将chars[index]添加到plain_text中
        plain_text += chars[index]

# 输出解密后的字符串
print('解密后的字符串是：', plain_text)
```
