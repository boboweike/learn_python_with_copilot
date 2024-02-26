# 字典推导式(dictionary comprehension)

```py
# 定义一个字典cities_in_F，包含5个城市的华氏温度
cities_in_F = {'New York': 32,
               'Boston': 75,
               'Los Angeles': 100,
               'Chicago': 50,
               'Seattle': 80}

# 使用字典推导式将华氏温度转换为摄氏温度，使用round函数保留小数点后两位
cities_in_C = {key: round((value - 32) * 5 / 9, 2) for key, value in cities_in_F.items()}
# 输出转换后的摄氏温度
print(cities_in_C)


# 定义一个字典weather，包含5个城市的天气情况
weather = {'New York': 'snowing',
           'Boston': 'sunny',
           'Los Angeles': 'sunny',
           'Chicago': 'cloudy',
           'Seattle': 'rainy'}

# 使用字典推导式过滤出天气情况为晴天的城市
sunny_weather = {key: value for key, value in weather.items() if value == 'sunny'}
# 输出天气情况为晴天的城市
print(sunny_weather)


# 定义一个字典cities，包含5个城市的华氏温度
cities = {'New York': 32,
          'Boston': 75,
          'Los Angeles': 100,
          'Chicago': 50,
          'Seattle': 80}


# 使用字典推导式将华氏温度转为"WARN"(>=40)或者"COLD"(<40)
temperature = {key: 'WARM' if value >= 40 else 'COLD' for key, value in cities.items()}
# 输出转换后的温度
print(temperature)


# 定义一个函数temp，接收一个华氏温度，
# 返回"HOT"(>=70)、"WARM"(>=40 & <=69)或者"COLD"(<40)
def temp(f):
    if f >= 70:
        return 'HOT'
    elif f >= 40:
        return 'WARM'
    else:
        return 'COLD'


# 使用字典推导式将华氏温度通过temp函数转换为对应的气温
temperature = {key: temp(value) for key, value in cities.items()}
# 输出转换后的温度
print(temperature)
```
