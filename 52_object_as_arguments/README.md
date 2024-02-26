# 对象作为参数

```py
# 定义一个Car类，它只有一个类变量color，初始化为None。该类没有方法。
class Car:
    color = None


# 定义一个Bike类，它只有一个类变量color，初始化为None。该类没有方法。
class Bike:
    color = None


# 定义一个函数，它的参数是一个Car对象和一个color。函数的功能是将Car对象的color属性设置为传入的color参数。
def change_color(vehicle, color):
    vehicle.color = color


# 创建一个Car对象car1，将它的color属性设置为'red'。
car1 = Car()
change_color(car1, 'red')
print(car1.color)
# 创建一个Car对象car2，将它的color属性设置为'blue'。
car2 = Car()
change_color(car2, 'blue')
print(car2.color)
# 创建一个Car对象car3，将它的color属性设置为'green'。
car3 = Car()
change_color(car3, 'green')
print(car3.color)

# 创建一个Bike对象bike1，将它的color属性设置为'yellow'。
bike1 = Bike()
change_color(bike1, 'yellow')
print(bike1.color)
```
