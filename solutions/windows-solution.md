### github

- personal access token for git on command line: [Managing your personal access tokens](https://docs.github.com/en/authentication/keeping-your-account-and-data-secure/managing-your-personal-access-tokens)

a temporary token: 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

#### git on command line

- [提交文件到github的两种方法](https://blog.csdn.net/u013553529/article/details/59144904#:~:text=%E6%96%B9%E6%B3%95%E4%B8%80%EF%BC%9A%E6%9C%AC%E5%9C%B0%E7%9B%AE%E5%BD%95%E6%89%A7%E8%A1%8C%20git%20init%EF%BC%8C%E4%B8%8D%E6%89%A7%E8%A1%8C%20git%20clone%201%20%E6%89%A7%E8%A1%8C%20git,%EF%BC%89%203%20%E6%89%A7%E8%A1%8C%20git%20push%20origin%20main%20%E5%B0%86%E6%9C%AC%E5%9C%B0%E5%B7%A5%E7%A8%8B%E6%8F%90%E4%BA%A4%E5%88%B0github)

#### github加速：fast github

- [『FastGithub』一款.Net开源的稳定可靠Github加速神器，轻松解决GitHub访问难题](https://blog.csdn.net/qq_34202873/article/details/132543478)

- FastGithub for ubuntu chrome: [安装FastGithub从而实现加速github的步骤(Ubuntu)](https://blog.csdn.net/Lambert0320/article/details/132204181)

## technique learning

- [geeksforgeeks](https://www.geeksforgeeks.org/)

## machine learning

- [UC Irvine Machine Learning Repository](https://archive.ics.uci.edu/)



- YOLO

### Mediapipe

- 官网：[Mediapipe](https://developers.google.cn/mediapipe)

应用实例：

- [Python: Hand landmark estimation with MediaPipe](https://techtutorialsx.com/2021/04/10/python-hand-landmark-estimation/)

## windows 10

### windows命令行

- Windows CMD常用命令大全（值得收藏） - 小火龙的文章 - 知乎
  https://zhuanlan.zhihu.com/p/468515490



- 对输出结果进行筛选

```
pip list | find "sci"
```

### windows 10禁用更新

- 唯一无副作用禁用Win10/11更新方法，一键暂停1000周 - 电手的文章 - 知乎
  https://zhuanlan.zhihu.com/p/642914883

### markdown的一些用法

- 花体字母

$$
\mathbb{R} \quad 
\mathcal{R} \quad 
\mathscr{R} \quad 
\mathrm{R} \quad 
\mathbf{R} \quad 
\mathit{R} \quad 
\mathsf{R} \quad 
\mathtt{R} \quad 
\mathfrak{R}
$$

### PDF在线处理网站

- https://smallpdf.com/cn/result#r=67207b39f561989bfb2d9c923280ec83&t=compress

# resources

### 电子书

- z-library: 发送含任意内容的邮件至blackbox@zlib.se即可获得最新网址

### 镜像站

- [清华大学开源软件镜像站](https://mirrors.tuna.tsinghua.edu.cn/)

# python

#### 语法

python的断言功能：

```python
assert(0) # 参数为0时触发断言
```

#### anaconda

- [conda常用命令汇总](https://blog.csdn.net/raelum/article/details/125109819?ops_request_misc=%7B%22request%5Fid%22%3A%22169638859316800180635510%22%2C%22scm%22%3A%2220140713.130102334..%22%7D&request_id=169638859316800180635510&biz_id=0&utm_medium=distribute.pc_search_result.none-task-blog-2~all~top_positive~default-1-125109819-null-null.142%5Ev94%5Einsert_down28v1&utm_term=Conda%E6%8C%87%E4%BB%A4&spm=1018.2226.3001.4187)

conda重命名虚拟环境时，需要复制原有环境并重命名，参考：[anaconda 重命名 虚拟环境、删除环境、复制环境](https://blog.csdn.net/chenran187906/article/details/106900396)

#### pycharm

- [帮助文档](https://www.jetbrains.com/help/pycharm/run-debug-configuration.html)

### python库

#### scipy

- [Py之Scipy：Scipy库(高级科学计算库)的简介、安装、使用方法之详细攻略](https://blog.csdn.net/qq_41185868/article/details/79682406)

#### numpy

- [numpy-菜鸟教程](https://www.runoob.com/numpy/numpy-tutorial.html)

- [NumPy reference](https://numpy.org/doc/stable/reference/index.html)（速度较慢）

#### virtualenv

- [user guide](https://virtualenv.pypa.io/en/latest/user_guide.html)

# 深度学习

- 【[双语字幕]吴恩达深度学习deeplearning.ai】 https://www.bilibili.com/video/BV1FT4y1E74V/?share_source=copy_web&vd_source=c6317e87993cd23a0e65d74c89d6599d

- 【(强推|双字)2022吴恩达机器学习Deeplearning.ai课程】 https://www.bilibili.com/video/BV1Pa411X76s/?p=150&share_source=copy_web&vd_source=c6317e87993cd23a0e65d74c89d6599d

配套资料：

- https://github.com/robbertliu/deeplearning.ai-andrewNG
- [【目录】【中文】【deplearning.ai】【吴恩达课后作业目录】](https://blog.csdn.net/u013733326/article/details/79827273)
- [Deeplearning.ai深度学习教程中文笔记](https://github.com/fengdu78/deeplearning_ai_books)



- 【李沐】动手学深度学习】 https://www.bilibili.com/video/BV18h411r7Z7/?share_source=copy_web&vd_source=c6317e87993cd23a0e65d74c89d6599d

## notes

提高python程序执行效率的方法（尽量避免显式的for-loop）：

1. 向量化
2. 广播

#### 概念

- 过拟合：训练集预测精度提高，测试集预测精度降低

### logistic regression 二分类算法

#### 常用符号表示

$(x,\ y)$：一个训练样本，$x \in R^{n_x}$（$n_x$维向量）， $ y \in \{ 0,\ 1 \}$

$m = m_{train}$：训练样本数量

$m_{test} = \#test$：测试样本数量

$X = [x^{(1)},\ x^{(2)},\ ...,\ x^{(m)}]$：训练集，$X \in R^{n_x \times m}$

$Y = [y^{(1)},\ y^{(2)},\ ...,\ y^{(m)}]$：$Y \in R^{1 \times m}$

#### 算法介绍

模型输出：
$$
a = \hat{y} = \sigma(w^Tx + b) = \sigma(z) \\
z = w^Tx + b
$$
Sigmoid函数：
$$
\sigma(z) = \frac{1}{1 + e^{-z}} \\
\frac{d\sigma(z)}{dz} = \sigma(z)[1 - \sigma(z)]
$$

#### loss & cost function

- loss function: $\mathscr{l}(\hat{y},\ y)$，衡量模型在单个训练样本上的表现


损失函数的设计：避免函数出现多个局部最优值，应使得损失函数为一个凸函数

此处采用的损失函数（交叉熵损失函数）：
$$
\mathscr{l}(\hat{y},\ y) = -(y\ln\hat{y} + (1-y)\ln(1 - \hat{y}))
$$


- cost function（成本函数）：衡量模型在全体训练样本上的表现

$$
J(w,\ b) = \frac{1}{m}\sum_{i=1}^m \mathscr{l}(\hat{y}^{(i)},\ y^{(i)})
$$

==损失函数和成本函数的推导==

给定单个训练样本$(x,\ y)$，则在给定特征$x$的前提下标签$y$出现的概率可表示为：
$$
P(y=1|x) = \hat{y} \\
P(y=0|x) = 1-\hat{y} \\
\Rightarrow P(y|x) = \hat{y}^{y} + (1 - \hat{y})^{1 - y}
$$
在训练时我们希望使$P(y|x)$越大越好，这意味着模型的预测输出越接近实际标签值。

取自然对数：
$$
\ln P(y|x) = y\ln\hat{y} + (1-y)\ln(1 - \hat{y}) = -\mathscr{l}(\hat{y},\ y)
$$
由此得到了loss function: 
$$
\mathscr{l}(\hat{y},\ y) = -(y\ln\hat{y} + (1-y)\ln(1 - \hat{y}))
$$
对于loss function，我们希望它越小越好。

根据概率论中极大似然的概念，令：
$$
P_{labels\ in\ training\ set} = \prod_{i=1}^mP(y^{(i)}|x^{(i)}) \\
\begin{align}
\ln\prod_{i=1}^mP(y^{(i)}|x^{(i)}) &= \sum_{i=1}^m\ln P(y^{(i)}|x^{(i)}) \\
&= -\sum_{i=1}^m \mathscr{l}(\hat{y}^{(i)},\ y^{(i)})
\end{align}
$$
我们的目标是使得$P_{labels\ in\ training\ set}$最大，对应$\sum_{i=1}^m \mathscr{l}(\hat{y}^{(i)},\ y^{(i)})$应取最小值，此外对该式进行适当的缩放即得到cost function: 
$$
J(w,\ b) = \frac{1}{m}\sum_{i=1}^m \mathscr{l}(\hat{y}^{(i)},\ y^{(i)})
$$

#### 梯度下降法 gradient descent

$$
w := w - \alpha\frac{\partial J(w,\ b)}{\partial w} \\
b := b - \alpha\frac{\partial J(w,\ b)}{\partial b}
$$

$\alpha$：学习率

#### 说明

- 其他符号定义

$$
X = [x^{(1)},\ x^{(2)}, ...,\ x^{(m)}]_{n_x \times m} \\
Y = [y^{(1)},\ y^{(2)},\ ...,\ y^{(m)}]_{1 \times m} \\
A = \sigma(w^TX + b) = [a^{(1)},\ a^{(2)},\ ...,\ a^{(m)}]
$$

- 链式求导

<img src="C:\Users\Joker\AppData\Roaming\Typora\typora-user-images\image-20240229204344149.png" alt="image-20240229204344149" style="zoom: 33%;" />

loss function: 
$$
\mathscr{l}(a,\ y) = -(y\log a + (1 - y)\log(1 - a)) \\
\frac{\partial \mathscr{l}(a,\ y)}{\partial a} = -\frac{y}{a} + \frac{1 - y}{1 - a}
$$

$$
\begin{aligned}
\frac{\partial \mathscr{l}(a,\ y)}{\partial z} &= \frac{\partial \mathscr{l}(a,\ y)}{\partial a} \frac{da}{dz} \\
&= (-\frac{y}{a} + \frac{1 - y}{1 - a}) \cdot a(1 - a) \\
&= a - y
\end{aligned}
$$


$$
z = w^Tx + b \\
\frac{\partial z(w,\ b)}{\partial w_{n_x \times 1}} = 
\begin{bmatrix}
\frac{\partial z}{\partial w_1} \\
\frac{\partial z}{\partial w_2} \\
\vdots \\
\frac{\partial z}{\partial w_{n_x}} \\
\end{bmatrix} = 
\begin{bmatrix}
x_1 \\
x_2 \\
\vdots \\
x_{n_x} \\
\end{bmatrix}
= x_{n_x \times 1} (矩阵求导) \\
\quad \frac{\partial z(w,\ b)}{\partial b} = 1
$$

最终求导结果：
$$
\begin{aligned}
\frac{\partial J}{\partial w}|_{n_x \times 1} &= \frac{1}{m}\sum_{i=1}^m [\frac{\partial \mathscr{l}^{(i)}}{\partial z^{(i)}} \frac{\partial z^{(i)}}{\partial w}] \\
&= \frac{1}{m}\sum_{i=1}^m[(a^{(i)} - y^{(i)})_{1 \times 1} \cdot x^{(i)}_{n_x \times 1}] \\
& = \frac{1}{m}X(A - Y)^T_{n_x \times 1} \\

\frac{\partial J}{\partial b} &= \frac{1}{m}\sum_{i=1}^m \frac{\partial \mathscr{l}^{(i)}}{\partial z^{(i)}}\frac{\partial z^{(i)}}{\partial b} \\
&= \frac{1}{m}\sum_{i=1}^m(a^{(i)} - y^{(i)}) \ (标量)
\end{aligned}
$$

#### 注意

- 在代码中使用for循环会显著降低运行速度，应当使用向量化和python广播形式

### 神经网络

#### activation function

- sigmoid（可用于二元分类）: 

$$
\sigma(z) = \frac{1}{1 + e^{-z}} \\
\sigma'(z) = \sigma(z)(1 - \sigma(z))
$$

<img src="C:\Users\Joker\AppData\Roaming\Typora\typora-user-images\image-20240302105107689.png" alt="image-20240302105107689" style="zoom:50%;" />

- tanh: 

$$
tanh(z) = \frac{e^{z} - e^{-z}}{e^{z} + e^{-z}} \\
tanh'(z) = 1 - tanh^2(z)
$$

<img src="C:\Users\Joker\AppData\Roaming\Typora\typora-user-images\image-20240302105145302.png" alt="image-20240302105145302" style="zoom:50%;" />

- ReLU（Rectified Liner Unit，学习速度更快）: 

$$
ReLU(z) = \max(0,\ z) \\
ReLU'(z) = 
\begin{cases}
0,\ z < 0 \\
1,\ z \ge 0
\end{cases}
$$

<img src="C:\Users\Joker\AppData\Roaming\Typora\typora-user-images\image-20240302105202878.png" alt="image-20240302105202878" style="zoom:50%;" />

==注== 编程实现时令$z=0$处的导数为1

- leaky ReLU: 

$$
g(z) = \max(0.01z,\ z) \\
g'(z) = 
\begin{cases}
0.01,\ z < 0 \\
1,\ z \ge 0
\end{cases}
$$

<img src="C:\Users\Joker\AppData\Roaming\Typora\typora-user-images\image-20240302105258320.png" alt="image-20240302105258320" style="zoom:50%;" />

#### forward propogation

以两层网络为例：

<img src="C:\Users\Joker\AppData\Roaming\Typora\typora-user-images\image-20240302101541463.png" alt="image-20240302101541463" style="zoom:50%;" />

- $a^{[l]}_{i}$：activation，表示网络中第$l$层第$i$个神经元的值，且$a^{[0]} = X$
- $a^{[l](i)}$：第$i$个训练样本下第$l$层的值



针对第$i$个样本的前向传播过程：
$$
\begin{aligned}
z^{[1](i)} &= W^{[1]}x^{(i)} + b^{[1]} \\
a^{[1](i)} &= \sigma(z^{[1](i)}) \\
z^{[2](i)} &= W^{[2]}a^{[1](i)} + b^{[2]} \\
a^{[2](i)} &= \sigma(z^{[2](i)})
\end{aligned}
$$

- $x = [x_1,\ x_2,\ x_3]^T$

- $W^{[1]}_{4 \times 3}$：4个隐含层单元，样本含3个特征



前向传播过程-针对样本集的向量化：
$$
\begin{aligned}
Z^{[1]} &= W^{[1]}X + B^{[1]} \\
A^{[1]} &= \sigma(Z^{[1]}) \\
Z^{[2]} &= W^{[2]}A^{[1]} + B^{[2]} \\
A^{[2]} &= \sigma(Z^{[2]})
\end{aligned}
$$

- $X = [x^{(1)},\ x^{(2)},\ ...,\ x^{(m)}]_{n_x \times m} = A^{[0]}$：表示样本集
- $Z^{[1]} = [z^{[1](1)},\ z^{[1](2)},\ ...,\ z^{[1](m)}]$
- $Z^{[2]} = [z^{[2](1)},\ z^{[2](2)},\ ...,\ z^{[2](m)}]$
- $A^{[1]} = [a^{[1](1)},\ a^{[1](2)},\ ...,\ a^{[1](m)}]$
- $A^{[2]} = [a^{[2](1)},\ a^{[2](2)},\ ...,\ a^{[2](m)}]$
- $B^{[1]} = [b^{[1]},\ b^{[1]},\ ...,\ b^{[1]}]_{\_\times m}$

#### back propogation

- $n^{[l]}$：第$l$层的节点数



- $dZ^{[2]} = \frac{\partial J}{\partial Z^{[2]}},\ Z^{[2]}_{1 \times m}(m个样本)$

- $$
  \begin{aligned}
  A^{[2]} &= [A^{[2](1)},\ A^{[2](2)},\ ...,\ A^{[2](m)}] \\
  &= [a^{[2](1)},\ a^{[2](2)},\ ...,\ a^{[2](m)}]_{1 \times m} \\
  \end{aligned}
  $$


$$
\begin{aligned}
dZ^{[2]} &= [dz^{[2](1)},\ dz^{[2](2)},\ ...,\ dz^{[2](m)}] \\
&= [\frac{1}{m}(A^{[2](1)} - )]
\end{aligned}
$$


- $Y = [y^{(1)},\ y^{(2)},\ ...,\ y^{(m)}]_{1 \times m}$
- 第2层输出层只有1个节点，采用sigmoid函数，参考logistic regression部分，有：

$$
\frac{\partial \mathscr{l}}{\partial z} = a - y \\
dz = \frac{\partial J}{\partial z} = \frac{1}{m}\sum_{i=1}^m\frac{\partial \mathscr{l}^{(i)}}{\partial z}
$$



![image-20240302120903407](C:\Users\Joker\AppData\Roaming\Typora\typora-user-images\image-20240302120903407.png)

## pytorch

官网：https://pytorch.org/get-started/locally/

## transformer

# 图像处理

计算机视觉领域可使用的数据集：COCO

参考：[Dataset之COCO数据集：COCO数据集的简介、下载、使用方法之详细攻略](https://blog.csdn.net/qq_41185868/article/details/82939959)

### opencv python

- [Ubuntu下安装opencv-python(详解)](https://blog.csdn.net/weixin_44756050/article/details/104825269)

文档

- 官网教程：[OpenCV-Python Tutorials](https://docs.opencv.org/4.x/d6/d00/tutorial_py_root.html)

- 摄像头参数详解：[Flags for video I/O](https://docs.opencv.org/3.4/d4/d15/group__videoio__flags__base.html) 

### face_recognition

dlib的github官网：https://github.com/davisking/dlib

似乎找不到ubuntu下dlib的.whl文件，可以尝试手动编译安装

- [ubuntu20.04安装Dlib方法](https://zhuanlan.zhihu.com/p/449942621)



- [[已解决]face_recognition库安装，dlib库安装](https://blog.csdn.net/weixin_53236070/article/details/124306424)

## yolo

作者的yolo网页：https://pjreddie.com/darknet/yolov1/



- [YOLO系列算法精讲：从yolov1至yolov8的进阶之路（2万字超全整理）](https://blog.csdn.net/wjinjie/article/details/107509243?ops_request_misc=%257B%2522request%255Fid%2522%253A%2522170901435516800211595559%2522%252C%2522scm%2522%253A%252220140713.130102334..%2522%257D&request_id=170901435516800211595559&biz_id=0&utm_medium=distribute.pc_search_result.none-task-blog-2~all~top_positive~default-1-107509243-null-null.142^v99^pc_search_result_base7&utm_term=yolo&spm=1018.2226.3001.4187)



- 【百万播放】零基础、快速学YOLO目标检测算法！完整学习路线一条龙，无脑通关！【YOLOv5|YOLO算法|目标检测算法】】 https://www.bilibili.com/video/BV1XW4y1a7f4/?p=14&share_source=copy_web&vd_source=c6317e87993cd23a0e65d74c89d6599d

### yolov1

- 【精读AI论文】YOLO V1目标检测，看我就够了】 https://www.bilibili.com/video/BV15w411Z7LG/?share_source=copy_web&vd_source=c6317e87993cd23a0e65d74c89d6599d

### yolov5

yolov5 github: https://github.com/ultralytics/yolov5?tab=readme-ov-file

#### 树莓派部署yolov5

### yolov7

yolov7 github: https://github.com/WongKinYiu/yolov7

## ResNet



















