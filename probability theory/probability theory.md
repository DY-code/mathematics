### 期末考试范围

- 期末考试范围：第一章到第八章（第十二章不考，但作业需要做）
- 重点章节：第二，第三，第四，第七，第八章
- 重点概念题：全概率公式，随机变量函数的分布，独立性，边缘分布，两个随机变量函数分布，协方差，相关系数，参数估计，假设检验，区间估计

# 常用公式&结论

$$
P(AB) + P(A\overline{B}) = P(A)
$$

## 常用符号的定义

对任意实数a以及非负整数r，定义
$$
\begin{pmatrix}
a \\ r
\end{pmatrix} = 
\frac{a(a - 1)...(a - r + 1)}{r!}, \quad 
\begin{pmatrix}
a \\ 0
\end{pmatrix} = 1
$$
特别的，当a为正整数，且$r \le a$时，该式表示组合数，即有：
$$
\begin{pmatrix}
a \\ r
\end{pmatrix} = C_a^r
$$

## 排列组合

$$
A_n^m = n(n-1)(n-2)···(n - m + 1) = \frac{n!}{(n-m)!} \\
C_n^m = \frac{n!}{m!(n-m)!}
$$

## 抽签原理

中签概率与抽签顺序无关。n个人[不放回]()地先后从n个签中抽1张，其中m张中奖（m<n），则每个人中奖的概率均为$P = \frac{m}{n}$。

# 概率论的基本概念

## 事件的运算

- 若事件A、B互斥，则$P(AB) = 0$，反之不成立

### 交换律

$$
A \cup B = B \cup A, \quad A \cap B = B \cap A
$$

### 结合律

$$
A \cup (B \cup C) = (A \cup B) \cup C \\
A \cap (B \cap C) = (A \cap B) \cap C
$$

### 分配律

$$
A \cup(B \cap C) = (A \cup B) \cap (A \cup C) \\
A \cap(B \cup C) = (A \cap B) \cup (A \cap C)
$$

### 德摩根律

$$
\overline{A \cup B} = \overline{A} \cap \overline{B} \\
\overline{A \cap B} = \overline{A} \cup \overline{B}
$$

## 概率

### 概率的定义（条件）

#### 非负性

对于每一个事件A，有$P(A) \ge 0$

#### 规范性

对于必然事件S，有$P(S) = 1$

#### 可列可加性

设$A_1, A_2, ...$是两两互不相容的事件，即对于$A_iA_j = \varnothing, i \ne j, i,j = 1,2,...$，有：
$$
P(A_1 \cup A_2 \cup \ ...) = P(A_1) + P(A_2) + ...
$$

### 概率的重要性质

#### 性质1

$$
P(\varnothing) = 0
$$

#### 性质2（有限可加性）

若$A_1,A_2,...A_n$是两两互不相容的事件，则有：
$$
P(A_1 \cup A_2 \cup \ ... \ \cup A_n) = P(A_1) + P(A_2) + ... + P(A_n)
$$

#### 性质3

若事件$A,B$满足$A \subset B$，则有：
$$
P(B - A) = P(B) - P(A) \\
P(B) \ge P(A)
$$

####  性质4

对任一事件A有：
$$
P(A) \le 1
$$

#### 性质5（逆事件的概率）

$$
P(\overline{A}) = 1 - P(A)
$$

#### 性质6（加法公式）

对任意两事件A，B有：
$$
P(A \cup B) = P(A) + P(B) - P(AB)
$$

## 古典概型

古典概型的特点：

1. 试验的样本空间只包含有限个元素
2. 试验中每个基本事件发生的可能性相同

### 古典概型事件概率的计算公式

若事件A包含k个基本事件，即$A = \{e_{i_1}\} \cup \{e_{i_2}\} \cup ... \cup\{e_{i_k}\}$，这里$i_1, i_2, ... , i_n$是$1,2,...,n$中某k个不同的数，则有：
$$
P(A) = \sum_{j = 1}^k P(\{e_{i_j}\}) = \frac{k}{n} = \frac{A包含的基本事件数}{S中基本事件的总数}
$$

## 条件概率

==定义==

设A，B是两个事件，且$P(A) > 0$，称
$$
P(B \vert A) = \frac{P(AB)}{P(A)}
$$
为在事件A发生的条件下事件B发生的条件概率。

### 条件概率满足的条件

#### 非负性

对每一事件B，有$P(B \vert A) \ge 0$

#### 规范性

对于必然事件S，有$P(S \vert A) = 1$

#### 可列可加性

设$B_1,B_2,...$是两两互不相容的事件，则有：
$$
P(\bigcup_{i=1}^{\infty} B_i \vert A) = \sum_{i=1}^{\infty} P(B_i \vert A)
$$

### 乘法定理

设$P(A) > 0$，有：
$$
P(AB) = P(B \vert A)P(A)
$$
上式称为[乘法公式]()

#### 乘法公式的推广

