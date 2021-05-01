

# 数据处理

## numpy

numpy是一个运行速度很快的数学库，主要用于数组计算。

1. 一个强大的N维数组对象ndarray(np.array)
2. 广播功能函数
3. 整合C/C++/Fortran代码的工具
4. 线性代数、傅里叶变换、随机数生成等功能

### np.array

```python
# 一维
np.array([1, 2, 3])
# 二维
np.array([[1,  2],  [3,  4]])  
```

### np.dtype

```python
# 类型字段名可以用于存取实际的 age 列
dt = np.dtype([('age',np.int8)]) 
a = np.array([(10,),(20,),(30,)], dtype = dt) 
print(a['age'])
```

### np.arange

```python
import numpy as np
x = np.arange(10, # 起始点，默认值为0
              20, # 终止点，不包含
              2,) # 步长

```

### np.reshape

可以在不改变数据的条件下修改形状

```python
import numpy as np
 
a = np.arange(8)
print ('原始数组：')
print (a)
print ('\n')
"""
[0 1 2 3 4 5 6 7]
"""
 
b = a.reshape(4,2)
print ('修改后的数组：')
print (b)
"""
[[0 1]
 [2 3]
 [4 5]
 [6 7]]
"""
```

### np.random

作用：使得随机数据可预测

#### np.random.seed()

seed（）里的数字就相当于设置了一个盛有随机数的“聚宝盆”，一个数字代表一个“聚宝盆”，当我们在seed（）的括号里设置相同的seed，“聚宝盆”就是一样的，那当然每次拿出的随机数就会相同（不要觉得就是从里面随机取数字，只要设置的seed相同取出地随机数就一样）。如果不设置seed，则每次会生成不同的随机数。（注：seed括号里的数值基本可以随便设置哦）

```python
# 不同seed里面参数不同，实验结果不同；相同参数结果一样
np.random.seed(0)
np.random.rand(10)
Out[357]: 
array([0.5488135 , 0.71518937, 0.60276338, 0.54488318, 0.4236548 ,
       0.64589411, 0.43758721, 0.891773  , 0.96366276, 0.38344152])
# np.random.seed(0)
np.random.rand(10)
Out[358]: 
array([0.79172504, 0.52889492, 0.56804456, 0.92559664, 0.07103606,
       0.0871293 , 0.0202184 , 0.83261985, 0.77815675, 0.87001215])
```



## pandas

# 数据可视化

## matplotlib

