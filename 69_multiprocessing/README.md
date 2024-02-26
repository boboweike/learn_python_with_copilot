# 多进程(multiprocessing)

```py
# 导入multiprocessing模块的Process类
from multiprocessing import Process
# 导入time模块
import time

# 定义一个counter函数，参数为num，通过while循环从0开始计数，直到num为止
# 该函数用于模拟一个需要大量计算的任务
def counter(num):
    count = 0
    while count < num:
        count += 1


# 定义一个process_func函数，参数为表示进程数量的process_num和表示计数的count_num
# 步骤：
# 1. 计算每个进程需要计数的次数count_num_each = count_num // process_num
# 2. 获取开始时间start_time
# 3. 根据process_num创建进程，每个进程运行counter函数计数count_num_each次
# 4. 等待所有进程结束
# 5. 获取结束时间end_time
# 6. 输出process_num/count_num和运行时间
def process(process_num, count_num):
    count_num_each = count_num // process_num
    start_time = time.time()
    process_list = []
    for i in range(process_num):
        process_list.append(Process(target=counter, args=(count_num_each,)))
    for process_item in process_list:
        process_item.start()
    for process_item in process_list:
        process_item.join()
    end_time = time.time()
    print(f'process_num={process_num}, count_num={count_num}, time={end_time-start_time}')


# 定义一个main函数
# 步骤：
# 1. 定义process_num = 1
# 2. 定义count_num = 100000000
# 3. 调用process函数
def main():
    process_num = 4
    count_num = 100000000
    process(process_num, count_num)


# 判断是否为主模块
if __name__ == '__main__':
    main()
```