设A，B，C为事件，且$P(AB) > 0$，则有：
$$
P(ABC) = P(C \vert AB)P(B \vert A)P(A)
$$
一般的，设$A_1, A_2, ..., A_n$为n个事件，$n \ge 2$，且$P(A_1 A_2 ... A_{n-1}) > 0$，则有
$$
P(A_1 A_2 ... A_n) = P(A_n \vert A_1 A_2 ... A_{n - 1}) P(A_{n - 1} \vert A_1 A_2 ... A_{n - 2}) ... P(A_2 \vert A_1) P(A_1)
$$

### 全概率公式 ==重点==

设试验E的样本空间为S，A为E的事件，[$B_1, B_2, ... ,B_n$为S的一个划分]()，且$P(B_i) > 0, (i = 1, 2, ..., n)$，则：
$$
\begin{aligned}
P(A) &= P(A \vert B_1)P(B_1) + P(A \vert B_2)P(B_2) + ... + P(A \vert B_n)P(B_n) \\
&= \sum_{i = 1}^{n}P(A | B_i)P(B_i)
\end{aligned}
$$

### 贝叶斯公式 ==重点==

设试验E的样本空间为S，A为E的事件，$B_1, B_2, ... ,B_n$为S的一个划分，且$P(A) > 0, P(B_i) > 0(i = 1,2,...,n)$，则：
$$
P(B_i \vert A) = \frac{P(A \vert B_i)P(B_i)}{\sum_{j=1}^{n}P(A \vert B_j)P(B_j)}
$$

事实上有：
$$
P(B_i \vert A) = \frac{P(AB_i)}{P(A)} = 
\frac{P(A \vert B_i)P(B_i)}{\sum_{j=1}^{n}P(A \vert B_j)P(B_j)} \\
(利用全概率公式)
$$

==注== 贝叶斯公式可用于“[已知结果判断原因]()”的情况

# 随机变量及其分布 ==重点==

## 分布函数

==定义== 设$\xi$是随机变量，x是任意的实数，称
$$
F(x) = P(\xi \le x) \quad (-\infty < x < \infty)
$$
为随机变量$\xi$的[分布函数]()

==注意== 

- $F(x)$是随机变量$\xi$取值不大于x的概率，即分布函数$F(x)$描述的是事件$\xi \le x$的概率，它是[定义于全体实数，以区间$[0, 1]$为值域]()的普通函数
- 对任意实数$a < b$，随机点落在区间$(a, b]$内的概率，显然有

$$
P(a < \xi \le b) = P(\xi \le b) - P(\xi \le a) = F(b) - F(a)
$$

### 分布函数的性质

- $$
  0 \le F(x) \le 1
  $$

- 若$x_1 < x_2$，则$F(x_1) \le F(x_2)$，即$F(x)$是[不减函数]()

- $$
  F(-\infty) = \lim_{x \rightarrow -\infty}F(x) = 0, \quad F(+\infty) = \lim_{x \rightarrow +\infty}F(x) = 1
  $$

- $$
  F(x_0 + 0) = \lim_{t \rightarrow x_0^+}F(t) = F(x_0)
  $$

即$F(x)$是[右连续]()的.

进一步还可以得到其他性质：

- $$
  P(\xi > x) = 1 - P(\xi \le x) = 1 - F(x)
  $$

- $$
  P(\xi = x) = F(x) - F(x - 0)
  $$

- $$
  P(\xi < x) = P(\xi \le x) - P(\xi = x) = F(x - 0)
  $$

- $$
  P(\xi \ge x) = 1 - P(\xi < x) = 1 - F(x - 0)
  $$

## 离散型随机变量及其分布

离散型随机变量：随机变量的所有可能取值是[有限多个或可列无限多个]()

### 分布列

设$\xi$是一个离散型随机变量，取值为$x_1, x_2, ...,  x_n,...,$且$P(\xi = x_k) = p_k(k = 1, 2, ...)$，则称$\{p_k\}$为随机变量$\xi$的概率分布列，简称分布列.

根据概率的性质，分布列满足：

- $$
  p_k \ge 0,k = 1, 2, ...
  $$

- $$
  \sum_{k = 1}^{\infty}p_k = 1
  $$

### 离散型随机变量的分布函数

![](C:\Users\Joker\Documents\TyporaFiles\Curriculum\概率论\image\离散型随机变量的分布函数.png)

### 常见的离散型随机变量

#### （0-1）分布（伯努利分布、两点分布）

随机变量X只可能取0、1两个值，其分布列为：
$$
P(X = k) = p^k(1 - p)^{1 - k} \\ 
k = 0,1 \quad (0 < p < 1)
$$

#### 二项分布

若试验E只有两种可能结果A和它的逆事件$\overline{A}$，则称E为[伯努利试验]().

设随机变量$\xi$表示n重伯努利试验中“成功”出现的次数，设每次成功的概率为p，则$\xi$的分布列为：
$$
p_k = P(\xi = k) = C_n^kp^k(1 - p)^{n - k} \\
(k = 0, 1, ..., n; 0 < p < 1)
$$
称$\xi$服从[二项分布]()，记为：
$$
\xi \sim b(n, p)
$$

#### 泊松分布

设随机变量X取值$0, 1, 2, ...$，且其分布列为：
$$
P(X = k) = \frac{\lambda^ke^{-\lambda}}{k!}
\quad k = 0,1,2,... \\
其中\lambda > 0是常数
$$
则称X服从参数为$\lambda$的泊松分布，记作：
$$
X \sim \pi(\lambda)
$$

