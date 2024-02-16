# 继承(inheritance)

## 在 Python 中，如何实现类继承(inheritance)？[ask_copilot]

```py
# 定义一个类Organism，包含一个alive类变量，缺省值为True
class Organism:
    alive = True


# 定义一个类Animal，继承自Organism，它有一个eat方法
class Animal(Organism):
    def eat(self):
        print('This animal is eating')


# 定义一个类Dog，继承自Animal，它有一个bark方法
class Dog(Animal):
    def bark(self):
        print('This dog is barking')


# 定义一个类Bird，继承自Animal，它有一个fly方法
class Bird(Animal):
    def fly(self):
        print('This bird is flying')


# 创建一个Dog对象
dog = Dog()
# 访问Dog对象的alive类变量
print(dog.alive)
# 调用Dog对象的eat方法
dog.eat()
# 调用Dog对象的bark方法
dog.bark()

# 创建一个Bird对象
bird = Bird()
# 访问Bird对象的alive类变量
print(bird.alive)
# 调用Bird对象的eat方法
bird.eat()
# 调用Bird对象的fly方法
bird.fly()
```
