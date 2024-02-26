# `if __name__ == '__main__'`

## 1. 运行 module_one.py

```py
# 打印输出__name__
print(__name__)

# 导入module_two模块
import module_two

# 打印输出module_two.__name__
print(module_two.__name__)
```

## 2. 运行 module_two.py

```py
# 打印输出__name__
print(__name__)

# 导入module_one模块
import module_one

# 打印输出module_two.__name__
print(module_one.__name__)
```

## 3. 运行 module_one.py

```py
# 如果这是一个独立的程序，那么就输出：直接运行这个模块
# 否则，输出：被其他模块导入
if __name__ == "__main__":
    print("直接运行这个模块")
else:
    print("被其他模块导入")
```

## 4. 运行 module_two.py

```py
# 导入module_one模块
import module_one
```

## 5. 运行 module_one.py

```py
# 定义一个函数main，输出：这是main函数
def main():
    print("这是main函数")


# 如果这是一个独立的程序，那么就执行main函数
# 否则，不执行
if __name__ == "__main__":
    main()
```

## 6. 运行 module_two.py

```py
# 导入module_one模块
import module_one
```