##### 泊松定理

设随机变量X服从二项分布$B(n, p_n)$，又设$\lambda > 0$是一常数，n是任意正整数，若$np_n = \lambda$，则对任一固定的非负整数k有：
$$
\lim_{n \rightarrow \infty}P_n(X = k) = \lim_{n \rightarrow \infty}C_n^kp_n^k(1 - p_n)^{n - k} = \frac{\lambda^ke^{-\lambda}}{k!}
$$
上述定理表明当n很大，p很小$(np = \lambda)$时有以下近似式：
$$
C_n^kp^k(1 - p)^{n - k} \approx \frac{\lambda^ke^{-\lambda}}{k!} \quad (其中\lambda = np)
$$
即以n，p为参数的二项分布的概率值可以由参数为$\lambda = np$的泊松分布的概率值近似.

## 连续型随机变量及其分布

==定义== 对于随机变量X的分布函数$F(x)$，如果存在非负可积函数$f(x),x \in (-\infty, +\infty)$，使得对任意实数x，有
$$
F(x) = \int_{-\infty}^xf(t)dt = P(X \le x)
$$
则称X为[连续型随机变量]()，称$f(x)$为X的概率密度函数，简称为[概率密度]().

==注== 

- 连续型随机变量的分布函数在R上连续
- 连续型随机变量取任一指定实数值a的概率均为0，即：

$$
P(X = a) = 0
$$

- 对连续型随机变量X，有：

$$
\begin{aligned}
P(a \le X \le b) &= P(a < X \le b) \\
&= P(a \le X < b) \\
&= P(a < X < b)
\end{aligned}
$$

### 概率密度的性质

- $$
  f(x) \ge 0
  $$

- $$
  \int_{-\infty}^{+\infty}f(x)dx = 1
  $$

上述两条性质是判定一个$f(x)$是[某随机变量X的概率密度]()的充要条件.

- 对于任意实数$x_1, x_2(x_1 < x_2)$：

$$
P\{x_1 < X \le x_2\} = F(x_2) - F(x_1) = \int_{x_1}^{x_2}f(x)dx
$$

- 若$f(x)$在点x处连续，则有：

$$
F'(x) = f(x)
$$

### 常见的连续型随机变量

#### 均匀分布

若随机变量X的概率密度为：
$$
f(x) = 
\begin{cases}
\frac{1}{b - a}, \quad a \le x \le b \\
\\
0, \quad 其他
\end{cases}
$$
则称X在区间$(a, b)$上服从[均匀分布]()，记作
$$
X \sim U(a, b)
$$
X的分布函数为
$$
F(x) = 
\begin{cases}
0, \quad x < a \\
\\
\frac{x - a}{b - a}, \quad a \le x < b \\
\\
1, \quad x \ge b
\end{cases}
$$

#### 指数分布

若随机变量X具有概率密度：
$$
f(x) = 
\begin{cases}
\frac{1}{\theta}e^{-\frac{x}{\theta}}, \quad x > 0 \\
\\
0, \quad x \le 0
\end{cases} 
\quad \quad 其中\theta > 0为常数
$$
则称X服从参数为$\theta$的指数分布，其分布函数为：
$$
F(x) = 
\begin{cases}
1 - e^{-\frac{x}{\theta}}, \quad x > 0 \\
\\
0, \quad x \le 0
\end{cases}
$$

==说明== $E(X) = \theta$

##### 性质

###### 无记忆性

$$
P\{X > x_0 + \Delta x | X > x_0\} = P\{X > \Delta x\}
$$

证明：
$$
P\{X > x_0 + \Delta x | X > x_0\} = 
\frac{P\{(X > x_0 + 
\Delta x) \cap (X > x_0)\}}{P\{X > x_0\}} \\
= \frac{P\{X > x_0 + \Delta x\}}{P\{X > x_0\}} = \frac{e^{-\frac{x_0 + \Delta x}{\theta}}}{e^{-\frac{x_0}{\theta}}} = P\{X > \Delta x\}
$$
==另注== 

- 指数分布：唯一无记忆性的连续型分布
- 几何分布：唯一无记忆性的离散型分布

#### 正态分布

若连续型随机变量X的概率密度为
$$
f(x) = \frac{1}{\sqrt{2\pi}\sigma}e^{-\frac{(x - \mu)^2}{2 \sigma^2}}, \quad -\infty < x < \infty \\
其中\mu和\sigma(\sigma > 0)都是常数
$$
则称X服从参数为$\mu$和$\sigma$的正态分布或高斯分布，记作
$$
X \sim N(\mu, \sigma^2)
$$

##### 正态分布概率密度函数$f(x)$的性质

![image-20221016153313370](C:\Users\Joker\AppData\Roaming\Typora\typora-user-images\image-20221016153313370.png)

##### 标准正态分布

