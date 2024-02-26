# 方法级联(method chaining)

```py
# 定义一个Car类，它有四个方法turn_on/drive/brake/turn_off
# 支持级联方法调用
class Car:
    def turn_on(self):
        print('The car is starting')
        return self

    def drive(self):
        print('The car is driving')
        return self

    def brake(self):
        print('The car is braking')
        return self

    def turn_off(self):
        print('The car is stopping')
        return self


# # 创建一个Car对象，然后调用它的四个方法
# car = Car()
# car.turn_on()
# car.drive()
# car.brake()
# car.turn_off()

# 创建一个Car对象，然后调用它的四个方法，使用级联方法调用
car = Car()
car.turn_on()\
 .drive()\
 .brake()\
 .turn_off()
```
