# 面向对象编程

## 在 Python 中，如何定义类？如何创建类实例？如何调用实例方法？[ask_copilot]

## 创建 Car 类

```py
# 定义一个类Car
# 该类包含4个属性：make、model、year、color
# 该类包含两个方法：drive()、stop()

class Car:
    def __init__(self, make, model, year, color):
        self.make = make
        self.model = model
        self.year = year
        self.color = color
        self.odometer_reading = 0

    def drive(self):
        print("The car is moving.")

    def stop(self):
        print("The car has stopped.")
```

## 创建 Car 实例和调用方法

```py
# 导入car中的Car类
from car import Car

# 创建一个Car实例car1
car1 = Car('audi', 'a4', 2016, 'blue')
# 创建一个Car实例car2
car2 = Car('bmw', 'm3', 2015, 'red')

# 访问car1的属性
print(car1.make)
print(car1.model)
print(car1.year)
print(car1.color)

# 调用car1的drive()方法
car1.drive()
# 调用car1的stop()方法
car1.stop()

# 调用car2的drive()方法
car2.drive()
# 调用car2的stop()方法
car2.stop()
```