当$\mu = 0, \sigma = 1$时，$N(0, 1)$称为[标准正态分布]()
$$
概率密度函数：\varphi(x) = \frac{1}{\sqrt{2\pi}}e^{-\frac{x^2}{2}}, \quad -\infty < x < \infty \\
分布函数：\varPhi(x) = \frac{1}{\sqrt{2\pi}}\int_{-\infty}^x e^{-\frac{t^2}{2}}dt, \quad -\infty < x < \infty
$$
![image-20221016153814748](C:\Users\Joker\AppData\Roaming\Typora\typora-user-images\image-20221016153814748.png)

###### $\varphi(x),\varPhi(x)$的性质

- $$
  \varphi(0) = \frac{1}{\sqrt{2\pi}}, \quad \varPhi(0) = \frac{1}{2}
  $$

- $$
  \varphi(-x) = \varphi(x)
  $$

- $$
  \varPhi(-x) = 1 - \varPhi(x)
  $$

- 若正态分布$N(\mu, \sigma^2)$的分布函数为$F(x)$，则

$$
F(x) = \varPhi(\frac{x - \mu}{\sigma})
$$

该性质表明，可以用标准正态分布的分布函数$\varPhi(x)$计算其他正态分布的分布函数$F(x)$.

进而可以得到，若$X \sim N(\mu, \sigma^2)$，则
$$
F(x) = P\{\frac{X - \mu}{\sigma} \le \frac{x - \mu}{\sigma}\} = \varPhi(\frac{x - \mu}{\sigma}) \\
P\{x_1 < X \le x_2\} = F(x_2) - F(x_1) = \varPhi(\frac{x_2 - \mu}{\sigma}) - \varPhi(\frac{x_1 - \mu}{\sigma})
$$

###### $\varPhi(x)的计算$

![image-20221016154814428](C:\Users\Joker\AppData\Roaming\Typora\typora-user-images\image-20221016154814428.png)

##### $3\sigma$规则

当$X \sim N(0, 1)$时
$$
P(\vert X \vert \le 1) = 0.6826 \\
P(\vert X \vert \le 2) = 0.9544 \\
P(\vert X \vert \le 3) = 0.9974 \\
$$
当$X \sim N(\mu, \sigma^2)$时
$$
P(\vert X - \mu \vert \le \sigma) = 0.6826 \\
P(\vert X - \mu \vert \le 2\sigma) = 0.9544 \\
P(\vert X - \mu \vert \le 3\sigma) = 0.9974 \\
$$

## 离散型和连续型随机变量的比较

![image-20221016150822285](C:\Users\Joker\AppData\Roaming\Typora\typora-user-images\image-20221016150822285.png)

## 随机变量函数的分布 ==重点== 

若$X \sim N(\mu, \sigma^2)$，令$Y = \frac{X - \mu}{\sigma}$，则$Y \sim N(0, 1)$.

### X为连续型随机变量

若X为连续型随机变量，概率密度为$f_X(x)$，求$Y = g(X)$的概率密度$f_Y(x)$一般采用[分布函数法]()：

![image-20221016155702159](C:\Users\Joker\AppData\Roaming\Typora\typora-user-images\image-20221016155702159.png)

# 多维随机变量及其分布 ==重点==

## 边缘分布 ==重点==

- 离散型

$$
P\{X = x_i\} = \sum_{j = 1}^{\infty} p_{ij} = p_{i \cdot} \\
P\{Y = y_j\} = \sum_{i = 1}^{\infty} p_{ij} = p_{\cdot j}
$$

称$p_{i \cdot}, p_{\cdot j}$为边缘分布律

- 连续型

$$
f_X(x) = \int_{-\infty}^{\infty} f(x, y)dy \\
f_Y(y) = \int_{-\infty}^{\infty} f(x, y)dx
$$

称$f_X(x), f_Y(y)$为边缘概率密度

## 条件分布

### 

## 相互独立的随机变量 ==重点==

若随机变量$X, Y$相互独立，其等价条件为：
$$
F(x, y) = F_X(x) F_Y(y)
$$


- 若连续型随机变量$X, Y$相互独立，其等价条件为：

$$
f(x, y) = f_X(x) f_Y(y)
$$

- 若离散型随机变量$X, Y$相互独立，其等价条件为：

$$
P\{X = x_i, Y = y_j\} = P\{X = x_i\} P\{y = y_j\}
$$

## 两个随机变量的函数的分布 ==重点==

### $Z = X + Y$的分布

设$(X, Y)$是二维连续型随机变量，它具有概率密度$f(x, y)$，则$Z = X + Y$仍为连续型随机变量，其概率密度为：
$$
f_{X + Y}(z) = \int_{-\infty}^{\infty} f(z - y, y)dy \\
或 \quad f_{X + Y}(z) = \int_{-\infty}^{\infty} f(x, z - x)dx
$$
若$X, Y$相互独立，设$(X, Y)$关于$X, Y$的边缘密度分别为$f_X(x), f_Y(y)$，则上式可化为：
$$
f_{X + Y}(z) = \int_{-\infty}^{\infty} f_X(z - y)f_Y(y)dy \\
或 \quad f_{X + Y}(z) = \int_{-\infty}^{\infty} f_X(x)f_Y(z - x)dx
$$
上两式称为$f_X, f_Y$的[卷积公式]()

#### 正态随机变量的线性组合

