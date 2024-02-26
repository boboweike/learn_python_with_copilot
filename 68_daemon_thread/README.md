# 守护(daemon)线程

```py
import time
import threading


def timer():
    print()
    print()
    count = 0
    while True:
        time.sleep(1)
        count += 1
        print('已登录 ', count, ' 秒')


# 定义一个线程t, 它执行timer函数
t = threading.Thread(target=timer)
t.start()

# # 定义一个守护线程d, 它是timer的守护线程
# d = threading.Thread(target=timer, daemon=True)
# d.start()

answer = input('要退出吗？(Y/y退出)')
```
