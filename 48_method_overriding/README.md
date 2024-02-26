# 方法重载(method overriding)

```py
# 定义一个Animal类，它有一个run方法
class Animal(object):
    def run(self):
        print('Animal is running...')


# 定义一个Dog类，它继承自Animal类
class Dog(Animal):
    def run(self):
        print('Dog is running...')


# 创建一个Dog类的实例
dog = Dog()
# 调用run方法
dog.run()
```