设X，Y相互独立且$X \sim N(\mu_1, \sigma_1^2),\ Y \sim N(\mu_2, \sigma_2^2)$，则有：
$$
Z = X + Y \sim N(\mu_1 + \mu_2,\ \sigma_1^2 + \sigma_2^2) \\
aX + bY \sim N(a\mu_1 + b\mu_2,\ a^2\sigma_1^2 + b^2\sigma_2^2)
$$
更一般地，可以证明[有限个相互独立的正态随机变量的线性组合仍然服从正态分布]()。

### $M = \max\{X, Y\}$及$N = \min\{X, Y\}$的分布 ==常考==

- $M = \max\{ X, Y\}$的分布函数为：

$$
F_{max}(z) = F_X(z)F_Y(z)
$$

- $N = \min\{ X, Y \}$的分布函数为：

$$
F_{min}(z) = 1 - [1 - F_X(z)][1 - F_Y(z)]
$$

# 随机变量的数字特征 ==重点==

## 常用分布的数字特征总结

![image-20221121091152998](C:\Users\Joker\AppData\Roaming\Typora\typora-user-images\image-20221121091152998.png)

==纠正==：

对于二项分布$B(n, p)$，其分布律为：
$$
P(X = k) = C_n^kp^k(1 - p)^{n - k} \quad k = 0, 1, ..., n
$$

- 两点分布的方差推导：

$$
E(X^2) = E(X) = p \\
D(X) = E(X^2) - E^2(X) = p - p^2 = p(1 - p)
$$

- 指数分布的分布函数：

$$
F(x) = 1 - e^{-\frac{x}{\theta}} \quad (x > 0)
$$

## 数学期望

数学期望简称期望，又称均值

### 离散型随机变量的数学期望

$$
E(X) = \sum_{k = 1}^\infty x_kp_k \\
（级数绝对收敛）
$$

### 连续型随机变量的数学期望

$$
E(X) = \int_{-\infty}^{+\infty} xf(x)dx \\
（积分绝对收敛）
$$

### 随机变量函数的数学期望

设随机变量Y是随机变量X的函数：$Y = g(X) \quad (连续函数)$

- X为离散型随机变量

$$
E(Y) = E[g(X)] = \sum_{k = 1}^{\infty}g(x_k)p_k
$$

- X为连续型随机变量

$$
E(Y) = E[g(X)] = \int_{-\infty}^{+\infty}g(x)f(x)dx
$$

#### 多随机变量函数的数学期望

##### 离散型

![image-20221121103134888](C:\Users\Joker\AppData\Roaming\Typora\typora-user-images\image-20221121103134888.png)

##### 连续型

设Z是随机变量X，Y的函数：$Z = g(X, Y)$（连续函数），若二维随机变量$(X, Y)$的概率密度为$f(x, y)$，则有
$$
E(Z) = E[g(X, Y)] = \int_{-\infty}^{\infty} \int_{-\infty}^{\infty} g(x, y)f(x, y)dxdy
$$
特别的，令$Z = X$，则有：
$$
E(X) = \int_{-\infty}^{\infty} \int_{-\infty}^{\infty} xf(x, y)dxdy
$$

##### 由$(X, Y)$联合分布律或联合概率密度求X、Y的数学期望

![image-20221121102859097](C:\Users\Joker\AppData\Roaming\Typora\typora-user-images\image-20221121102859097.png)

### 条件数学期望

- 离散型

$$
E(X \vert Y = y_j) = \sum x_i p_{i \vert j}
$$

- 连续型

$$
E(X \vert Y = y) = \int_{-\infty}^{+\infty} x f_{X \vert Y}(x \vert y)dx
$$

### 数学期望的性质

- $$
  E(C) = C
  $$

- $$
  E(CX) = CE(X)
  $$

- $$
  E(X \pm Y) = E(X) \pm E(Y)
  $$

- 设$X, Y$相互独立，则

$$
E(XY) = E(X)E(Y)
$$

==注意== 该结论反之不一定成立

## 方差

$$
D(X) = Var(X) = E\{ [X - E(X)]^2 \}
$$

![image-20221121103324806](C:\Users\Joker\AppData\Roaming\Typora\typora-user-images\image-20221121103324806.png)

### 方差的计算

方差$D(X)$可以看做随机变量X的函数$g(X) = [X - E(X)]^2$的数学期望

![image-20221121111921646](C:\Users\Joker\AppData\Roaming\Typora\typora-user-images\image-20221121111921646.png)

[计算方差的简化公式]()：
$$
D(X) = E(X^2) - E^2(X)
$$

### 方差的性质

![image-20221121103644907](C:\Users\Joker\AppData\Roaming\Typora\typora-user-images\image-20221121103644907.png)

对于(3)有：
$$
D(X + Y) = D(X) + D(Y) + 2Cov(X, Y)
$$

当$X, Y$不相关时，$Cov(X, Y) = 0$，则有$D(X + Y) = D(X) + D(Y)$


## 协方差与相关系数 ==重点==

### 协方差

![image-20221121103822952](C:\Users\Joker\AppData\Roaming\Typora\typora-user-images\image-20221121103822952.png)

[计算协方差的简单公式]()：
$$
Cov(X, Y) = E(XY) - E(X)E(Y)
$$
![image-20221121104008425](C:\Users\Joker\AppData\Roaming\Typora\typora-user-images\image-20221121104008425.png)

