# Duck Typing

```py
# 定义一个Duck类，它有两个方法：walk和talk
class Duck:
    def walk(self):
        print("Duck is walking")
    def talk(self):
        print("Duck is talking")


# 定义一个Chicken类，它有两个方法：walk和talk
class Chicken:
    def walk(self):
        print("Chicken is walking")
    def talk(self):
        print("Chicken is talking")


# 定义一个Person类，它有一个方法：catch
class Person:
    def catch(self, duck):
        duck.walk()
        duck.talk()
        print("I caught the critter!")


# 创建一个Duck对象
duck = Duck()
# 创建一个Chicken对象
chicken = Chicken()
# 创建一个Person对象
person = Person()
# 调用Person对象的catch方法，传入Duck对象
person.catch(duck)
# 调用Person对象的catch方法，传入Chicken对象
person.catch(chicken)
```
