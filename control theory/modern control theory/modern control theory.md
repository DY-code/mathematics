考试题型：![image-20231122194832408](C:\Users\Joker\AppData\Roaming\Typora\typora-user-images\image-20231122194832408.png)

# 填空&简答

## 简答题

### 试说明线性变换不改变线性系统的传递函数

![image-20231124161335497](C:\Users\Joker\AppData\Roaming\Typora\typora-user-images\image-20231124161335497.png)

- 矩阵逆运算的性质：

$$
(ABC)^{-1} = C^{-1}B^{-1}A^{-1}
$$

### 简述对偶原理，对偶系统的传递函数矩阵有什么联系？

对偶原理：

![image-20231124161639707](C:\Users\Joker\AppData\Roaming\Typora\typora-user-images\image-20231124161639707.png)

对偶系统的[传递函数矩阵互为转置]()

### 什么是最小实现？对于一个实现，其为最小实现的充分必要条件是什么？

![image-20231124164304270](C:\Users\Joker\AppData\Roaming\Typora\typora-user-images\image-20231124164304270.png)

### 试写出采用[凯莱-哈密顿定理]()求状态转移矩阵的具体步骤

<img src="C:\Users\Joker\AppData\Roaming\Typora\typora-user-images\image-20231124165822139.png" alt="image-20231124165822139" style="zoom:67%;" />

### 对于一个线性系统，如何判断系统状态反馈可镇定？

<img src="C:\Users\Joker\AppData\Roaming\Typora\typora-user-images\image-20231124172151432.png" alt="image-20231124172151432" style="zoom:67%;" />

## 试题参考