#### 协方差的性质

![image-20221121104045799](C:\Users\Joker\AppData\Roaming\Typora\typora-user-images\image-20221121104045799.png)

### 相关系数

![image-20221121104137727](C:\Users\Joker\AppData\Roaming\Typora\typora-user-images\image-20221121104137727.png)

#### 相关系数的性质

- $\vert \rho_{XY} \vert \le 1$
- ![image-20221121104413895](C:\Users\Joker\AppData\Roaming\Typora\typora-user-images\image-20221121104413895.png)

==说明== 

 ![image-20221121104459787](C:\Users\Joker\AppData\Roaming\Typora\typora-user-images\image-20221121104459787.png)

#### [对“不相关性”和“相互独立”区别的说明]()

![image-20221121104643122](C:\Users\Joker\AppData\Roaming\Typora\typora-user-images\image-20221121104643122.png)

==特例== 二维正态随机变量X与Y相互独立与不相关是等价的

## 矩和协方差矩阵

### 原点矩&中心矩

![image-20221121105009276](C:\Users\Joker\AppData\Roaming\Typora\typora-user-images\image-20221121105009276.png)

### 协方差矩阵

![image-20221121105036445](C:\Users\Joker\AppData\Roaming\Typora\typora-user-images\image-20221121105036445.png)

### 相关矩阵

![image-20221121105102228](C:\Users\Joker\AppData\Roaming\Typora\typora-user-images\image-20221121105102228.png)

# 大数定律与中心极限定理

## 大数定律

### 切比雪夫不等式

设X为随机变量，$E(X) = \mu,\ D(X) = \sigma^2 < +\infty$，则对任意的正数$\varepsilon$，有

$$
P\{ \vert X - \mu \vert \ge \varepsilon \} \le \frac{\sigma^2}{\varepsilon^2}
$$

等价于：

$$
P\{ \vert X - \mu \vert < \varepsilon \} \ge 1 - \frac{\sigma^2}{\varepsilon^2}
$$

==说明== 

- 切比雪夫不等式只与随机变量X的期望和方差有关，与X的分布类型无关 
- 切比雪夫不等式给出了随机变量偏离期望的概率的下界，但通常该下界比较“保守”

### 三个常用的大数定律

依概率收敛：

![image-20221121101013732](C:\Users\Joker\AppData\Roaming\Typora\typora-user-images\image-20221121101013732.png)

#### 切比雪夫大数定律

![image-20221121101137355](C:\Users\Joker\AppData\Roaming\Typora\typora-user-images\image-20221121101137355.png)

#### 辛钦大数定律

![image-20221121101246680](C:\Users\Joker\AppData\Roaming\Typora\typora-user-images\image-20221121101246680.png)

==说明==

![image-20221121101307625](C:\Users\Joker\AppData\Roaming\Typora\typora-user-images\image-20221121101307625.png)

#### 伯努利大数定律

![image-20221121101329897](C:\Users\Joker\AppData\Roaming\Typora\typora-user-images\image-20221121101329897.png)

==说明==

![image-20221121101425802](C:\Users\Joker\AppData\Roaming\Typora\typora-user-images\image-20221121101425802.png)

## 中心极限定理

中心极限定理：随机变量和的分布收敛于正态分布的一类定理

### 三个常用的中心极限定理

#### 独立同分布中心极限定理

![image-20221121101753339](C:\Users\Joker\AppData\Roaming\Typora\typora-user-images\image-20221121101753339.png)

==说明==

![image-20221121101834010](C:\Users\Joker\AppData\Roaming\Typora\typora-user-images\image-20221121101834010.png)

#### 李雅普诺夫中心极限定理

![image-20221121102003263](C:\Users\Joker\AppData\Roaming\Typora\typora-user-images\image-20221121102003263.png)

#### 德莫弗-拉普拉斯中心极限定理 ==重点== （参考教材第五版P126，例1,2,3）

![image-20221121101903147](C:\Users\Joker\AppData\Roaming\Typora\typora-user-images\image-20221121101903147.png)

==说明==

![image-20221121101940425](C:\Users\Joker\AppData\Roaming\Typora\typora-user-images\image-20221121101940425.png)

# 样本与抽样分布

## 基本概念

### 经验分布函数

<img src="C:\Users\Joker\AppData\Roaming\Typora\typora-user-images\image-20230209143946115.png" alt="image-20230209143946115" style="zoom:80%;" />

<img src="C:\Users\Joker\AppData\Roaming\Typora\typora-user-images\image-20230209144025940.png" alt="image-20230209144025940" style="zoom:80%;" />

<img src="C:\Users\Joker\AppData\Roaming\Typora\typora-user-images\image-20230209144104957.png" alt="image-20230209144104957" style="zoom:80%;" />

### 用样本推断总体

![image-20230209144307269](C:\Users\Joker\AppData\Roaming\Typora\typora-user-images\image-20230209144307269.png) 

## 样本数字特征

### 常用统计量

- 样本均值

$$
\overline{X} = \frac{1}{n}\sum_{i = 1}^nX_i
$$

