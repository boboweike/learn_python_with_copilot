# 多线程(multithreading)的使用

```py
# 在Python中如何实现多线程编程？
# multithreading和multiprocessing的区别？

# 导入threading和time模块
import threading
import time

# 定义一个eat_breakfast函数，其中睡眠3秒
def eat_breakfast():
    time.sleep(3)
    print('You eat breakfast!')


# 定义一个drink_coffee函数，其中睡眠4秒
def drink_coffee():
    time.sleep(4)
    print('You drank coffee!')


# 定义一个study函数，其中睡眠5秒
def study():
    time.sleep(5)
    print('You finished studying!')

# 获取当前时间存入变量start_time
start_time = time.time()

# # 依次调用eat_breakfast、drink_coffee和study函数
# eat_breakfast()
# drink_coffee()
# study()

# 创建一个线程对象，target参数传入eat_breakfast函数，然后调用start方法启动线程
thread_1 = threading.Thread(target=eat_breakfast)
thread_1.start()
# 创建一个线程对象，target参数传入drink_coffee函数，然后调用start方法启动线程
thread_2 = threading.Thread(target=drink_coffee)
thread_2.start()
# 创建一个线程对象，target参数传入study函数，然后调用start方法启动线程
thread_3 = threading.Thread(target=study)
thread_3.start()

# 使用join方法等待线程结束
thread_1.join()
thread_2.join()
thread_3.join()

# 获取当前时间存入变量end_time
end_time = time.time()

# 打印输出end_time - start_time的值
print(end_time - start_time)


# 打印输出当前活跃的线程数
print(threading.active_count())
# 打印输出当前活跃的线程信息
print(threading.enumerate())
```
