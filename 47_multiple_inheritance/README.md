# 多继承(multiple inheritance)

```py
# 定义一个被捕食者Prey类，它有一个逃跑flee方法
class Prey:
    def flee(self):
        print("This is Prey.flee()")


# 定义一个捕食者Predator类，它有一个捕食hunt方法
class Predator:
    def hunt(self):
        print("This is Predator.hunt()")


# 定义一个兔子Rabbit类，它继承了Prey类
class Rabbit(Prey):
    pass


# 定义一个鱼类Fish，它继承了Prey和Predator类
class Fish(Prey, Predator):
    pass


# 定义一个狼类Wolf，它继承了Predator类
class Wolf(Predator):
    pass


# 分别定义一个兔子对象，一个鱼对象，一个狼对象
rabbit = Rabbit()
fish = Fish()
wolf = Wolf()


# 调用兔子对象的flee方法
rabbit.flee()
# 调用鱼对象的flee方法
fish.flee()
# 调用鱼对象的hunt方法
fish.hunt()
# 调用狼对象的hunt方法
wolf.hunt()
```