- 样本方差

$$
\begin{aligned}
S^2 &= \frac{1}{n - 1}\sum_{i = 1}^n(X_i - \overline{X})^2 \\
&= \frac{1}{n - 1}(\sum_{i = 1}^n X_i^2 - n\overline{X}^2)
\end{aligned}
$$

==注意== 分母为$n - 1$

- 样本标准差

$$
S = \sqrt{\frac{1}{n - 1}\sum_{i = 1}^n(X_i - \overline{X})^2}
$$

- 样本k阶（原点）矩

$$
A_k = \frac{1}{n}\sum_{i = 1}^n X_i^k \quad (k = 1, 2, ...)
$$

- 样本k阶中心矩

$$
B_k = \frac{1}{n}\sum_{i = 1}^n(X_i - \overline{X})^k \quad (k = 1, 2, ...)
$$

![image-20230209145305927](C:\Users\Joker\AppData\Roaming\Typora\typora-user-images\image-20230209145305927.png)

计算观察值即用$x_i$代替$X_i$

<img src="C:\Users\Joker\AppData\Roaming\Typora\typora-user-images\image-20230209145033967.png" alt="image-20230209145033967" style="zoom:80%;" />

## 正态总体的抽样分布

### U统计量及其分布

<img src="C:\Users\Joker\AppData\Roaming\Typora\typora-user-images\image-20230209150139260.png" alt="image-20230209150139260" style="zoom:80%;" />

<img src="C:\Users\Joker\AppData\Roaming\Typora\typora-user-images\image-20230209150158820.png" alt="image-20230209150158820" style="zoom:80%;" />

### $\chi^2$统计量及其分布

![image-20230209111950764](C:\Users\Joker\AppData\Roaming\Typora\typora-user-images\image-20230209111950764.png)

性质：

<img src="C:\Users\Joker\AppData\Roaming\Typora\typora-user-images\image-20230209150741573.png" alt="image-20230209150741573" style="zoom:80%;" />

==重要结论== （记忆，证明不要求）

若总体$X \sim N(\mu, \sigma^2)$，$X_1, X_2, ..., X_n$是它的一个样本，则统计量
$$
\chi^2 = \frac{(n - 1)S^2}{\sigma^2} \sim \chi^2(n - 1)
$$
称为$\chi^2$统计量

#### 上侧$\alpha$分位数

<img src="C:\Users\Joker\AppData\Roaming\Typora\typora-user-images\image-20230209154257869.png" alt="image-20230209154257869" style="zoom:80%;" />

<img src="C:\Users\Joker\AppData\Roaming\Typora\typora-user-images\image-20230209154526869.png" alt="image-20230209154526869" style="zoom:80%;" />

### T统计量及其分布

![image-20230209112037327](C:\Users\Joker\AppData\Roaming\Typora\typora-user-images\image-20230209112037327.png)

#### T分布的分位点

![image-20230209155606806](C:\Users\Joker\AppData\Roaming\Typora\typora-user-images\image-20230209155606806.png)

### F统计量及其分布

![image-20230209112124960](C:\Users\Joker\AppData\Roaming\Typora\typora-user-images\image-20230209112124960.png)

#### F分布的上侧$\alpha$分位数

<img src="C:\Users\Joker\AppData\Roaming\Typora\typora-user-images\image-20230209160204303.png" alt="image-20230209160204303" style="zoom:80%;" />

### 正态总体样本均值与样本方差的分布

设$X_1, X_2, ..., X_n$来自正态总体$X \sim N(\mu, \sigma^2)$，$\overline{X}$表示样本均值，$S^2$表示样本方差，则近似有：
$$
\overline{X} \sim N(\mu, \frac{\sigma^2}{n})
$$

==扩展== 若$E(X) = \mu, \ D(X) = \sigma^2$，实际上有：
$$
E(\overline{X}) = \mu \\
D(\overline{X}) = \frac{\sigma^2}{n}
$$

### $\Gamma$函数

<img src="C:\Users\Joker\AppData\Roaming\Typora\typora-user-images\image-20230209150628084.png" alt="image-20230209150628084" style="zoom:80%;" />

# 参数估计 ==重点==

## 点估计

点估计：构造合适的统计量，估计总体的未知参数

==注意== 估计值与估计量的区别

### 矩估计法

用样本均值估计总体均值：

设样本均值：
$$
\overline{X} = \frac{1}{n}\sum_{i = 1}^n X_i
$$
总体均值为$\mu$，总体均值估计量为$\hat{\mu}$，记$\hat{\mu} = \overline{X}$

#### 计算未知参数$\theta$的矩估计套路

1. $\mu = E(X) = g(\theta)$
2. 令$\mu = g(\theta) = \overline{X}$，解得$\hat{\theta} = h(\overline{X})$，称为$\theta$的估计量
3. 用样本观测值求出$\overline{X}$，代入$h(\overline{X})$，得到$\theta$的估计值

### 最大似然估计法

一个试验中，得到了一组样本观察值，则有理由相信这个观察值出现的概率最大。因此，考察未知参数$\theta$取何值时，这组样本观察值出现的概率最大，那么就用这个值作为$\theta$的（最大似然）估计值。

