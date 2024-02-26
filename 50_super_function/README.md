# 调用 super 方法

```py
# 定义一个Rectangle类
class Rectangle:
    pass

# 定义一个Square类，继承Rectangle类,
# 它有两个属性，一个长度length，一个宽度width
# 它有一个方法，计算面积area
class Square(Rectangle):
    def __init__(self, length, width):
        self.length = length
        self.width = width

    def area(self):
        return self.length * self.width

# 定义一个Cube类，继承Square类
# 它有三个属性，一个长度length，一个宽度width，一个高度height
# 它有一个方法，计算体积volume
class Cube(Square):
    def __init__(self, length, width, height):
        super().__init__(length, width)
        self.height = height

    def volume(self):
        return self.length * self.width * self.height


# 创建一个Square对象
s = Square(3, 4)
# 调用area方法
print(s.area())

# 创建一个Cube对象
c = Cube(3, 4, 5)
# 调用volume方法
print(c.volume())
```
