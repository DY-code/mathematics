#### pip

常用命令：

- `pip show`：展示已安装包的信息，如：

```
pip show scipy
```

#### anaconda

- [conda常用命令汇总](https://blog.csdn.net/raelum/article/details/125109819?ops_request_misc=%7B%22request%5Fid%22%3A%22169638859316800180635510%22%2C%22scm%22%3A%2220140713.130102334..%22%7D&request_id=169638859316800180635510&biz_id=0&utm_medium=distribute.pc_search_result.none-task-blog-2~all~top_positive~default-1-125109819-null-null.142%5Ev94%5Einsert_down28v1&utm_term=Conda%E6%8C%87%E4%BB%A4&spm=1018.2226.3001.4187)

conda重命名虚拟环境时，需要复制原有环境并重命名，参考：[anaconda 重命名 虚拟环境、删除环境、复制环境](https://blog.csdn.net/chenran187906/article/details/106900396)



- 安装jupyter notebook

在新创建的python虚拟环境中默认没有安装jupyter notebook（base环境可以使用），可以使用以下命令安装：

```
conda install nb_conda_kernels
```

在命令行中打开jupyter notebook可使用如下命令：

```
jupyter notebook
```

#### pycharm

- [帮助文档](https://www.jetbrains.com/help/pycharm/run-debug-configuration.html)

#### jupyter notebook

###### 魔法函数

```
%lsmagic  # 列出所有魔法函数
%matplotlib inline  # 绘图内嵌
```

参考：[Jupyter中的魔法函数](https://zhuanlan.zhihu.com/p/142942524)

### python库

#### pandas

文档：https://pandas.pydata.org/pandas-docs/stable/reference/frame.html



- dataframe的数据类型转换

```python
df = df.astype('float32')
```

参考：[pandas的dataframe如何更改数据类型？](https://blog.csdn.net/Python_Ai_Road/article/details/81158376)

#### matplotlib

- [API Reference](https://matplotlib.org/stable/api/index.html)

- `matplotlib.pyplot`: https://matplotlib.org/stable/api/pyplot_summary.html



- 在x=0, y=0处画线形成十字

```python
# 绘制水平线
plt.axhline(0, color='black', linestyle='--')
# 绘制垂直线
plt.axvline(0, color='black', linestyle='--')
```

参考：[python 在x=0,y=0处画线形成十字](https://blog.csdn.net/baishuiniyaonulia/article/details/121099621)

- 指定两坐标轴的比例相同

```python
plt.axis("equal")
```

参考：

- https://matplotlib.org/stable/api/_as_gen/matplotlib.pyplot.axis.html
- [【matplotlib】可视化解决方案——如何正确设置轴长度和范围](https://blog.csdn.net/pcx171/article/details/130406896)

#### scipy

- [Py之Scipy：Scipy库(高级科学计算库)的简介、安装、使用方法之详细攻略](https://blog.csdn.net/qq_41185868/article/details/79682406)

#### numpy

- [numpy-菜鸟教程](https://www.runoob.com/numpy/numpy-tutorial.html)

- [NumPy reference](https://numpy.org/doc/stable/reference/index.html)（速度较慢）



```python
np.multiply() # 各元素分别相乘
```



###### numpy计算矩阵的逆

```python
import numpy as np

a  = np.array([[1, 2], [3, 4]])  # 初始化一个非奇异矩阵(数组)
print(np.linalg.inv(a))  # 对应于MATLAB中 inv() 函数

# 矩阵对象可以通过 .I 更方便的求逆
A = np.matrix(a)
print(A.I)
```

参考：[Numpy 中的矩阵求逆](https://blog.csdn.net/xienan_ds_zj/article/details/86738316)

###### numpy计算方差：`ndarray.var()`

`ndarray.var()`的计算公式（无参数，ddof=0）：
$$
D(X) = \frac{1}{n}\sum_{i=1}^n (x_i - \overline{x})^2
$$
`ndarray.var(ddof=1)`的计算公式：
$$
D(X) = \frac{1}{n-1}\sum_{i=1}^n (x_i - \overline{x})^2
$$

###### numpy计算协方差：`numpy.cov()`的计算过程细节

```python
import numpy as np
X = np.array([5674.68, 5699.83, 5631.67])
Y = np.array([426.676, 433.312, 440.343])
data = np.vstack([X, Y])

# np.cov()的具体计算过程
mean_val = data.mean(axis=1, keepdims=True)
data1 = data - mean_val
cov2 = 1/2 * np.dot(data1, data1.T)
print(cov2)

# data:每一列表示一个样本，一行对应一个属性
# 两个输出结果一致
print(np.cov(data))

# 协方差的计算公式
X_mean = X.mean()
Y_mean = Y.mean()
my_cov = np.multiply(X-X_mean, Y-Y_mean).sum() / 2
# 结果与c_01一致
print(my_cov)
```

协方差的计算公式：
$$
cov(x,\ y) = \frac{1}{n-1}\sum_{i=1}^n(x_i - \overline{x})(y_i - \overline{y})
$$
参考：[协方差矩阵计算方法](https://blog.csdn.net/blackyuanc/article/details/100703888#:~:text=%E5%8D%8F%E6%96%B9%E5%B7%AE%E7%9F%A9%E9%98%B5%E8%AE%A1%E7%AE%97%E6%96%B9%E6%B3%95%201%201.%20%E5%8D%8F%E6%96%B9%E5%B7%AE%E7%9F%A9%E9%98%B5%20X%2CY%20%E6%98%AF%E4%B8%A4%E4%B8%AA%E9%9A%8F%E6%9C%BA%E5%8F%98%E9%87%8F%EF%BC%8C%20X%2CY%20%E7%9A%84%E5%8D%8F%E6%96%B9%E5%B7%AE,m%20p%3B%201%20a%20m%20p%3B%201%5D%20)

==注== 自身的协方差 = 自身的方差

#### virtualenv

- [user guide](https://virtualenv.pypa.io/en/latest/user_guide.html)

#### os

文档：https://docs.python.org/3/library/os.html

- `os.path.join()`: 将多个路径拼接起来

参考：https://www.geeksforgeeks.org/python-os-path-join-method/

## 语法

### 魔法函数

- `__name__`：当前模块（文件）的名称，当该模块被直接运行时，`__name == __main__`

参考：if __name__ == '__main__' 如何正确理解? - 初识CV的回答 - 知乎
https://www.zhihu.com/question/49136398/answer/1654722335

### 字符串

- formatted string literals（格式化字符串文字）: `f"..."`

适用于python3.6及以上，示例：

```python
>>> name = "Fred"
>>> f"his name is {name}"
'his name is Fred'
```

参考：[What is print(f"...")](https://stackoverflow.com/questions/57150426/what-is-printf)

### python类的构造和使用

参考：https://www.runoob.com/python/python-object.html



##### python类的一些内置函数

###### 类对象的调用：`__call__`

示例：

```python
class Person:
    def __call__(self, name):
        print("__call__: " + name)
        
person = Person()
person("Fred")
# 输出结果：__call__: Fred
```

###### 索引符号重载

```python 
object[key] <==> object.__getitem__(key)
```

与之相似的还有`__setitem__`、`__delitem__`，详细用法参考：[How to implement __getitem__, __setitem__, and __delitem__ in Python](https://geekpython.in/implement-getitem-setitem-and-delitem-in-python)

## 其他

python的断言功能：

```python
assert(0) # 参数为0时触发断言
```































 