#### 计算未知参数$\theta$的最大似然估计套路

1. 写出似然函数（给定样本出现的概率）
2. 对似然函数取对数（方便求导）
3. 求导，令导函数等于0，反解出$\theta$，得到的即为$\theta$的估计值（如果是估计量则用随机变量表示）

<img src="C:\Users\Joker\AppData\Roaming\Typora\typora-user-images\image-20230208142834581.png" alt="image-20230208142834581" style="zoom:80%;" />

#### 似然估计的性质

<img src="C:\Users\Joker\AppData\Roaming\Typora\typora-user-images\image-20230209095816028.png" alt="image-20230209095816028" style="zoom:80%;" />

## 估计量的评估标准

### 无偏性

<img src="C:\Users\Joker\AppData\Roaming\Typora\typora-user-images\image-20230211202648568.png" alt="image-20230211202648568" style="zoom:80%;" />

- 不论总体X服从什么分布，当总体k阶矩存在时，样本k阶原点矩$A_k$是总体k阶原点矩的无偏估计。特别地，[样本均值$\overline{X}$是总体均值$E(X)$的无偏估计量。]()

## 区间估计

<img src="C:\Users\Joker\AppData\Roaming\Typora\typora-user-images\image-20230212113321212.png" alt="image-20230212113321212" style="zoom:80%;" />

- 区间估计要求根据样本给出未知参数的一个范围，并保证参数的真值以指定的较大概率属于这个范围。即以区间的形式给出未知参数的一个范围, 同时还给出此区间包含参数真值的可信程度。这种形式的估计称为区间估计。

- $1 - \alpha$称为[置信度或置信水平]()
- 置信度的理解：假设$1 - \alpha = 0.95$，则经过100次抽样得到的100个估计区间中约有95个包含了真实值。（以总体均值$\mu$的估计为例，$\mu$是确定的一个未知常数（不会变化），但每次抽样得到的样本均值$\overline{X}$都在变化）

### 构造置信区间的一般方法

<img src="C:\Users\Joker\AppData\Roaming\Typora\typora-user-images\image-20230210100749187.png" alt="image-20230210100749187" style="zoom:80%;" />

==注意== $\sigma$表示总体标准差，$S$表示样本标准差

### 单个正态总体参数的置信区间

<img src="C:\Users\Joker\AppData\Roaming\Typora\typora-user-images\image-20230212114324060.png" alt="image-20230212114324060" style="zoom:67%;" />

#### 均值$\mu$的置信区间

- 方差$\sigma^2$已知

由：
$$
\frac{\overline{X} - \mu}{\sigma/\sqrt{n}} \sim N(0, 1) \\

P\{ \vert \frac{\overline{X} - \mu}{\sigma/\sqrt{n}} \vert < Z_{\alpha / 2} \} = 1 - \alpha
$$
则有：
$$
P\{ \overline{X} - \frac{\sigma}{\sqrt{n}}Z_{\alpha / 2} < \mu  < \overline{X} + \frac{\sigma}{\sqrt{n}}Z_{\alpha / 2} \} = 1 - \alpha
$$
即置信度为$1 - \alpha$的置信区间为：
$$
(\overline{X} \pm \frac{\sigma}{\sqrt{n}}Z_{\alpha / 2})
$$

- 方差$\sigma^2$未知

由：
$$
T = \frac{\overline{X} - \mu}{S / \sqrt{n}} \sim t(n - 1) \\

P\{ -t_{\alpha / 2}(n - 1) < T < t_{\alpha / 2}(n - 1) \} = 1 - \alpha
$$
则有：
$$
P\{ \overline{X} - \frac{S}{\sqrt{n}}t_{\alpha / 2}(n - 1) < \mu < \overline{X} + \frac{S}{\sqrt{n}}t_{\alpha / 2}(n - 1) \} = 1 - \alpha
$$
由此得到$\sigma^2$未知时，$\mu$的置信度为$1 - \alpha$的置信区间为：
$$
(\overline{X} - \frac{S}{\sqrt{n}}t_{\alpha / 2}(n - 1), \ \overline{X} + \frac{S}{\sqrt{n}}t_{\alpha / 2}(n - 1))
$$
简写为：
$$
\begin{pmatrix}
\overline{X} \pm \frac{S}{\sqrt{n}}t_{\alpha / 2}(n - 1)
\end{pmatrix}
$$

#### 方差$\sigma^2$的置信区间

![image-20230210105732926](C:\Users\Joker\AppData\Roaming\Typora\typora-user-images\image-20230210105732926.png)

![image-20230210105748728](C:\Users\Joker\AppData\Roaming\Typora\typora-user-images\image-20230210105748728.png)

# 假设检验 ==重点==

## 假设检验的步骤

<img src="C:\Users\Joker\AppData\Roaming\Typora\typora-user-images\image-20230212120311478.png" alt="image-20230212120311478" style="zoom: 67%;" />

## 假设检验情况分类

![image-20230212120918362](C:\Users\Joker\AppData\Roaming\Typora\typora-user-images\image-20230212120918362.png)

![image-20230212121110347](C:\Users\Joker\AppData\Roaming\Typora\typora-user-images\image-20230212121110347.png)

































