# 抽象类和抽象方法

```py
# 定义一个类Vehicle
class Vehicle:
    def run(self):
        pass


# 定义一个类Car，继承Vehicle
class Car(Vehicle):
    def run(self):
        print('小汽车在行驶')


# 定义一个类Bike，继承Vehicle
class Bike(Vehicle):
    def run(self):
        print('自行车在行驶')


# 创建一个Vehicle对象
vehicle = Vehicle()
# 调用run方法
vehicle.run()

# 创建一个Car对象
car = Car()
# 调用run方法
car.run()

# 创建一个Bike对象
bike = Bike()
# 调用run方法
bike.run()
```