- [天津大学2022~2023现代控制理论期末考试](https://blog.csdn.net/m0_53253879/article/details/128191318)
- [百度文库试题](https://wenku.baidu.com/view/e9837f69bd1e650e52ea551810a6f524ccbfcbfa.html?_wkts_=1700812464569)
- https://max.book118.com/html/2018/1018/8006035073001127.shtm
- 24哈工大控制工程考研 | 《现代控制理论》典型习题梳理（二） - 研当当的文章 - 知乎
  https://zhuanlan.zhihu.com/p/659627386

# 第1章 控制系统的状态空间表达式

## 状态变量及状态空间表达式

- 单输入-单输出系统：

![image-20230916172143298](C:\Users\Joker\AppData\Roaming\Typora\typora-user-images\image-20230916172143298.png)

- 多输入-多输出系统：

![image-20230909095517666](C:\Users\Joker\AppData\Roaming\Typora\typora-user-images\image-20230909095517666.png)

## 状态变量及状态空间表达式的模拟结构图

### 框图绘制步骤

![image-20230909095836027](C:\Users\Joker\AppData\Roaming\Typora\typora-user-images\image-20230909095836027.png)

==注意== 习惯上一般将各状态分量对应的积分器从左到右按倒序排列，如下图示例所示，$x_3$在最左侧，$x_1$在最右侧，输入$u$一般放在左侧，输出$y$放在右侧：

<img src="C:\Users\Joker\AppData\Roaming\Typora\typora-user-images\image-20231124205810182.png" alt="image-20231124205810182" style="zoom:67%;" />

## 状态变量及状态空间表达式的建立（一）

### 由系统框图建立状态空间表达式

步骤：

![image-20230916201439716](C:\Users\Joker\AppData\Roaming\Typora\typora-user-images\image-20230916201439716.png)

==注意== 通常一个积分器的输出对应一个状态变量

==常用转换==
$$
\frac{K}{Ts + 1} = \frac{K}{T} \cdot \frac{s^{-1}}{1 + \frac{1}{T}s^{-1}}
$$

对比闭环系统传递函数：
$$
\varphi(s) = \frac{G}{1 + GH}
$$
则有：
$$
G = \frac{1}{s} \\
H = \frac{1}{T}
$$

### 由系统机理建立状态空间表达式

## 状态变量及状态空间表达式的建立（二）

实现问题：由描述系统输入-输出动态关系的运动方程式或传递函数，建立系统的状态空间表达式。

考虑单变量线性定常系统：
$$
y^{(n)} + a_{n - 1}y^{(n - 1)} + ... + a_1\dot{y} + a_0y \\
= b_mu^{(m)} + b_{m - 1}u^{(m - 1)} + ... + b_1\dot{u} + b_0u
$$
传递函数：
$$
W(s) = \frac{Y(s)}{U(s)} = \frac{b_ms^m + b_{m - 1}s^{m - 1} + ... + b_1s + b_0}{s^n + a_{n - 1}s^{n - 1} + ... + a_1s + a_0} \\
m \le n （可认为m = n）
$$

### 传递函数中没有零点时的实现 ==记忆==

$$
\begin{bmatrix}
\dot{x}_1 \\
\dot{x}_2 \\
\vdots \\
\dot{x}_{n - 1} \\
\dot{x}_n \\
\end{bmatrix} = 
\begin{bmatrix}
0 & 1 & 0 & \dots & 0 \\
0 & 0 & 1 & \dots & 0 \\
\vdots & \vdots & \vdots & \ddots & \vdots \\
0 & 0 & 0 & \dots & 1 \\
-a_0 & -a_1 & -a_2 & \dots & -a_{n - 1} \\
\end{bmatrix}
\begin{bmatrix}
x_1 \\
x_2 \\
\vdots \\
x_{n - 1} \\
x_n \\
\end{bmatrix} + 
\begin{bmatrix}
0 \\
0 \\
\vdots \\
0 \\
1 \\
\end{bmatrix} u
$$

$$
y = 
\begin{bmatrix}
b_0 & 0 & 0 & \dots & 0 
\end{bmatrix}
\begin{bmatrix}
x_1 \\
x_2 \\
\vdots \\
x_{n - 1} \\
x_n \\
\end{bmatrix}
$$

### 传递函数中有零点时的实现

#### 实现方法1 ==记忆==

$$
\begin{bmatrix}
\dot{x}_1 \\
\dot{x}_2 \\
\vdots \\
\dot{x}_{n - 1} \\
\dot{x}_n \\
\end{bmatrix} = 
\begin{bmatrix}
0 & 1 & 0 & \dots & 0 \\
0 & 0 & 1 & \dots & 0 \\
\vdots & \vdots & \vdots & \ddots & \vdots \\
0 & 0 & 0 & \dots & 1 \\
-a_0 & -a_1 & -a_2 & \dots & -a_{n - 1} \\
\end{bmatrix}
\begin{bmatrix}
x_1 \\
x_2 \\
\vdots \\
x_{n - 1} \\
x_n \\
\end{bmatrix} + 
\begin{bmatrix}
0 \\
0 \\
\vdots \\
0 \\
1 \\
\end{bmatrix} u
$$

$$
y = 
\begin{bmatrix}
(b_0 - a_0b_n) & 
(b_1 - a_1b_n) & 
\dots &
(b_{n - 1} - a_{n - 1}b_n)
\end{bmatrix}
\begin{bmatrix}
x_1 \\
x_2 \\
\vdots \\
x_{n - 1} \\
x_n \\
\end{bmatrix} + b_n u
$$

#### 实现方法2（等效思想）

$$
\begin{bmatrix}
\dot{x}_1 \\
\dot{x}_2 \\
\vdots \\
\dot{x}_{n - 1} \\
\dot{x}_n \\
\end{bmatrix} = 
\begin{bmatrix}
0 & 1 & 0 & \dots & 0 \\
0 & 0 & 1 & \dots & 0 \\
\vdots & \vdots & \vdots & \ddots & \vdots \\
0 & 0 & 0 & \dots & 1 \\
-a_0 & -a_1 & -a_2 & \dots & -a_{n - 1} \\
\end{bmatrix}
\begin{bmatrix}
x_1 \\
x_2 \\
\vdots \\
x_{n - 1} \\
x_n \\
\end{bmatrix} + 
\begin{bmatrix}
\beta_{n - 1} \\
\beta_{n - 2} \\
\vdots \\
\beta_1 \\
\beta_0 \\
\end{bmatrix} u
$$

$$
y = 
\begin{bmatrix}
1 & 0 & 0 & \dots & 0
\end{bmatrix}
\begin{bmatrix}
x_1 \\
x_2 \\
\vdots \\
x_{n - 1} \\
x_n \\
\end{bmatrix} + \beta_nu
$$

$$
\begin{bmatrix}
1 \\
a_{n - 1} & 1 \\
a_{n - 2} & a_{n - 1} & 1 \\
\vdots & \vdots & \ddots & \ddots \\
a_0 & a_1 & \dots & a_{n - 1} & 1
\end{bmatrix}
\begin{bmatrix}
\beta_{n} \\
\beta_{n - 1} \\
\beta_{n - 2} \\
\vdots \\
\beta_{0} \\
\end{bmatrix} = 
\begin{bmatrix}
b_{n} \\
b_{n - 1} \\
b_{n - 2} \\
\vdots \\
b_{0} \\
\end{bmatrix}
$$

### 多输入-多输出系统微分方程的实现

见第一章PPT62

### 系统的并联型实现

已知系统传递函数：
$$
W(s) = \frac{c_1}{s - \lambda_1} + \frac{c_2}{s - \lambda_2} + ... + \frac{c_n}{s - \lambda_n} = \sum_{i = 1}^n \frac{c_i}{s - \lambda_i}
$$
其模拟结构图如下：

<img src="C:\Users\Joker\AppData\Roaming\Typora\typora-user-images\image-20231014112831601.png" alt="image-20231014112831601" style="zoom:50%;" /><img src="C:\Users\Joker\AppData\Roaming\Typora\typora-user-images\image-20231014112848373.png" alt="image-20231014112848373" style="zoom:50%;" />

对应的状态空间表达式：
$$
\dot{x} = 
\begin{pmatrix}
\lambda_1 & 0 & \dots & 0 \\
0 & \lambda_2 & \dots & 0 \\
\vdots & \vdots & \ddots & \vdots \\
0 & 0 & \dots & \lambda_n
\end{pmatrix} x + 
\begin{pmatrix}
1 \\
1 \\
\vdots \\
1
\end{pmatrix}u \\
y = (c_1,\ c_2,\ ...,\ c_n)x
$$
或：
$$
\dot{x} = 
\begin{pmatrix}
\lambda_1 & 0 & \dots & 0 \\
0 & \lambda_2 & \dots & 0 \\
\vdots & \vdots & \ddots & \vdots \\
0 & 0 & \dots & \lambda_n
\end{pmatrix} x + 
\begin{pmatrix}
c_1 \\
c_2 \\
\vdots \\
c_n
\end{pmatrix}u \\
y = (1,\ 1,\ ...,\ 1)x
$$

## 状态矢量的线性变换（坐标变换）

- 状态的非奇异线性变换不改变系统的能控性和能观性

### 系统状态空间表达式的非唯一性

### 系统特征值的不变性及系统的不变量

#### 系统特征值

系统特征值即系统矩阵A的特征值，即特征方程：
$$
| \lambda I - A | = 0
$$
的根。

#### 系统的不变量与特征值的不变性

系统的不变量：特征多项式的系数
$$
| \lambda I - A | = \lambda^n + a_{n-1}\lambda^{n-1} + ... + a_1\lambda + a_0 = 0
$$

#### 特征矢量

设$\lambda_i$为系统的一个特征值，若存在一个$n$维非零矢量$p_i$满足：
$$
Ap_i = \lambda_ip_i
$$
则称矢量$p_i$为系统对应于特征值$\lambda_i$的特征矢量。

==注== 特征矢量的求法，见第一章PPT76

### 1.5.3 状态空间表达式变换为约旦标准形

$$
\begin{cases}
\dot{x} = Ax + Bu \\
y = Cx
\end{cases}
\stackrel{x = Tz}{===\Rightarrow}
\begin{cases}
\dot{z} = Jz + T^{-1}Bu \\
y = CTz
\end{cases}
\ (J = T^{-1}AT)
$$

#### 约旦标准形矩阵

- 无重根：对角线型

$$
\begin{aligned}
J &= T^{-1}AT \\
&= 
\begin{bmatrix}
\lambda_1 & 0 & \dots & 0 \\
0 & \lambda_2 & \dots & 0 \\
\vdots & \vdots & \ddots & \vdots \\
0 & 0 & \dots & \lambda_n
\end{bmatrix}
\end{aligned}
$$

- 有重根（$q$个重根$\lambda_1$）：约旦块型

$$
J = 
\begin{bmatrix}
\lambda_1 & 1 & \dots & 0 \\
0 & \lambda_1 & \ddots & \vdots & & 0 \\
\vdots & \vdots & \ddots & 1 \\
0 & 0 & \dots & \lambda_1 \\
& & & & \lambda_{q + 1} & 0 & 0 \\
& 0 & & & 0 & \ddots & 0 \\
& & & & 0 & 0 & \lambda_n
\end{bmatrix}
$$

==注== 

- 二阶矩阵逆的求法

$$
T = 
\begin{bmatrix}
a & b \\
c & d
\end{bmatrix} \\
T^{-1} = \frac{T^*}{|T|}
= \frac{1}{ad - bc}
\begin{bmatrix}
d & -b \\
-c & a
\end{bmatrix}
$$

- 伴随矩阵的计算

==定义== 行列式$\vert A \vert$的各个元素的代数余子式$A_{ij}$所构成的如下矩阵：
$$
A^* = 
\begin{pmatrix}
A_{11} & A_{21} & \dots & A_{n1} \\
A_{12} & A_{22} & \dots & A_{n2} \\
\dots & \dots & \dots & \dots \\
A_{1n} & A_{2n} & \dots & A_{nn} \\
\end{pmatrix}
$$
称为矩阵A的伴随矩阵（[注意其中元素的顺序]()，存在一个转置操作）

余子式：元素$a_{ij}$对应的余子式$M_{ij}$为矩阵[删去第$i$行第$j$列后的行列式]()。

代数余子式：设n阶行列式$|A|$元素$(i,j)$的余子式为$M_{ij}$，则对应的代数余子式为：
$$
A_{ij} = (-1)^{i + j}M_{ij}
$$

#### ==约旦标准形变换矩阵T的求法==

约旦标准形变换矩阵$T$ = 系统矩阵$A$的特征矢量组成的矩阵

##### A的特征值无重根

1. 求A的n个互异特征根$\lambda_i$
2. 求$\lambda_i$的特征矢量$P_i$：$\lambda_iP_i - AP_i = 0$
3. $T = (P_1, P_2, ..., P_n)$

##### A的特征值有重根

对应$q$个$\lambda_1$重根的各向量$P_1, ..., P_n$的求法：
$$
\begin{cases}
\lambda_1P_1 - AP_1 = 0 \\
\lambda_1P_2 - AP_2 = -P_1 \\
\dots \\
\lambda_1P_q - AP_q = -P_{q - 1} \\
\end{cases}
$$
$P_1$仍为$\lambda_1$对应的特征矢量，$P_2, ..., P_n$称为**广义特征矢量**。

## 从状态空间表达式求传递函数阵

### 传递函数（阵）

#### 单输入-单输出系统

- 输入-状态

$$
W_{ux}(s) = \frac{X(s)}{U(s)} = (sI - A)^{-1}b
$$

==注意== 此处得到的输入-状态传递函数为一个[列向量]()，注意与下面输入-输出传递函数之间的区别

- 输入-输出

$$
W(s) = \frac{Y(s)}{U(s)} = c(sI - A)^{-1}b + d
$$

#### 多输入-多输出系统

- 输入-状态

$$
W_{ux}(s) = \frac{X(s)}{U(s)} = (sI - A)^{-1}B
$$

- 输入-输出

$$
\begin{aligned}
W(s) &= \frac{Y(s)}{U(s)} \\ 
&= C(sI - A)^{-1}B + D \\
&= [W_{ij}(s)]
\end{aligned}
$$

$W_{ij}(s)$：第j个输入对第i个输出的传递关系

==注== 同一系统，状态空间表达式不唯一，但传递函数阵不变

### 子系统在各种连接时的传递函数阵

- 并联

![image-20231124170651411](C:\Users\Joker\AppData\Roaming\Typora\typora-user-images\image-20231124170651411.png)
$$
W(s) = W_1(s) \pm W_2(s)
$$

- 串联

![image-20231124170715859](C:\Users\Joker\AppData\Roaming\Typora\typora-user-images\image-20231124170715859.png)
$$
W(s) = W_2(s) \cdot W_1(s)
$$
==注意== 传递函数中$W_1(s),\ W_2(s)$的先后次序 和 在结构图中的先后次序是[相反]()的。

- 反馈 

![image-20231124170742671](C:\Users\Joker\AppData\Roaming\Typora\typora-user-images\image-20231124170742671.png)
$$
\begin{aligned}
W(s) &= W_1(s)[I + W_2(s)W_1(s)]^{-1} \\
&= [I + W_1(s)W_2(s)]^{-1}W_1(s)
\end{aligned}
$$
==注== 类比典型反馈系统的传递函数形式：
$$
w(s) = \frac{G}{1 + GH}
$$

# 第2章 状态空间表达式的解

## 2.1 线性定常齐次状态方程的解（自由解）

系统的自由解：系统输入为零时，由初始状态引起的自由运动，此时状态方程为：
$$
\dot{x} = Ax \\
初始状态：x(t_0) = x_0
$$
该式有唯一确定解：
$$
x(t) = e^{A(t - t_0)}x_0,\ t \ge t_0
$$

## 矩阵指数函数-状态转移矩阵

### 状态转移矩阵

### 状态转移矩阵（矩阵指数函数）的基本性质

### 几个特殊的矩阵指数函数

#### 1. $A$为对角线矩阵

$$
A = \varLambda = 
\begin{bmatrix}
\lambda_1 & & 0 \\
& \ddots & \\
0 & & \lambda_n
\end{bmatrix} \\
e^{At} = \varPhi(t) = 
\begin{bmatrix}
e^{\lambda_1t} & & 0 \\
& \ddots \\
0 & & e^{\lambda_nt}
\end{bmatrix}
$$

#### 2. $A$能通过非奇异变换对角线化

$A$的对角化：$T^{-1}AT = \varLambda$，则
$$
e^{At} = \varPhi(t) = 
T
\begin{bmatrix}
e^{\lambda_1t} & & 0 \\
& \ddots \\
0 & & e^{\lambda_nt}
\end{bmatrix}
T^{-1}
$$

#### 3. $A$为约旦矩阵

$$
A = J = 
\begin{bmatrix}
\lambda & 1 & &  0 \\
& \lambda & \ddots & \\
& & \ddots & 1 \\
0& & & \lambda 
\end{bmatrix}_{n \times n} \\

e^{Jt} = \varPhi(t) = 
e^{\lambda t}
\begin{bmatrix}
1 & t & \frac{1}{2!}t^2 & \dots & \frac{1}{(n - 1)!}t^{n - 1} \\
0 & 1 & t & \dots & \frac{1}{(n - 2)!}t^{n - 2} \\
& & & \dots  \\
0 & 0 & 0 & \dots & t \\
0 & 0 & 0 & \dots & 1
\end{bmatrix}(每行向下求导)
$$

#### 4. $A = \begin{bmatrix} \sigma & \omega \\ -\omega & \sigma \end{bmatrix}$

$$
e^{At} = \varPhi(t) = 
\begin{bmatrix}
\cos\omega t & \sin\omega t \\
-\sin\omega t & \cos\omega t
\end{bmatrix}
e^{\sigma t}
$$

### $\varPhi(t)$或$e^{At}$的计算

#### 由$e^{At}$或$\varPhi(t)$的定义直接计算

$$
e^{At} = \sum_{n = 0}^{\infty} \frac{1}{n!}A^nt^n
$$

==注意== 此方法难以获得解析解

#### 变换A为约旦标准形

- $A$特征值互异

$A$的对角化：$\varLambda = T^{-1}AT$，$T$是使$A$变换为对角线矩阵的变换阵
$$
e^{At} = Te^{\varLambda t}T^{-1} = 
T
\begin{bmatrix}
e^{\lambda_1t} & & 0 \\
& \ddots \\
0 & & e^{\lambda_nt}
\end{bmatrix}
T^{-1}
$$

- $A$特征值有重根

令$J = T^{-1}AT$，$T$是使$A$变换为约旦块型矩阵的变换阵
$$
e^{At} = Te^{Jt}T^{-1} = 
e^{\lambda t}T
\begin{bmatrix}
1 & t & \frac{1}{2!}t^2 & \dots & \frac{1}{(n - 1)!}t^{n - 1} \\
0 & 1 & t & \dots & \frac{1}{(n - 2)!}t^{n - 2} \\
& & & \dots  \\
0 & 0 & 0 & \dots & t \\
0 & 0 & 0 & \dots & 1
\end{bmatrix}T^{-1}
$$

#### 利用拉氏变换法求$e^{At}$

$$
e^{At} = \varPhi(t) = L^{-1}[(sI - A)^{-1}]
$$

##### 常用拉氏变换

$$
\frac{1}{s + a} \rightarrow e^{-at} \\
\frac{m!}{s^{m+1}} \rightarrow t^m
$$

#### 应用凯莱-哈密顿定理求$e^{At}$

所有等于或高于n次的项均可以表示为低次项之和：
$$
\begin{aligned}
e^{At} &= a_{n - 1}(t)A^{n - 1} + a_{n - 2}(t)A^{n - 2} + \dots + a_{1}(t)A + a_0(t)I \\
&= \sum_{i = 0}^{n-1} a_i(t)A^i
\end{aligned}
$$
==注意== n为特征方程最高次项的阶数，也即方阵A的阶数。

##### $a_i(t)$的计算公式

-  A的特征值互异

$$
\begin{bmatrix}

a_0(t) \\

a_1(t) \\

\vdots \\

a_{n - 1}(t) \\

\end{bmatrix} = 

\begin{bmatrix}

1 & \lambda_1 & \lambda_1^2 & \dots & \lambda_1^{n - 1} \\

1 & \lambda_2 & \lambda_2^2 & \dots & \lambda_2^{n - 1} \\

& & \dots & \dots \\

1 & \lambda_n & \lambda_n^2 & \dots & \lambda_n^{n - 1} \\

\end{bmatrix}^{-1}

\begin{bmatrix}

e^{\lambda_1t} \\

e^{\lambda_2t} \\

\vdots \\

e^{\lambda_nt} 

\end{bmatrix}
$$

==注意== 不要忽略公式中的[求逆操作]()

- A的特征值均相同（$= \lambda_1$） ==不看==

$$
\begin{bmatrix}

a_0(t) \\

a_1(t) \\

\vdots \\

a_{n - 1}(t) \\

\end{bmatrix} = 

\begin{bmatrix}

0 & 0 & 0 & \dots & 0 & 1 \\

0 & 0 & 0 & \dots & 1 & (n - 1)\lambda_1 \\

\vdots & \vdots & \vdots &  & & \vdots \\

0 & 0 & 1 & \dots & & \frac{(n - 1)(n - 2)}{2!}\lambda_1^{n - 3} \\

0 & 1 & 2\lambda_1 & \dots & & \frac{(n - 1)\lambda_1^{n - 2}}{1!} \\

1 & \lambda_1 & \lambda_1^2 & \dots & \lambda_1^{n - 2} & \lambda_1^{n - 1}

\end{bmatrix}^{-1}

\begin{bmatrix}

\frac{1}{(n - 1)!}t^{n - 1}e^{\lambda_1t} \\

\frac{1}{(n - 2)!}t^{n - 2}e^{\lambda_1t} \\

\vdots \\

\frac{1}{2!}t^{2}e^{\lambda_1t} \\

te^{\lambda_1t} \\

e^{\lambda_1t}

\end{bmatrix}
$$

## 线性定常系统非齐次方程的解

<img src="C:\Users\Joker\AppData\Roaming\Typora\typora-user-images\image-20230920091800463.png" alt="image-20230920091800463" style="zoom:67%;" />

# 第3章 线性控制系统的能控性和能观性

## 能控性的定义

### 能控性的含义

1. 系统在$u(t)$的控制下，$x(t)$的转移情况
2. 与输出$y(t)$无关

## 线性定常系统的能控性判别

### 具有约旦标准形系统的能控性判别

#### A为对角线矩阵

单输入/多输入系统：若[B的任一行]()不为0，则系统完全能控

#### A为约旦块

单输入/多输入系统：若[约旦块对应的B末尾行]()非全0，则系统能控

==帮助理解== 在约旦标准型系统中，各状态分量存在如下关系：
$$
\dot{x}_{i} = \lambda_i x_i + x_{i+1}
$$
因而有：
$$
\begin{aligned}
& x_n \\
&\Downarrow 影响 \\
& x_{n-1} \\
& \Downarrow 影响 \\
& x_{i} \\
& \Downarrow 影响 \\
& x_{1} 
\end{aligned}
$$
即：

- $x_n$可[影响]()其他所有状态分量 $\Rightarrow$ [能控性]()判别
- $x_1$可[反映]()其他所有状态分量 $\Rightarrow$ [能观性]()判别

#### A为普通矩阵的处理方法

线性变换不改变系统的能控性
$$
\dot{x} = Ax + Bu \\
\Downarrow x = Tz \\
\dot{z} = Jz + T^{-1}Bu
$$

### 直接从A与B判别系统的能控性

#### 单输入系统（P97）

<img src="C:\Users\Joker\AppData\Roaming\Typora\typora-user-images\image-20230909151847271.png" alt="image-20230909151847271" style="zoom: 50%;" />

#### 多输入系统

<img src="C:\Users\Joker\AppData\Roaming\Typora\typora-user-images\image-20230927092103716.png" alt="image-20230927092103716" style="zoom: 67%;" />

## 线性连续定常系统的能观性

### 能观性定义

如果对任意给定的输入$u$，在有限观测时间$t_f > t_0$内，输出$y(t)$能唯一地确定$x(t_0)$，则称状态$x(t_0)$是能观测的。

### 线性定常系统能观性判别

#### 具有约旦标准型系统的能观性判别

- A为对角线矩阵：若输出矩阵C[任一列不为0]()，则系统完全能观
- A为约旦块矩阵：若输出矩阵C[对应每个约旦块开头一列非全零]()，则系统能观

#### 直接从A，C阵判断系统的能观性（秩判据）

系统：$
\begin{cases}
\dot{x} = Ax,\ x(t_0) = x_0 \\
y = Cx
\end{cases}
$
能观性矩阵：$
N_{nm \times n} = [C \quad CA \quad ... CA^{n - 1}]^T
$
完全能观的充要条件：能观性矩阵N的秩为n

## 能控性与能观性的对偶关系

### 线性系统的对偶关系

对于两系统：
$$
\Sigma_1:
\begin{cases}
\dot{x}_1 = A_1x_1 + B_{1, n \times r}u_{1, r} \\
y_{1, m} = C_{1, m \times n}x_1
\end{cases} \\
\Sigma_2:
\begin{cases}
\dot{x}_2 = A_2x_2 + B_{2, n \times m}u_{2, m} \\
y_{2, r} = C_{2, r \times n}x_2
\end{cases}
$$
$\Sigma_1, \Sigma_2$互为对偶的条件：
$$
A_2 = A_1^T,\ B_2 = C_1^T,\ C_2 = B_1^T
$$
==注== 

- 对偶系统的传递函数矩阵[互为转置]()：

<img src="C:\Users\Joker\AppData\Roaming\Typora\typora-user-images\image-20231124162235611.png" alt="image-20231124162235611" style="zoom: 80%;" />

- 互为对偶的系统，其特征方程式相同：

$$
| sI - A_1 | = | sI - A_2^T | = | sI - A_2 |
$$

### 对偶原理

若系统$\Sigma_1, \Sigma_2$互为对偶，则有：$\Sigma_1$完全能控 $\Harr$ $\Sigma_2$完全能观。

![image-20230927092439476](C:\Users\Joker\AppData\Roaming\Typora\typora-user-images\image-20230927092439476.png)

## 状态空间表达式的能控标准型与能观标准型

==注意== 状态空间表达式化为能控标准型和能观标准型的前提条件：系统能控或能观

### 单输入系统的能控标准型

#### 能控标准$I$型

$$
\begin{cases}
\dot{x} = Ax + bu \\
y = cx
\end{cases}
\stackrel{x = T_{c1}\overline{x}}{===\Rightarrow}
\begin{cases}
\dot{\overline{x}} = \overline{A}\overline{x} + \overline{b}\overline{u} \\
y = \overline{c}\overline{x} 
\end{cases}
$$

特征方程：
$$
|\lambda I - A| = \lambda^n + a_{n - 1}\lambda^{n - 1} + ... + a_1\lambda + a_0 = 0 \\
$$

其中：

$$
T_{c1} = 
[A^{n - 1}b \quad A^{n - 2}b \quad ... \quad b]
\begin{bmatrix}
1 & & & & 0 \\
a_{n - 1} & 1 \\
\vdots & & \ddots \\
a_2 & a_3 & & \ddots \\
a_1 & a_2 & \dots & a_{n - 1} & 1
\end{bmatrix} \\
\overline{A} = T_{c1}^{-1}AT_{c1} = 
\begin{bmatrix}
0 & 1 & 0 & \dots & 0 \\
0 & 0 & 1 & \dots & 0 \\
\vdots & \vdots & \vdots & \ddots & \vdots \\
0 & 0 & 0 & \dots & 1 \\
-a_0 & -a_1 & -a_2 & \dots & -a_{n - 1}
\end{bmatrix} \\
\overline{b} = [0 \quad 0 \quad ... \quad 1]^T \\
\overline{c} = cT_{c1}
$$

#### 能控标准$II$型

$$
\begin{cases}
\dot{x} = Ax + bu \\
y = cx
\end{cases}
\stackrel{x = T_{c2}\overline{x}}{====\Rightarrow}
\begin{cases}
\dot{\overline{x}} = \overline{A}\overline{x} + \overline{b}\overline{u} \\
y = \overline{c}\overline{x} 
\end{cases} \\
$$

其中：
$$
T_{c2} = [b \quad Ab \quad ... \quad A^{n - 1}b] \\
\overline{A} = T_{c2}^{-1}AT_{c2} = 
\begin{bmatrix}
0 & 0 & \dots & 0 & -a_0 \\
1 & 0 & \dots & 0 & -a_1 \\
0 & 1 & \dots & 0 & -a_2 \\
\vdots & \vdots & \ddots & \vdots & \vdots \\
0 & 0 & \dots & 1 & -a_{n - 1} \\
\end{bmatrix} \\
\overline{b} = [1 \quad 0 \quad \dots \quad 0 \quad 0]^T \\
\overline{c} = cT_{c2} = 
[cb \quad cAb \quad \dots \quad cA^{n - 1}b]
$$

==注==

- 在能控标准$II$型中，有$T_{c2} = M = [b \quad Ab \quad ... \quad A^{n - 1}b]$
- 记忆公式时，注意$\overline{A},\ \overline{b}$中1的分布特点

### 单输出系统的能观标准型

#### 能观标准$I$型

与能控标准$II$型对偶：
$$
\begin{cases}
\dot{x} = Ax + bu \\
y = cx
\end{cases} 
\stackrel{x = T_{o1}\tilde{x}}{====\Rightarrow}
\begin{cases}
\dot{\tilde{x}} = \tilde{A}\tilde{x} + \tilde{b}u \\
y = \tilde{c}\tilde{x}
\end{cases} \\
$$


其中：
$$
T_{o1}^{-1} = N = 
\begin{bmatrix}
c \\
cA \\
\vdots \\
cA^{n - 1}
\end{bmatrix}
\\
\tilde{A} = T_{o1}^{-1}AT_{o1} = 
\begin{bmatrix}
0 & 1 & \dots & 0 & 0 \\
0 & 0 & \ddots & 0 & 0 \\
\vdots & \vdots & \ddots & \ddots & \vdots \\
0 & 0 & \dots & 0 & 1 \\
-a_0 & -a_1 & \dots & -a_{n - 2} & -a_{n - 1}
\end{bmatrix} \\
\tilde{b} = T_{o1}^{-1}b = [cb \quad cAb \quad \dots \quad cA^{n - 1}b]^T \\
\tilde{c} = cT_{o1} = [1 \quad 0 \quad 0 \quad ... \quad 0]
$$

#### 能观标准$II$型

与能控标准$I$型对偶：
$$
\begin{cases}
\dot{x} = Ax + bu \\
y = cx
\end{cases}
\stackrel{x = T_{o2}\tilde{x}}{====\Rightarrow}
\begin{cases}
\dot{\tilde{x}} = \tilde{A}\tilde{x} + \tilde{b}u \\
y = \tilde{c}\tilde{x}
\end{cases} \\
$$
其中：
$$
T_{o2}^{-1} = 
\begin{bmatrix}
1 & a_{n - 1} & \dots & a_2 & a_1 \\
0 & 1 & \dots & a_3 & a_2 \\
\vdots & \vdots & \ddots & \vdots & \vdots \\
0 & 0 & \dots & 1 & a_{n - 1} \\
0 & 0 & \dots & 0 & 1
\end{bmatrix}
\begin{bmatrix}
CA^{n - 1} \\
\vdots \\
CA \\
C
\end{bmatrix} \\
\tilde{A} = T_{o2}^{-1}AT_{o2} = 
\begin{bmatrix}
0 & 0 & \dots & 0 & -a_0 \\
1 & 0 & \dots & 0 & -a_1 \\
0 & 1 & \dots & 0 & -a_2 \\
\vdots & \vdots & \ddots & \vdots & \vdots \\
0 & 0 & \dots & 1 & -a_{n - 1} 
\end{bmatrix} \\
\tilde{b} = T_{o2}^{-1}b \\
\tilde{c} = cT_{o2} = [0 \quad 0 \quad 0 \quad \dots \quad 1]
$$

==注==

- 在能观标准$I$型中，有$T_{o1}^{-1} = N = [C \quad CA \quad \dots \quad CA^{n-1}]^T$
- 在记忆公式时，注意$\tilde{A},\ \tilde{c}$中1的分布特点

## 线性系统的结构分解

### 按能控性分解

$$
\begin{cases}
\dot{x} = Ax + Bu \\
y = Cx
\end{cases}
\stackrel{x = R_c\hat{x}}{===\Rightarrow}
\begin{cases}
\dot{\hat{x}} = \hat{A}\hat{x} + \hat{B}u \\
y = \hat{C}\hat{x}
\end{cases} \\
$$

$$
\hat{x} = 
\begin{bmatrix}
\hat{x}_1 \\ 
\hat{x}_2
\end{bmatrix} \\
\hat{A} = R_c^{-1}AR_c = 
\begin{bmatrix}
\hat{A}_{11} & \hat{A}_{12} \\
0 & \hat{A}_{22}
\end{bmatrix} \\
\hat{B} = R_c^{-1}B = 
\begin{bmatrix}
B_1 \\
0
\end{bmatrix} \\
\hat{C} = CR_c = [\hat{C}_1 \quad \hat{C}_2]
$$

==注== $\hat{A}$[左下]()角为0

分解得到子系统：

能控：$
\dot{\hat{x}}_1 = \hat{A}_{11}\hat{x}_1 + \hat{A}_{12}\hat{x}_2 + \hat{B}_1u 
$

不能控：$
\dot{\hat{x}}_2 = \hat{A}_{22}\hat{x}_2 
$

#### 非奇异变换阵$R_c$的获取

- 前$n_1$个列矢量是[能控性矩阵M]()中$n_1$个[线性无关]()的列
- 其他列在确保$R_c$是非奇异的条件下任意选取

#### ==按能控性分解的步骤==

1. 判断能控性（若状态不完全能控，则进行能控性分解）
2. 确定变换矩阵$R_c$（选取要参考能控性判别阵M）
3. 套公式计算：

$$
\overline{A} = R_c^{-1}AR_c \\
\overline{B} = R_c^{-1}B \\
\overline{C} = CR_c
$$

4. 提取子系统：

$$
\dot{\overline{x}}_1 = \overline{A}_{11}\overline{x}_1 + \overline{A}_{12}\overline{x}_2 + \overline{B}_1u \\
\dot{\overline{x}}_2 = \overline{A}_{22}\overline{x}_2
$$

==注== 选取不同的非奇异变换阵$R_c$得到的二维能控子系统的状态空间表达式应当是相同的（能控标准$II$型），因为变换阵的前$n_1$列是能控性判别矩阵中的$n_1$个线性无关的列。（B135）

### 按能观性分解

$$
\begin{cases}
\dot{x} = Ax + Bu \\
y = Cx
\end{cases}
\stackrel{x = R_o\tilde{x}}{===\Rightarrow}
\begin{cases}
\dot{\tilde{x}} = \tilde{A}\tilde{x} + \tilde{B}u \\
y = \tilde{C}\tilde{x}
\end{cases} \\
$$

$$
\tilde{A} = R_o^{-1}AR_o = 
\begin{bmatrix}
\tilde{A}_{11} & 0 \\
\tilde{A}_{21} & \tilde{A}_{22}
\end{bmatrix} \\
\tilde{B} = R_o^{-1}B = 
\begin{bmatrix}
\tilde{B}_1 \\
\tilde{B}_2
\end{bmatrix} \\
\tilde{C} = CR_o = 
\begin{bmatrix}
\tilde{C}_1 & 0
\end{bmatrix}
$$

==注== $\hat{A}$[右上]()角为0矩阵

状态空间的分解：

- 能观：$
\begin{cases}
\dot{\tilde{x}}_1 = \tilde{A}_{11}\tilde{x}_1 + \tilde{B}_1u \\
y = \tilde{C}_1\tilde{x}_1 
\end{cases} 
$
- 不能观：$
\dot{\tilde{x}}_2  = \tilde{A}_{21}\tilde{x}_1 + \tilde{A}_{22}\tilde{x}_2 + \tilde{B}_2u
$

#### 非奇异变换阵$R_o^{-1}$的获取

- 前$n_1$行矢量是能观性判别阵中$n_1$个线性无关的行
- 其他行矢量在确保$R_o^{-1}$为非奇异的条件下任意选取

#### 按能观性分解的步骤

1. 判断能观性
2. 确定变换矩阵
3. 套公式计算
4. 提取子系统

### 按能控性和能观性分解



![image-20231119150957373](C:\Users\Joker\AppData\Roaming\Typora\typora-user-images\image-20231119150957373.png)

#### 能控能观分解的步骤

  1. 判断能控性
  2. 按能控性分解
  3. 分别判断能控子系统和不能控子系统的能观性
  4. 分别按能观性分解
  5. 按四类状态变量分组，写出分解后系统

## 3.9 传递函数阵的实现问题

### 实现问题的基本概念

实现的定义：

给定传递函数阵$W(s)$，求一状态空间表达式：
$$
\Sigma 
\begin{cases}
\dot{x} = Ax + Bu \\
y = Cx + Du
\end{cases}
$$
满足$C(sI - A)^{-1}B + D = W(s)$

### 能控标准型实现和能观标准型==实现==

对于单输入单输出系统，其传递函数设为：
$$
W(s) = \frac{\beta_{n-1}s^{n-1} + \beta_{n-2}s^{n-2} + ... + \beta_1s + \beta_0}{s^n + \alpha_{n-1}s^{n-1} + ... + \alpha_1s + \alpha_0}
$$
==注意== 此处$\beta_n = 0$，为[真分式]()的形式

#### 能控标准型

![image-20231124164212953](C:\Users\Joker\AppData\Roaming\Typora\typora-user-images\image-20231124164212953.png)

#### 能观标准型

![image-20231124164233905](C:\Users\Joker\AppData\Roaming\Typora\typora-user-images\image-20231124164233905.png)

### 最小实现

最小实现的定义：

![image-20231124162629155](C:\Users\Joker\AppData\Roaming\Typora\typora-user-images\image-20231124162629155.png)

==定理==

传递函数阵$W(s)$的一个实现：
$$
\Sigma
\begin{cases}
\dot{x} = Ax + Bu \\
y = Cx
\end{cases}
$$
是最小实现的充要条件：$\Sigma(A, B, C)$[能控且能观]()。

## 3.10 传递函数中==零极点对消==与状态能控性和能观性之间的关系

对于一个单输入单输出系统$\Sigma(A, b, c)$
$$
\dot{x} = Ax + bu \\
y = cx
$$
是[能控并能观]()的充要条件是传递函数：
$$
W(s) = c(sI - A)^{-1}b
$$
的[分子分母间没有零极点对消]()。

# 第4章 稳定性与李雅普诺夫方法

## 4.1 李雅普诺夫关于稳定性的定义

### 李雅普诺夫意义下稳定

![image-20231120145301391](C:\Users\Joker\AppData\Roaming\Typora\typora-user-images\image-20231120145301391.png)

### 渐进稳定

![image-20231120145342726](C:\Users\Joker\AppData\Roaming\Typora\typora-user-images\image-20231120145342726.png)

### 大范围渐进稳定

![image-20231120145415880](C:\Users\Joker\AppData\Roaming\Typora\typora-user-images\image-20231120145415880.png)

### 不稳定

![image-20231120145501767](C:\Users\Joker\AppData\Roaming\Typora\typora-user-images\image-20231120145501767.png)

## 4.2 李雅普诺夫第一法

### 线性系统的稳定判据

- **渐进稳定**的充要条件：矩阵A的[特征根均具有负实部]()
- **输出稳定**的充要条件：传递函数的[极点全部位于s左半平面]()

![image-20231027173702817](C:\Users\Joker\AppData\Roaming\Typora\typora-user-images\image-20231027173702817.png)

状态稳定和输出稳定的关系：

<img src="C:\Users\Joker\AppData\Roaming\Typora\typora-user-images\image-20231027173759808.png" alt="image-20231027173759808" style="zoom:67%;" />

## 4.3 李雅普诺夫第二法

### 预备知识

#### 标量函数的符号性质

![image-20231120145917727](C:\Users\Joker\AppData\Roaming\Typora\typora-user-images\image-20231120145917727.png)

#### 二次型标量函数

定义：
$$
V(x) = x^TPx \\
= (x_1 \quad x_2 \quad ... \quad x_n)
\begin{pmatrix}
p_{11} & p_{12} & \dots & p_{1n} \\
p_{21} & p_{22} & \dots & p_{2n} \\
\vdots & \vdots & \ddots & \vdots \\
p_{n1} & p_{n2} & \dots & p_{nn} \\
\end{pmatrix}
\begin{pmatrix}
x_1 \\
x_2 \\
\vdots \\
x_n 
\end{pmatrix}
$$
二次型函数的标准型：若矩阵P为实对称阵，则必存在正交矩阵$T$，通过变换$x = T\overline{x}$，使得：
$$
v(x) = \overline{x}^T 
\begin{pmatrix}
\lambda_1  & & & \\
& \lambda_2 & & \\
& & \ddots & \\
& & & \lambda_n
\end{pmatrix} \overline{x}
$$
$V(x)$正定的充要条件：对称阵P的所有特征值均大于0。

==注== 矩阵$P$的符号性质定义：$P$和$V(x)$的符号性质完全一致。

#### 希尔维斯特判据

![image-20231120151235181](C:\Users\Joker\AppData\Roaming\Typora\typora-user-images\image-20231120151235181.png)

- $\Delta_i|_{i = n} = 0$对应半正定或半负定

### 李雅普诺夫第二法判据

![image-20231027172333587](C:\Users\Joker\AppData\Roaming\Typora\typora-user-images\image-20231027172333587.png)

<img src="C:\Users\Joker\AppData\Roaming\Typora\typora-user-images\image-20231027172442449.png" alt="image-20231027172442449" style="zoom: 67%;" />

#### 李雅普诺夫第二法的步骤

1. 计算平衡状态（原点，$x_e = 0$）
2. 选取正定能量函数$V(x)$​

标量函数$V(x)$需满足的条件：

- 具有连续的一阶偏导
- 是正定的，即$V(x)|_{x = 0} = 0,\ V(x)|_{x \ne 0} > 0$

3. 求得$\dot{V}(x)$后，将状态方程代入，在$x \ne 0$的条件下判断$\dot{V}(x)$的定号性：

$$
\dot{V}(x)
\begin{cases}
正定/半正定
\begin{cases}
正定 \Rightarrow 不稳定 \\
半正定，不恒为0 \Rightarrow 不稳定 
\end{cases} \\
半负定
\begin{cases}
恒为0 \Rightarrow 稳定，非渐进稳定 \\
不恒为0 \Rightarrow 渐进稳定
\end{cases} \\
负定 \Rightarrow 渐进稳定
\end{cases}
$$

==注意== 

- 系统的平衡状态应保持在原点处，这样才能根据正定能量函数$V(x)$的正定性判断系统的稳定性。当系统平衡状态不处于原点时，需进行坐标变换，见例5：

![image-20231121195132554](C:\Users\Joker\AppData\Roaming\Typora\typora-user-images\image-20231121195132554.png)

## 4.4 李雅普诺夫方法在线性系统中的应用

对于线性定常系统$\dot{x} = Ax$，$A$非奇异，则平衡点$x_e = 0$大范围渐进稳定的充要条件：

- 李雅普诺夫第一法：$A$的特征根均具有负实部

- 李雅普诺夫第二法

思路一：先给定正定能量函数，在判别能量变化，即矩阵$P$先给定。

思路二：系统渐进稳定的[充要条件]()是，对于任意给定的正定对称矩阵$Q$，[存在正定矩阵$P$]()，满足李雅普诺夫方程
$$
A^TP + PA = -Q \\
(通常取Q = I)
$$
==思路二的应用步骤==：

1. 选取一个正定矩阵$Q = I$
2. 代入李雅普诺夫方程$A^TP + PA = -Q$
3. 解出矩阵$P$
4. 按希尔维斯特判据判定$P$的正定性
5. 做出系统渐进稳定的结论（$P$为正定$\Rightarrow$系统渐进稳定）

==注意== 若$V(x)$的导数沿任意轨迹不恒为零，则可取$Q$为[半正定]()（B171）

选取李雅普诺夫函数：
$$
V(x) = x^TPx
$$
结合李雅普诺夫方程$A^TP + PA = -Q$，则有：
$$
\begin{aligned}
\dot{V}(x) &= x^T(A^TP + PA)x \\
&= -x^TQx
\end{aligned}
$$
因此，在证明$V(x)$的导数不恒为零时，需取[$V(x) = -x^TQx$]()

# 第5章 线性定常系统的综合

本章讨论常规综合：综合目标仅为了使系统性能满足某种笼统指标要求。

## 5.1 线性反馈控制系统的基本结构及其特性

### 5.1.1 状态反馈

![image-20231122120135633](C:\Users\Joker\AppData\Roaming\Typora\typora-user-images\image-20231122120135633.png)

- 开环系统：

$$
\begin{aligned}
\Sigma_0 &= (A, B, C) \\
&= 
\begin{cases}
\dot{x} = Ax + Bu \\
y = Cx
\end{cases}
\end{aligned}
$$

- 状态线性反馈控制律：

$$
u = Kx + v
$$

$K$：状态反馈系数（增益）阵

- 闭环系统的状态空间表达式：

$$
\begin{aligned}
\Sigma_k &= [(A + BK), B, C] \\
&= 
\begin{cases}
\dot{x} = (A + BK)x + Bv \\
y = Cx
\end{cases}
\end{aligned}
$$

- 闭环系统的传递函数阵：

$$
W_k(s) = C[sI - (A + BK)]^{-1}B
$$

### 5.1.2 输出反馈

- 输出线性反馈控制律：

$$
u = Hy + v
$$


$H$：输出反馈增益阵

- 闭环系统的状态空间表达式：

$$
\begin{aligned}
\Sigma_H &= [(A + HC), B, C] \\
&= 
\begin{cases}
\dot{x} = (A + BHC)x + Bv \\
y = Cx
\end{cases}
\end{aligned}
$$

- 闭环系统的传递函数阵：

$$
W_H(s) = C[sI - (A + BHC)]^{-1}B
$$

==说明==

1. 输出反馈中的$HC$与状态反馈中的$K$相当
2. 输出反馈只能相当于一种部分状态反馈
3. 当$C = I$时，$HC = K$，等同于全状态反馈

### 5.1.3 从输出到状态矢量导数$\dot{x}$反馈

- 闭环系统

$$
\begin{aligned}
\Sigma_G &= [(A + GC), B, C] \\
&= 
\begin{cases}
\dot{x} = (A + GC)x + Bu \\
y = Cx
\end{cases}
\end{aligned}
$$

$G$：反馈增益阵

- 闭环系统的传递函数阵：

$$
W_G(s) = C[sI - (A + GC)]^{-1}B
$$

### 5.1.5 闭环系统的能控性与能观性

- [状态反馈不改变能控性]()，能观性不确定
- **输出反馈**不改变受控系统的能控性和能观性

## 5.2 极点配置问题

指定极点分布，设计反馈增益阵。

各类反馈任意配置极点的充要条件：

- [状态]()反馈：系统完全[能控]()
- 输出反馈：[不能实现]()极点任意配置

- 输出到$\dot{x}$反馈：系统完全[能观]()

### 采用状态反馈

定理：采用状态反馈对系统$\Sigma_0(A, b, c)$任意配置极点的充要条件：$\Sigma_0(A, b, c)$[完全能控]()

#### 配置步骤

1. 由$x = T_{c1}\overline{x}$，将$\Sigma_0$化为能控标准$I$型：

$$
\begin{cases}
\dot{\overline{x}} = \overline{A}\overline{x} + \overline{b}u \\
y = \overline{c}\overline{x}
\end{cases}
$$

2. 加入状态反馈增益阵$\overline{K} = [\overline{k_0},\ \overline{k}_1,\ \dots,\ \overline{k}_{n - 1}]$：

$$
\begin{cases}
\dot{\overline{x}} = (\overline{A} + \overline{b}\overline{K})\overline{x} + \overline{b}u \\
y = \overline{c}\overline{x}
\end{cases}
$$

闭环特征多项式：
$$
f(\lambda) = \det{[\lambda I - (\overline{A} + \overline{b}\overline{K})]}
$$
期望特征多项式：
$$
f^*(\lambda) = \prod_{i = 1}^n (\lambda - p_i)
$$
$p_i$：期望的闭环极点

3. 使$f(\lambda) = f^*(\lambda)$，得到$\overline{K}$
4. 获得对应原系统状态$x$的$K$：

$$
K = \overline{K}T_{c1}^{-1}
$$

==注意== 当系统阶数较低时，可由原系统状态方程直接计算反馈增益阵$K$，[无需化为能控标准$I$型]()（主要是为了方便行列式计算）。此时计算步骤可简化为：

1. 引入状态反馈阵$K$，得闭环系统特征多项式：

$$
f(\lambda) = \det[\lambda I - (A + bk)]
$$

2. 由给定极点值得期望特征多项式：

$$
f^*(\lambda) = \prod_{i = 1}^n (\lambda - p_i)
$$

3. 比较$f(\lambda),\ f^*(\lambda)$对应各项系数，得$K$

### 采用输出反馈

对完全能控的单入单出系统，[不能]()采用输出线性反馈实现闭环系统极点的任意配置。

### 采用从输出到$\dot{x}$反馈

- 对系统$\Sigma_0(A, b, c)$采用从输出到$\dot{x}$的线性反馈实现闭环极点任意配置的充要条件：$\Sigma_0(A, b, c)$[完全能观]()

- 由$\lambda_{(A^T + c^TG^T)} = \lambda_{(A + Gc)}$：

设计$\Sigma_0(A, b, c)$输出到$\dot{x}$反馈阵$G$ $\Harr$ 对偶系统$\tilde{\Sigma}_0(A^T, c^T, b^T)$设计状态反馈阵$K$

## 5.3 系统镇定问题

系统镇定：受控系统通过反馈使其极点均具有负实部，保证为渐进稳定。

- 对系统$\Sigma_0(A, B, C)$，[状态反馈能镇定]()的充要条件：[不能控]()子系统为[渐进稳定]()

- 对系统$\Sigma_0(A, B, C)$，[输出反馈能镇定]()的充要条件：

1. $\Sigma_0$结构分解中能控且能观子系统是[输出反馈能镇定]()的
2. 其余子系统[渐进稳定]()

==注== 能控且能观系统不能通过输出线性反馈任意配置极点，[不一定输出反馈能镇定]()

- 对系统$\Sigma_0(A, B, C)$，[输出到$\dot{x}$反馈能镇定]()的充要条件：$\Sigma_0$的[不能观]()子系统为[渐进稳定]()

## 5.5 状态观测器

### 5.5.1 状态观测器定义

动态系统$\hat{\Sigma}$以$\Sigma_0$的输入$u$和输出$y$作为输入量，输出量$\hat{x}$渐进于$x$，即：
$$
\lim_{t \rightarrow \infty}|x - \hat{x}| = 0
$$
状态观测器作用：利用输入量和输出量，重构系统状态

### 5.5.2 状态观测器的存在性

对线性定常系统，[状态观测器存在的充要条件]()：$\Sigma_0$的[不能观子系统为渐进稳定]()。

### 5.5.3 状态观测器实现

$$
\dot{\hat{x}} = (A - GC)\hat{x} + Gy + Bu
$$

![image-20231123173625275](C:\Users\Joker\AppData\Roaming\Typora\typora-user-images\image-20231123173625275.png)

### 5.5.4 反馈矩阵G的设计

状态误差矢量：$\tilde{x} = x - \hat{x}$
$$
\dot{\tilde{x}} = (A - GC)\tilde{x}
$$

![image-20231122172936065](C:\Users\Joker\AppData\Roaming\Typora\typora-user-images\image-20231122172936065.png)

#### 设计步骤

1. 检验能观性，系统[能观]()则可构造观测器
2. 将系统化为能观$II$型：

$$
x = T\overline{x} \quad \Rightarrow \quad
\begin{cases}
\dot{\overline{x}} = \overline{A}\overline{x} + \overline{B}u \\
y = \overline{c}\overline{x}
\end{cases}
$$

3. 引入反馈阵：

$$
\overline{G} = 
\begin{bmatrix}
\overline{g}_1 \\
\overline{g}_2 \\
\end{bmatrix}
$$

得观测器特征多项式：
$$
f(\lambda) = \det[\lambda I - (\overline{A} - \overline{G}\overline{c})]
$$

4. 由期望极点得期望多项式：

$$
f^*(\lambda) = \prod_{i = 1}^n (\lambda - p_i)
$$

5. 比较系数$f(\lambda) = f^*(\lambda)$，得$\overline{G}$
6. 反变换到$x$状态下：[$G = T\overline{G}$]()
7. 观测器方程：

$$
\dot{\hat{x}} = (A - Gc)\hat{x} + bu + Gy \\
或：\dot{\hat{x}} = A\hat{x} + bu + G(y - \hat{y})
$$

==注意==

- 注意区分：

状态观测器的系数矩阵：$A_{观测器} = A-GC$

从输出到$\dot{x}$反馈闭环系统的系数矩阵：$A_{闭环} = A + GC$

- 当系统维数较低时，检验能观性后，可直接按特征式比较来确定反馈阵$G$，[无需化为能观标准型]()
- 化为能观标准形后$\overline{G}$的反变换公式$G = T\overline{G}$的证明（不标准）：

原系统状态观测器的系数矩阵：
$$
\tilde{A} = A - GC
$$
化为能观标准型系统后状态观测器的系数矩阵：
$$
\tilde{A}' = \overline{A} - \overline{G}\overline{C}
$$
参考能观标准型变换：
$$
x = T\overline{x}
$$
则有：
$$
\tilde{A}’ = T^{-1}\tilde{A}T
$$
即：
$$
T^{-1}AT - \overline{G}CT = T^{-1}AT - T^{-1}GCT
$$
对比可得：
$$
G = T\overline{G}
$$

### 5.5.5 降维观测器

若系统能观，且输出矩阵$c$的秩是$m$：

- $m$个状态分量可由$y$直接获得
- $(n - m)$个状态分量用$(n - m)$维的降维观测器进行重构

系统经$T$变换为如下形式：
$$
\begin{aligned}

\begin{pmatrix}
\dot{\overline{x}}_1 \\
\dot{\overline{x}}_2
\end{pmatrix} &= 
\begin{pmatrix}
\overline{A}_{11} & \overline{A}_{12} \\
\overline{A}_{21} & \overline{A}_{22}
\end{pmatrix}
\begin{pmatrix}
\overline{x}_1 \\
\overline{x}_2 
\end{pmatrix} + 
\begin{pmatrix}
\overline{B}_1 \\
\overline{B}_2
\end{pmatrix}u \\

\overline{y} &= (0, \quad I)
\begin{pmatrix}
\overline{x}_1 \\
\overline{x}_2 
\end{pmatrix} = \overline{x}_2
\end{aligned}
$$
降维观测器方程：
$$
\dot{\hat{\overline{w}}} = (\overline{A}_{11} - \overline{G}\overline{A}_{21})\hat{\overline{x}}_1 + (\overline{A}_{12} - \overline{G}\overline{A}_{22})\overline{y} + (\overline{B}_1 - \overline{G}\overline{B}_2)u \\
\hat{\overline{x}}_1 = \hat{\overline{w}} + \overline{G}\overline{y} 
$$
或将$\hat{\overline{x}}_1$代入：
$$
\dot{\hat{\overline{w}}} = (\overline{A}_{11} - \overline{G}\overline{A}_{21})\hat{\overline{w}} + [(\overline{A}_{11} - \overline{G}\overline{A}_{21})\overline{G} + (\overline{A}_{12} - \overline{G}\overline{A}_{22})]\overline{y} + (\overline{B}_1 - \overline{G}\overline{B}_2)u \\
\hat{\overline{x}}_1 = \hat{\overline{w}} + \overline{G}\overline{y} 
$$
得到原系统的状态估计：
$$
\hat{x} = T\hat{\overline{x}}
$$

## 5.6 利用状态观测器实现状态反馈的系统

### 5.6.1 系统的结构与状态空间表达式

$$
\begin{cases}
\dot{x} = Ax + BK\hat{x} + Bv \\
\dot{\hat{x}} = GCx + (A - GC + BK)\hat{x} + Bv \\
y = Cx
\end{cases}
$$

其中：
$$
\dot{\hat{x}} = (A - GC)\hat{x} + Gy + Bu \\
u = K\hat{x} + v
$$
![image-20231122193420541](C:\Users\Joker\AppData\Roaming\Typora\typora-user-images\image-20231122193420541.png)

### 5.6.2 闭环系统的基本特性

- [闭环极点设计的分离性]()：只要系统$(A, B, C)$能观，则系统的状态反馈阵$K$和观测器反馈阵$G$可分别进行设计

$\Sigma_k = (A + BK, B, C)$闭环极点：

1、$\Sigma_0$直接状态反馈系统的极点

2、观测器$\Sigma_G$的极点

二者独立，相互分离

- [传递函数矩阵的不变性]()

1、用观测器构成的状态反馈系统
2、状态直接反馈系统
二者传递函数相同

- [观测器反馈与直接状态反馈的等效性]()

当$t \rightarrow \infty$，进入稳态时，观测器反馈才与直接状态反馈等效

可通过选择$G$来加速$\tilde{x} \rightarrow 0$，即$\hat{x}$渐进于$x$的速度

### 5.6.3 带观测器状态反馈系统与带补偿器输出反馈系统的等价性

- 就传递特性而言，带观测器的状态反馈系统完全等效于同时带有串联补偿器和反馈补偿器的输出反馈系统
- 用补偿器可以构成完全等效于观测器反馈的系统





































