# time 模块

```py
import time

# 什么是epoch时间？
# epoch时间是1970年1月1日0时0分0秒的时间，是计算机中的一种时间表示方式，也称为Unix时间戳


# time.ctime vs time.time
# 获取epoch时间的字符串表示
print(time.ctime(0))

# 获取epoch时间+1000000秒的字符串表示
print(time.ctime(1000000))

# 获取epoch时间到现在所经过的秒数
print(time.time())

# 获取当前时间的字符串表示
# 等价于time.ctime(time.time())
print(time.ctime())

# struct_time对象 -> 日期时间字符串
# 获取当前本地时间的struct_time对象，赋值给time_object
time_object = time.localtime()
print(time_object)

# 将time_object转换为字符串表示，使用time.strftime，格式化字符串为"%B %d %Y %H:%M:%S"
print(time.strftime("%B %d %Y %H:%M:%S", time_object))

# 获取UTC时间的struct_time对象，赋值给time_object
time_object = time.gmtime()

# time.strptime，日期时间字符串 -> struct_time对象
# 定义一个日期字符串time_string，赋值为"June 30 2018 12:00:00"
time_string = "20 April, 2020"
# 将time_string转换为struct_time对象，使用time.strptime
time_object = time.strptime(time_string, "%d %B, %Y")
print(time_object)

# time.asctime和time.mktime
# 定义一个time_tuple，格式为(year, month, day, hours, minutes, seconds, #day of week, #day of the year, daylight_saving_flag)
time_tuple = (2020, 4, 20, 12, 0, 0, 0, 0, 0)
# 使用asctime，将time_tuple转换为字符串表示
print(time.asctime(time_tuple))
# 使用mktime，将time_tuple转换为epoch时间
print(time.mktime(time_tuple))
```
