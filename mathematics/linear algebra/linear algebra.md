# 常用公式&结论

- 看到方阵要联想到行列式

### 四次方差公式

$$
a^4-b^4=(a-b)*(a^3+a^2*b+a*b^2+b^3)
$$

### 矩阵的“因式分解”

若矩阵每行都有一个公因子，则该矩阵可被分解为“列向量 $\times$ 行向量”的形式：

$$
\begin{pmatrix}
a_1b_1 & a_1b_2 & a_1b_3 \\
a_2b_1 & a_2b_2 & a_2b_3 \\
a_3b_1 & a_3b_2 & a_3b_3
\end{pmatrix} = 
\begin{pmatrix}
a_1 \\
a_2 \\
a_3 \\
\end{pmatrix}
\begin{pmatrix}
b_1 & b_2 & b_3
\end{pmatrix} 
$$

#### 例题

已知矩阵：

$$
A = 
\begin{pmatrix}
1 & \frac{1}{2} & \frac{1}{3} \\
2 & 1 & \frac{2}{3} \\
3 & \frac{3}{2} & 1
\end{pmatrix}
$$

求$A^n$：

将矩阵A进行分解：

$$
A = 
\begin{pmatrix}
1 & \frac{1}{2} & \frac{1}{3} \\
2 & 1 & \frac{2}{3} \\
3 & \frac{3}{2} & 1
\end{pmatrix} = 
\begin{pmatrix}
1 \\
2 \\
3
\end{pmatrix}
\begin{pmatrix}
1 & \frac{1}{2} & \frac{1}{3}
\end{pmatrix}
$$

所以有：

$$
A^n = 
\begin{pmatrix}
1 \\
2 \\
3
\end{pmatrix}
[
\begin{pmatrix}
1 & \frac{1}{2} & \frac{1}{3}
\end{pmatrix}
\begin{pmatrix}
1 \\
2 \\
3
\end{pmatrix}
]
\cdots 
[
\begin{pmatrix}
1 & \frac{1}{2} & \frac{1}{3}
\end{pmatrix}
\begin{pmatrix}
1 \\
2 \\
3
\end{pmatrix}
]
\begin{pmatrix}
1 & \frac{1}{2} & \frac{1}{3}
\end{pmatrix} \\
=
3^{n-1} A
= 3^{n - 1} 
\begin{pmatrix}
1 & \frac{1}{2} & \frac{1}{3} \\
2 & 1 & \frac{2}{3} \\
3 & \frac{3}{2} & 1
\end{pmatrix}
$$

### 对$AB = 0$的讨论

- 若A，B都是方阵，对等式两边求行列式，可得：

$$
\vert AB \vert = \vert A \vert \vert B \vert = 0 \\
\therefore \vert A \vert = 0 \ 或 \ \vert B \vert = 0
$$

- 若有：

$$
A_{m \times n}B_{n \times l} = 0
$$

则$R(A) + R(B) \le n$

- 若A，B都是方阵，则有

$$
AB = 0, \ A可逆 \Rightarrow B = 0 \\
AB = 0, \ B可逆 \Rightarrow A = 0
$$

- 若$AB = 0$，则有

$$
A列满秩 \Rightarrow B = 0 \\
B行满秩 \Rightarrow A = 0
$$



- 将矩阵B拆分：

$$
A(b_1, b_2, ..., b_n) = 0
$$

此时[矩阵B中每一个列向量都是齐次线性方程$Ax = 0$的解]()，由此可以和齐次线性方程解的理论联系起来。

# 行列式

## 行列式的性质

### 性质1

行列式与它的转置行列式相等：
$$
\vert A^T \vert = \vert A \vert
$$

### 性质2

对换行列式的两行（列），行列式变号.

==推论== 若行列式有两行（列）完全相同，则该行列式等于0.

### 性质3

行列式的某一行（列）中所有元素都乘同一数k，等于用数k乘此行列式.

==推论== 行列式某一行（列）中所有元素的公因子可以提到行列式记号之外.

### 性质4

行列式中若有两行（列）对应元素成比例，则此行列式为0.

### 性质5

若行列式某行（列）元素都为两数之和，如：
$$
D = \begin{vmatrix}
a_{11} & a_{12} & \cdots & a_{1n} \\
\vdots & \vdots & & \vdots \\
a_{i1} + a_{i1}' & a_{i2} + a_{i2}' & \cdots & a_{in} + a_{in}' \\
\vdots & \vdots & & \vdots \\
a_{n1} & a_{n2} & \cdots & a_{nn}
\end{vmatrix}
$$
则有：
$$
D =
\begin{vmatrix}
a_{11} & a_{12} & \cdots & a_{1n} \\
\vdots & \vdots & & \vdots \\
a_{i1} & a_{i2} & \cdots & a_{in} \\
\vdots & \vdots & & \vdots \\
a_{n1} & a_{n2} & \cdots & a_{nn}
\end{vmatrix} + 
\begin{vmatrix}
a_{11} & a_{12} & \cdots & a_{1n} \\
\vdots & \vdots & & \vdots \\
a_{i1}' & a_{i2}' & \cdots & a_{in}' \\
\vdots & \vdots & & \vdots \\
a_{n1} & a_{n2} & \cdots & a_{nn}
\end{vmatrix}
$$

==注意== 和的行列式不可简单拆开，即
$$
\vert A + B \vert \ne \vert A \vert + \vert B \vert
$$

### 性质6

把行列式的某一行（列）的各元素乘同一数然后加到另一行（列）对应的元素上，行列式不变.

## 行列式展开

### 行列式按行（列）展开法则

行列式等于它的任一行（列）的各元素与其对应的代数余子式乘积之和，即：
$$
D = a_{i1}A_{i1} + a_{i2}A_{i2} + ... + a_{in}A_{in} \quad (i = 1,2,...,n) \\
或：D = a_{1j}A_{1j} + a_{2j}A_{2j} + ... + a_{nj}A_{nj} \quad (j = 1,2,...,n)
$$
==推论== 行列式某一行（列）的元素与另一行（列）的对应元素的代数余子式乘积之和等于零，即：
$$
a_{i1}A_{j1} + a_{i2}A_{j2} + ... + a_{in}A_{jn} = 0 \quad (i \ne j) \\
或：a_{1i}A_{1j} + a_{2i}A_{2j} + ... + a_{ni}A_{nj} = 0 \quad (i \ne j) 
$$
上述关于代数余子式的重要性质总结如下：
$$
\sum_{k = 1}^na_{ik}A_{jk} = 
\begin{cases}
D, \quad i = j\\
0, \quad i \ne j
\end{cases} \\

\sum_{k = 1}^na_{ki}A_{kj} = 
\begin{cases}
D, \quad i = j\\
0, \quad i \ne j
\end{cases}
$$

## 特殊行列式的计算

### 分块下三角行列式

设
$$
D = 
\begin{vmatrix}
a_{11} & \cdots & a_{1k} & & & & \\
\vdots & & \vdots & & 0 & & \\
a_{k1} & \cdots & a_{kk} & & & & \\
c_{11} & \cdots & c_{1k} & b_{11} & \cdots & b_{1n} \\
\vdots & & \vdots & \vdots & & \vdots \\
c_{n1} & \cdots & c_{nk} & b_{n1} & \cdots & b_{nn}
\end{vmatrix}, \\
D_1 = \det(a_{ij}) = 
\begin{vmatrix}
a_{11} & \cdots & a_{1k}\\
\vdots & & \vdots\\
a_{k1} & \cdots & a_{kk}
\end{vmatrix},\ 
D_2 = \det(b_{ij}) = 
\begin{vmatrix}
b_{11} & \cdots & b_{1n}\\
\vdots & & \vdots\\
b_{n1} & \cdots & b_{nn}
\end{vmatrix}
$$
则有：
$$
D = D_1D_2
$$

### 分块对角矩阵的行列式

对于分块对角矩阵
$$
A = 
\begin{vmatrix}
A_1 & & & \\
 & A_2 & & \\
 & & \ddots & \\
 & & & A_s
\end{vmatrix}
$$
具有如下性质：
$$
\vert A \vert = \vert A_1 \vert\vert A_2 \vert...\vert A_s \vert
$$

### 范德蒙德行列式

$$
\begin{vmatrix}
1 & 1 & \cdots & 1\\
x_1 & x_2 & \cdots & x_n\\
x_1^2 & x_2^2 & \cdots & x_n^2\\
\vdots & \vdots & & \vdots \\
x_1^{n-1} & x_2^{n-1} & \cdots & x_n^{n-1}\\
\end{vmatrix} = 
\prod_{n \ge i > j \ge 1}(x_i - x_j)
$$

## 行列式的常用结论

- 如果矩阵A，B为n阶方阵，则：

$$
\vert AB \vert = \vert A \vert\vert B \vert
$$

- 若A为可逆方阵，则有：

$$
\vert A^{-1} \vert = \vert A \vert ^{-1}
$$

# 矩阵及其运算

## 特殊矩阵

### 对称&反对称矩阵

#### 对称矩阵

$$
A^T = A
$$

#### 反对称矩阵

$$
A^T = -A
$$

### 对角矩阵

$$
\Lambda = 
\begin{pmatrix}
\lambda_1 & 0 & \cdots & 0 \\
0 & \lambda_2 & \cdots & 0 \\
\vdots & \vdots & & \vdots \\
0 & 0 & \cdots & \lambda_n
\end{pmatrix}
$$

对角阵也记作：
$$
\Lambda = diag(\lambda_1, \lambda_2, ... , \lambda_n)
$$

#### 对角矩阵的性质

对一个对角矩阵$\Lambda$有：
$$
\Lambda^a =
\begin{pmatrix}
\lambda_1^a & 0 & \cdots & 0 \\
0 & \lambda_2^a & \cdots & 0 \\
\vdots & \vdots & & \vdots \\
0 & 0 & \cdots & \lambda_n^a
\end{pmatrix}
$$

### 分块矩阵

将矩阵A用若干横线和竖线分成很多小矩阵（称为A的子块），以子块为元素的矩阵称为分块矩阵。分块矩阵的运算规则与普通矩阵的运算规则类似。

#### 分块矩阵的运算

##### 加法

对同型矩阵$A = (a_{ij})_{m \times n},B = (b_{ij})_{m \times n}$用相同的方法进行分块为$A = (A_{ij})_{s \times t},B = (B_{ij})_{s \times t}$，其中$A_{ij},B_{ij}$为同型矩阵，则
$$
A + B = (A_{ij} + B_{ij})_{s \times t}
$$

##### 数乘

将矩阵$A = (a_{ij})_{m \times n}$分块为$A = (A_{ij})_{s \times t}$，则
$$
kA = (kA_{ij})_{s \times t}
$$

##### 乘法

矩阵$A = (a_{ij})_{m \times n},B = (b_{ij})_{n \times l}$分别分块为$A = (A_{ij})_{s \times t},B = (B_{ij})_{t \times r}$，其中$A_{ij}$是$m_i \times n_j$矩阵，$B_{ij}$是$n_i \times l_j$矩阵，则
$$
C = AB = (C_{ij})_{s \times r}
$$
其中
$$
C_{ij} = A_{i1}B_{1j} + A_{i2}B_{2j} + ... + A_{it}B_{tj} \\
(i = 1,2,...,s; \quad j = 1,2,...,r)
$$

## 矩阵的运算

### 矩阵的线性运算

#### 加法

对同型矩阵$A = (a_{ij})_{s\times n},B = (b_{ij})_{s\times n}$，定义加法：
$$
A + B = (a_{ij} + b_{ij})_{s \times n}
$$

#### 数乘

数k与矩阵A的乘积定义为：
$$
kA = (ka_{ij})_{s \times n}
$$

### 矩阵的乘法

设$A = (a_{ij})_{s \times n}, B = (b_{ij})_{n \times m}$，则$AB = (c_{ij})_{s \times m}$，其中
$$
c_{ij} = \sum_{k = 1}^n a_{ik}b_{kj} \quad (i = 1,2,...,s;j = 1,2,...,m)
$$

#### 矩阵乘法满足的运算律

设A，B，C，为同型矩阵，k为数，则有：

- $(AB)C = A(BC)$
- $A(B + C) = AB + AC \ (左分配率) \\ (A + B)C = AC + AC \ (右分配率)$ 
- $k(AB) = (kA)B = A(kB)$

==注意== 矩阵乘法不满足交换律，即：
$$
AB \ne BA \\
(AB)^k \ne A^k B^k
$$

### 矩阵的转置

#### 矩阵转置满足的运算律

设A，B为矩阵，k为数，则有：

- $(A^T)^T = A$
- $(A + B)^T = A^T + B^T$
- $(AB)^T = B^T A^T$
- $(kA)^T = kA^T$

## 矩阵的初等变换与初等矩阵

### 矩阵的初等变换

==定义== 矩阵的下面三种变换称为矩阵的[初等行变换]()：

1. 对调两行（对调$i,j$两行，记作$r_i \harr r_j$）
2. 以非零数k乘以某一行的所有元素（第$i$行乘k，记作$r_i \times k$）
3. 把某一行所有元素的k倍加到另一行的对应元素上（第$j$行的k倍加到第$i$行上，记作$r_i + k \times r_j$）

矩阵的初等行变换与初等列变换统称为[初等变换]()。显然，三种初等变换都是可逆的，初等变换的逆变换仍为初等变换且变换类型相同。

### 矩阵的等价

若矩阵A经过有限次初等行变换可变为矩阵B，则称A，B行等价，记作$A \sim^r B$；若矩阵A经过有限次初等列变换可变为矩阵B，则称A，B列等价，记作$A \sim^c B$；若矩阵A经过有限次初等变换可变为矩阵B，则称A，B等价，记作$A \sim B$.

矩阵之间的等价关系具有如下性质：

- 反身性：$A \sim A$
- 对称性：若$A \sim B$，则$B \sim A$
- 传递性：若$A \sim B, \ B \sim C$，则$A \sim C$

### 重要的矩阵概念

#### 行阶梯形矩阵

设矩阵A满足以下两个条件：

1. 若矩阵有零行（每个元素都是零的行），则零行都在矩阵的最下方
2. 每个非零行的非零首元（第一个不是零的元素）都出现在上一行非零首元的右边，则称该矩阵为[行阶梯形矩阵]()

#### 行最简形矩阵

设矩阵A为行阶梯形矩阵，且满足以下两个条件：

1. 每个非零行的非零首元都为1
2. 每个非零行的非零首元所在的列的其他元素都是零，则称矩阵A为行最简阶梯形矩阵，简称为[行最简形矩阵]()

==注== 对任何矩阵A，总可以经过[有限次初等行变换]()把它们变为行阶梯形矩阵和行最简形矩阵。

#### 标准形

特点：标准型F的左上角是一个单位矩阵，其余元素全为零
$$
F = 
\begin{pmatrix}
E_r & O \\
O & O
\end{pmatrix}_{m \times n}
$$
==注==

- 任一矩阵A总可以经过[初等变换]()化为标准形
- 标准形由$m,n,r$三个数唯一确定，其中$r$就是行阶梯形矩阵中非零行的行数

### 初等矩阵

==定义== 由单位矩阵E经过[一次初等变换]()得到的方阵称为初等矩阵

- 把单位矩阵中第$i,j$两行对换（或第$i,j$两列对换），得到的初等矩阵记为$E(i,j)$
- 以数$k \ne 0$乘单位矩阵的第$i$行（或第$i$列），得到的初等矩阵记为$E(i(k))$
- 以k乘单位矩阵的第$j$行加到第$i$行上或以k乘单位矩阵的第$i$列加到第$j$列上，得到的初等矩阵记为$E(ij(k))$

#### 初等矩阵的性质

1. 初等矩阵均可逆
2. [n阶方阵A可逆的充要条件是存在有限个初等方阵$P_1, P_2, ..., P_l$，使$A = P_1 P_2 ... P_l$]()
3. A和B行等价的充要条件是存在m阶可逆矩阵P，使$PA = B$
4. A和B列等价的充要条件是存在n阶可逆矩阵Q，使$AQ = B$
5. A和B等价的充要条件是存在m阶可逆矩阵P及n阶可逆矩阵Q，使$PAQ = B$
6. 方阵A可逆的充要条件是A和单位矩阵E行等价

##### 定理1

设矩阵A是一个$m \times n$矩阵，对A施行一次[初等行变换]()相当于在A的[左边]()乘以相应的m阶初等矩阵；对A施行一次[初等列变换]()相当于在A的[右边]()乘以相应的n阶初等矩阵.

[初等矩阵都是可逆的，且其逆矩阵是同一类型的初等矩阵]()：
$$
E(i,j)^{-1} = E(i,j) \\
E(i(k))^{-1} = E(i(\frac{1}{k})) \\
E(ij(k))^{-1} = E(ij(-k))
$$

==扩展== 可以证明，矩阵
$$
A = 
\begin{pmatrix}
 & & & 1 \\
 & & 1 & \\
 & \ddots & & \\
 1 & & & 
\end{pmatrix}
$$

的逆是它本身，即有：

$$
A^2 = \begin{pmatrix}
 & & & 1 \\
 & & 1 & \\
 & \ddots & & \\
 1 & & & 
\end{pmatrix}
\begin{pmatrix}
 & & & 1 \\
 & & 1 & \\
 & \ddots & & \\
 1 & & & 
\end{pmatrix} = E
$$

##### 定理2

设矩阵A是一个$m \times n$矩阵，则存在行最简形矩阵B和m阶初等矩阵$P_1,P_2,...,P_s$满足
$$
P_1P_2...P_sA = B
$$

##### 定理3

设矩阵A是一个$m \times n$矩阵，则存在m阶初等矩阵$P_1,P_2,...,P_s$和n阶初等矩阵$Q_1,Q_2,...,Q_l$满足
$$
P_1P_2...P_sAQ_1Q_2...Q_l = F
$$
其中，F为A的标准形。

## 逆矩阵

==定义== 对于n阶方阵A，如果存在一个n阶方阵B，使得：
$$
AB = BA = E
$$
则称矩阵A是可逆的，并称矩阵B是A的逆矩阵，A的逆矩阵记作$A^{-1}$

### 伴随矩阵

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
称为矩阵A的伴随矩阵（[注意其中元素的顺序]()）

#### 伴随矩阵的性质

$$
AA^* = A^*A = \vert A \vert E \\
\vert A ^* \vert = \vert A \vert^{n-1}
$$

### 矩阵可逆的充要条件

矩阵A可逆的充要条件是$\vert A \vert \ne 0$，且有
$$
A^{-1} = \frac{1}{\vert A \vert}A^*
$$
其中$A^*$为矩阵A的伴随矩阵。

- 当$\vert A \vert = 0$时，称A为[奇异矩阵]()，否则称A为[非奇异矩阵]()。由此可得，A是可逆矩阵的充要条件是A为非奇异矩阵

==推论== 若$AB = E(或BA = E)$，则$B = A^{-1}$

### 逆矩阵的运算性质

- 若矩阵A可逆，则$A^{-1}$亦可逆，且$(A^{-1})^{-1} = A$

- 若矩阵A可逆，且$\lambda \ne 0$，则$\lambda A$亦可逆，且

$$
(\lambda A)^{-1} = \frac{1}{\lambda}A^{-1}
$$

- 若A，B为同阶可逆方阵，则AB亦可逆（[可逆矩阵的乘积仍为可逆矩阵]()），且
  $$
  (AB)^{-1} = B^{-1}A^{-1}
  $$

- 若A为可逆方阵，则有：

$$
\vert A^{-1} \vert = \vert A \vert ^{-1}
$$

证明：

$$
\begin{cases}
A^*A = \vert A \vert E \\
A^* = \vert A \vert A^{-1}
\end{cases}
\Rightarrow 
\begin{cases}
\vert A^* \vert \cdot \vert A \vert = \vert A \vert^n \\
\vert A^* \vert = \vert A \vert^n \cdot \vert A^{-1} \vert
\end{cases}
\Rightarrow 
\vert A^{-1} \vert = \vert A \vert ^{-1}
$$

- 若A为可逆矩阵，则$A^{-1}$可逆，且

$$
(A^T)^{-1} = (A^{-1})^T
$$

==推论== 可逆的对称矩阵的逆矩阵，仍为对称矩阵

证明：
$$
\begin{cases}
A^T = A \\
(A^T)^{-1} = (A^{-1})^T
\end{cases}
\quad \Rightarrow \quad
(A^{-1})^T = (A^T)^{-1} = A^{-1}
$$

- 若A为可逆矩阵，则$A^*$可逆，且

$$
(A^*)^{-1} = (A^{-1})^*
$$

==注意== 矩阵之和的逆不可简单拆开，即
$$
(A + B)^{-1} \ne A^{-1} + B^{-1}
$$

### 求二阶矩阵的逆

用“两调一除”的方法求二阶矩阵的逆：

先将矩阵A中的主对角元素调换其位置，再将副对角元素位置不换，加负号，最后用A的行列式$\vert A \vert$除矩阵A的每一个元素，即可得A的逆矩阵$A^{-1}$.

### 用初等变换求逆矩阵

#### 需了解的性质和定理

- 方阵A可逆的充分必要条件是存在有限个初等矩阵$P_1,P_2,...,P_l$，使$A = P_1P_2...P_l$
- 方阵A可逆的充分必要条件是$A \cong^r E$

#### 利用初等变换求逆矩阵的方法

当$\vert A \vert \ne 0$时，则由$A = P_1P_2...P_l$，得：
$$
P_l^{-1}P_{l-1}^{-1} ... P_1^{-1}A = E \\
P_l^{-1}P_{l-1}^{-1} ... P_1^{-1}E = A^{-1}\\
注：P_l^{-1}P_{l-1}^{-1} ... P_1^{-1}和A互逆
$$
对$n \times 2n$矩阵$(A \ E)$分块为$(A \vert B)$，则：
$$
P_l^{-1}P_{l-1}^{-1} ... P_1^{-1}(A,E) = (E, A^{-1})
$$
即，对矩阵$(A, E)$施行[初等行变换]()，当把A变成E的同时，原来的E就变成了$A^{-1}$

==注== 用此方法求逆矩阵的前提是矩阵可逆

#### 扩展1

对矩阵方程$AX = B$，其中A为n阶方阵，B为$n \times s$阶矩阵，如果A可逆，则$X = A^{-1}B$。当一系列初等行变换将A化为E的同时也将B化为了$A^{-1}B$，即有：
$$
P_l^{-1}P_{l-1}^{-1} ... P_1^{-1}(A,B) = (E, A^{-1}B)
$$
对于有n个未知数n个方程的线性方程组$Ax = b$，若增广矩阵$B = (A, b)$经初等行变换 可化为$(E,x)$时，则系数矩阵A可逆，且$x = A^{-1}b$为方程$Ax = b$的唯一解（向量）.

#### 扩展2

如果A经过一系列初等行变换变成B，则有可逆矩阵P，使得$PA = B$，则有：
$$
P (A \vert E) = (B \vert P) 
$$
即，当一系列初等行变换将A化为B的同时也将E化为了P.

### 分块对角矩阵的逆矩阵

设分块对角矩阵A，若$\vert A_i \vert \ne 0(i = 1, 2, ..., s)$，则
$$
\vert A \vert \ne 0,且 \\
A^{-1} = 
\begin{pmatrix}
A_1^{-1} & & & \\
 & A_2^{-1} & & \\
  & & \ddots & \\
  & & & A_s^{-1}
\end{pmatrix}
$$

另外，一般分块矩阵的逆矩阵可用待定系数法求得.

## 克拉默法则

对于含有n个未知数$x_1,x_2,...,x_n$的n个线性方程的方程组：
$$
\begin{cases}
a_{11}x_1 + a_{12}x_2 + ... + a_{1n}x_n = b_1 \\
a_{21}x_1 + a_{22}x_2 + ... + a_{2n}x_n = b_2 \\
\dots \dots \dots \\
a_{n1}x_1 + a_{n2}x_2 + ... + a_{nn}x_n = b_n \\
\end{cases}
$$
它的解可以用n阶行列式表示，即有：

[克拉默法则]()：如果上述线性方程组的系数矩阵A的行列式不等于零，即：
$$
\vert A \vert = 
\begin{vmatrix}
a_{11} & \dots & a_{1n}\\
\vdots & & \vdots\\
a_{n1} & \dots & a_{nn}
\end{vmatrix} 
\ne 0
$$
那么，[该方程组有唯一解]()：
$$
x_1 = \frac{\vert A_1 \vert}{\vert A \vert}, \quad x_2 = \frac{\vert A_2 \vert}{\vert A \vert}, \quad ... , x_n = \frac{\vert A_n \vert}{\vert A \vert}
$$
其中$A_j(j = 1,2,...,n)$是把系数矩阵A中第$j$列的元素用方程组右端的常数项代替后所得到的n阶矩阵，即：
$$
A_j = 
\begin{pmatrix}
a_{11} & \dots & a_{1,j-1} & b_1 & a_{1,j+1} & \dots & a_{1n}\\
\vdots & & \vdots & \vdots & \vdots & & \vdots \\
a_{n1} & \dots & a_{n,j-1} & b_n & a_{n,j+1} & \dots & a_{nn}\\
\end{pmatrix}
$$

### 关于线性方程组解的定理

#### 定理1

如果线性方程组的系数行列式$D \ne 0$，则方程组一定有解，且解是唯一的

#### 定理2

如果线性方程组无解或有解但不唯一，则它的系数行列式必为零

#### 定理3

如果齐次线性方程组：
$$
\begin{cases}
a_{11}x_1 + a_{12}x_2 + ... + a_{1n}x_n = 0 \\
a_{21}x_1 + a_{22}x_2 + ... + a_{2n}x_n = 0 \\
\dots \dots \dots \\
a_{n1}x_1 + a_{n2}x_2 + ... + a_{nn}x_n = 0 \\
\end{cases}
$$
的系数行列式$D \ne 0$，则该齐次线性方程组没有非零解（如果系数行列式$D = 0$，则它有且仅有一个零解）

#### 定理4

如果齐次线性方程组有非零解，则它的系数行列式D必为零

## 矩阵的秩

==定义== 在$m \times n$矩阵A中任取k行k列$k \le m, k \le n$，位于这k行k列交叉处的$k^2$个元素，不改变它们在A中所处的位置次序得到的k阶行列式，称为[矩阵A的k阶子式]()。若在矩阵A中有一个r阶子式D非零（此时低阶子式不可能都为零），且所有的$r + 1$阶子式（如果存在的话）都为零，则称D为[矩阵A的一个最高阶非零子式]()，称数r为矩阵A的秩，记作$R(A)$.

- 规定零矩阵的秩为零
- [$R(A^T) = R(A)$]()
- 可逆矩阵的秩等于阶数，称可逆（非奇异）矩阵为[满秩矩阵]()，称奇异矩阵为[降秩矩阵]()

### 矩阵秩的求法

==定理== 若$A \cong B$，则$R(A) = R(B)$

#### 初等变换求矩阵秩

用初等行变换把矩阵变成行阶梯形矩阵，行阶梯形矩阵中非零行的行数即为矩阵的秩.

### 矩阵秩的性质

- $0 \le R(A_{m \times n}) \le \min\{m, n\}$
- $R(A^T) = R(A)$
- 若$A \cong B$，则$R(A) = R(B)$
- 若P，Q可逆，则$R(PAQ) = R(A)$（可逆）
- $\max\{R(A), R(B)\} \le R(A, B) \le R(A) + R(B)$，特别当$B = b$时，$R(A) \le R(A, b) \le R(A) + 1$
- $R(A + B) \le R(A) + R(B)$
- $R(AB) \le \min\{R(A), R(B)\}$
- 若$A_{m \times n}B_{n \times l} = O$，则$R(A) + R(B) \le n$
- 若$A_{m \times n}B_{n \times l} = C$，且$R(A) = n$（列满秩矩阵），则$R(B) = R(C)$

==特殊情形== 矩阵乘法的消去律（$AB = 0$情形的讨论）

- 由$AB = 0$不能推出$A = 0 或 B = 0$
- 若A，B都是方阵，则有

$$
AB = 0, \ A可逆 \Rightarrow B = 0 \\
AB = 0, \ B可逆 \Rightarrow A = 0
$$

- 设$AB = 0$，则有

$$
A列满秩 \Rightarrow B = 0 \\
B行满秩 \Rightarrow A = 0
$$

### 矩阵秩与线性方程组解的关系

#### n元线性方程组$Ax = b$

- $$
  有解 \Harr R(A) = A(A, b)
  $$

- $$
  有唯一解 \Harr R(A) = R(A, b) = n \quad (n为未知数的个数). \\
  特别地，当方程个数等于未知数个数时，Ax = b有唯一解 \Harr \vert A \vert \ne 0 \quad (此时为克拉默法则)
  $$

- $$
  有无穷多个解 \Harr R(A) = R(A, b) < n
  $$

- $$
  无解 \Harr R(A) < R(A, b) \quad 或 \quad R(A) = R(A, b) - 1
  $$

#### 齐次线性方程组

齐次线性方程组$Ax = b$有非零解 $\Harr$ 方程组$R(A) < n$（n为未知数的个数，也是A的列数）

#### 矩阵方程

矩阵方程$AX = B$有解 $\Harr$ $R(A) = R(A, B)$

### 有关矩阵秩的重要结论

#### ==伴随矩阵的秩和原矩阵秩的关系==

设A为n阶矩阵，则有：
$$
\begin{aligned}
R(A) = n &: \quad R(A^*) = n \\
R(A) = n - 1 &: \quad R(A^*) = 1 \\
R(A) < n - 1 &: \quad R(A^*) = 0
\end{aligned}
$$

# 向量组的线性相关性

## 线性相关

### 线性相关的定义

给定向量组$A:\alpha_1, \alpha_2, ..., \alpha_m$，如果存在不全为零的数$k_1, k_2, ..., k_m$，使
$$
k_1\alpha_1 + k_2\alpha_2 + ... + k_m\alpha_m = O
$$
则称向量组A是[线性相关]()的，否则称它是[线性无关]()

==注==

1. 若$A:\alpha_1, \alpha_2, ..., \alpha_m$线性无关，则只有当$\lambda_1 = \lambda_2 = ... = \lambda_m = 0$时，才有$\lambda_1\alpha_1 + \lambda_2\alpha_2 + ... + \lambda_m\alpha_m = O$成立
2. 向量组只包含一个向量$\alpha$时，若$\alpha = O$则说$\alpha$线性相关；若$\alpha \ne O$，则说$\alpha$线性无关
3. 包含零向量的任何向量组都是线性相关的
4. 对于含有两个向量的向量组，它线性相关的充要条件是两向量的分量对应成比例，几何意义是两向量共线；三个向量线性相关的几何意义是三向量共面

### 定理

设向量组$A:\alpha_1, \alpha_2, ..., \alpha_m(m \ge 2)$，令$A = (\alpha_1, \alpha_2, ..., \alpha_m)$，则下列命题等价：

1. 向量组$A:\alpha_1, \alpha_2, ..., \alpha_m$线性相关
2. 线性方程组$Ax = O$有非零解
3. $R(A) < m$
4. 向量组A中[至少有一个向量]()能由其余$m - 1$个向量线性表示

与之相对有下列命题等价：

1. 向量组$A:\alpha_1, \alpha_2, ..., \alpha_m$[线性无关]()
2. 线性方程组$Ax = O$只有零解
3. $R(A) = m$
4. 向量组A中任何一个向量都不能由其余$m - 1$个向量线性表示

==相关结论==

- n维单位坐标向量组是线性无关的

### 线性相关的重要结论

1. 若向量组$A:\alpha_1, \alpha_2, ..., \alpha_m$线性相关，则向量组$B:\alpha_1, \alpha_2, ..., \alpha_m, \alpha_{m + 1}$也线性相关；反之，若向量组B线性无关，则向量组A也线性无关
2. m个n维向量组成的向量组，当$n < m$时一定线性相关（[向量个数大于维数一定线性相关]()）。特别地，$n + 1$个n维相关一定线性相关
3. 设向量组$A:\alpha_1, \alpha_2, ..., \alpha_m$线性无关，而向量组$B:\alpha_1, \alpha_2, ..., \alpha_m, \beta$线性相关，则向量$\beta$必能由向量组A线性表示，且表示式是唯一的
4. 设

$$
\alpha_j = 
\begin{pmatrix}
a_{1j} \\
a_{2j} \\
\vdots \\
a_{rj}
\end{pmatrix}, \quad
\beta_j = 
\begin{pmatrix}
a_{1j} \\
a_{2j} \\
\vdots \\
a_{rj} \\
a_{r+1, j}
\end{pmatrix}, \quad
(j = 1,2,...,m)
$$

即$\alpha_j$添上一个分量后得向量$\beta_j$，若向量组$A:\alpha_1, \alpha_2, ..., \alpha_m$线性无关，则向量组$B:\beta_1, \beta_2, ..., \beta_m$也线性无关；反之，若向量组B线性相关，则向量组A也线性相关

==注== 结论1可推广为：一个向量组若有线性相关的部分组，则该向量组必线性相关。特别地，含有零向量的向量组必线性相关；反之，若一个向量组线性无关，则它的任何部分都线性无关

## 向量组的秩

### 向量组的秩和最大线性无关组

==定义== 设有向量组A，如果在A中能选出r个向量$A_0:\alpha_1, \alpha_2, ..., \alpha_r$，满足

1. 向量组$A:\alpha_1, \alpha_2, ..., \alpha_r$线性无关
2. 向量组A中任意$r + 1$个向量（如果存在的话）都线性相关

则称向量组$A_0$是向量组A的一个[最大线性无关向量组]()（简称[最大无关组]()）。最大无关组所含向量的个数r称为[向量组的秩]()，记作$R_A$.

==注== 

- 只含零向量的向量组没有最大无关组，规定它的秩为0
- 最大无关组不唯一
- 向量组与它的最大无关组等价

#### 最大无关组的等价定义

设有向量组$A_0:\alpha_1, \alpha_2, ..., \alpha_r$是向量组A的一个部分组，且满足：

1. 向量组$A_0:\alpha_1, \alpha_2, ..., \alpha_r$线性无关
2. 向量组A的任意向量都能由向量组$A_0$线性表示

则向量组$A_0$是向量组A的一个[最大无关组]()

### 矩阵与向量组秩的关系

矩阵的秩等于它的列向量组的秩，也等于它的行向量组的秩，即：
$$
矩阵的秩 = 矩阵列向量组的秩 = 矩阵行向量组的秩
$$
若$D_r$是矩阵A的一个最高阶非零子式，则$D_r$所在的r列即为A的列向量组的一个最大无关组，$D_r$所在的行即为A的行向量组的一个最大无关组

### 向量组秩的重要结论

#### 定理1

向量b能由向量组$\alpha_1, \alpha_2, ..., \alpha_m$线性表示的充要条件是
$$
R(\alpha_1, \alpha_2, ..., \alpha_m) = R(\alpha_1, \alpha_2, ..., \alpha_m, b)
$$

#### 定理2

向量组$B:\beta_1, \beta_2, ..., \beta_s$能由向量组$A: \alpha_1, \alpha_2, ..., \alpha_m$线性表示的充要条件是
$$
R(\alpha_1, \alpha_2, ..., \alpha_m) = R(\alpha_1, \alpha_2, ..., \alpha_m, \beta_1, \beta_2, ..., \beta_s)
$$
==推论== 向量组$A: \alpha_1, \alpha_2, ..., \alpha_m$与向量组$B:\beta_1, \beta_2, ..., \beta_s$

等价的充要条件是
$$
R(\alpha_1, \alpha_2, ..., \alpha_m) = 
R(\beta_1, \beta_2, ..., \beta_s) = 
R(\alpha_1, \alpha_2, ..., \alpha_m, \beta_1, \beta_2, ..., \beta_s)
$$

（向量组等价：若向量组A，B等价，则A，B可相互线性表示）

#### 定理3

若向量组$B:\beta_1, \beta_2, ..., \beta_s$能由向量组$A: \alpha_1, \alpha_2, ..., \alpha_m$线性表示，则
$$
R(\beta_1, \beta_2, ..., \beta_s) \le
R(\alpha_1, \alpha_2, ..., \alpha_m)
$$

#### 定理4

向量组$\alpha_1, \alpha_2, ..., \alpha_m$线性相关的充要条件是$R(\alpha_1, \alpha_2, ..., \alpha_m) < m$；向量组线性无关的充要条件是$R(\alpha_1, \alpha_2, ..., \alpha_m) = m$

## 线性方程组解的结构

==定理== 若矩阵$A_{m \times n}$的秩$R(A) = r$，则齐次线性方程组$Ax = 0$解集S的秩$R_S = n - r$

### 齐次线性方程组

齐次线性方程组的解集的最大无关组称为该齐次线性方程组的[基础解系]()

#### 齐次线性方程组解向量的性质

- 若$x_1 = \xi_1, x_2 = \xi_2$是齐次线性方程组$Ax = 0$的解，则$x = \xi_1 + \xi_2$也是$Ax = 0$的解
- 若$x_1 = \xi_1$是齐次线性方程组$Ax = 0$的解，则$x = k\xi \ (k \in R)$也是$Ax = 0$的解

#### 齐次线性方程组的基础解系

对齐次线性方程组$Ax = 0$，设$R(A) = r$，则A的行最简形矩阵为：

$$
B = 
\begin{pmatrix}
1 & \dots & 0 & b_{11} & \dots & b_{1, n - r} \\
\vdots & & \vdots & \vdots & & \vdots \\
0 & \dots & 1 & b_{r1} & \dots & b_{r, n - r} \\
0 & & & \dots & & 0 \\
\vdots & & & & & \vdots \\
0 & & & \dots & & 0 \\
\end{pmatrix}
$$

则$Ax = 0$的基础解系为：

$$
\xi_1 = 
\begin{pmatrix}
-b_{11} \\
\vdots \\
-b_{r1} \\
1 \\
0 \\
\vdots \\
0
\end{pmatrix}, \quad 
\xi_2 = 
\begin{pmatrix}
-b_{12} \\
\vdots \\
-b_{r2} \\
0 \\
1 \\
\vdots \\
0
\end{pmatrix}, \quad 
\dots, \quad 
\xi_{n - r} = 
\begin{pmatrix}
-b_{1, n - r} \\
\vdots \\
-b_{r, n - r} \\
0 \\
0 \\
\vdots \\
1
\end{pmatrix}
$$

则齐次线性方程组$Ax = 0$的通解为：

$$
x = k_1\xi_1 + k_2\xi_2 + \dots + k_{n - r}\xi_{n - r} \quad (k_i \in R)
$$

==易错== 写出通解后要注意带上任意实数$k_i$的范围

### 非齐次线性方程组

非齐次线性方程解的结构：

非齐次方程的通解 = 对应齐次方程的通解 + 非齐次方程的一个特解

即：

$$
x = k_1\xi_1 + k_2\xi_2 + \dots + k_{n - r}\xi_{n - r} + \eta^*  \quad (k_i \in R)
$$

其中，$\eta^*$为非齐次方程的一个特解

#### 非齐次线性方程组解的性质

- 若$x_1 = \eta_1,\ x_2 = \eta_2$都是非齐次线性方程组$Ax = b$的解，则$x = \eta_1 - \eta_2$是对应的齐次线性方程组$Ax = 0$的解
- 若$x = \eta$是非齐次线性方程组$Ax = b$的解，$x = \xi$是对应的齐次线性方程组$Ax = 0$的解，则$x = \eta + \xi$是$Ax = b$的解

# 相似矩阵及二次型

## 向量的内积、长度及正交性

==定义== 设n维向量$e_1, e_2, ..., e_r$是向量空间V的一个基，若$e_1, e_2, ..., e_r$两两正交且都是单位向量，则称$e_1, e_2, ..., e_r$是V的一个[标准正交基]()

### 正交矩阵

$$
A^TA = E \quad (即A^{-1} = A^T)
$$

#### 正交矩阵的判定

- 方阵A为正交矩阵的充要条件是：A的列向量都是单位向量，且两两正交

#### 正交矩阵的性质

- 若A为正交矩阵，则$A^{-1} = A^T$也是正交矩阵，且$\vert A \vert = 1或(-1)$，进而可得[正交矩阵A的特征值只能取$1或-1$]()
- 若A，B都是正交矩阵，则AB也是正交矩阵
- 对正交变换$y = Px$，有

$$
\parallel y \parallel = \sqrt{y^Ty} = \sqrt{x^TP^TPx} = \sqrt{x^Tx} = \parallel x \parallel
$$

说明[经过正交变换向量长度保持不变]()

### 基的标准正交化

将基$a_1, ..., a_r$标准正交化，取

$$
\begin{aligned}
b_1 &= a_1, \\
b_2 &= a_2 - \frac{[b_1, a_2]}{\parallel b_1 \parallel ^2}b_1, \\
 & \cdots \cdots \cdots\\
b_r &= a_r - \frac{[b_1, a_r]}{\parallel b_1 \parallel ^2}b_1 - \frac{[b_2, a_r]}{\parallel b_2 \parallel ^2}b_2 - ... - \frac{[b_{r - 1}, a_r]}{\parallel b_{r - 1} \parallel ^2}b_{r - 1}
\end{aligned}
$$

然后将正交向量组$b_1, b_2, ..., b_r$单位化：

$$
\begin{aligned}
e_1 &= \frac{b_1}{\parallel b_1 \parallel}, \\
e_2 &= \frac{b_2}{\parallel b_2 \parallel}, \\
& \cdots \cdots \cdots \\
e_r &= \frac{b_r}{\parallel b_r \parallel}
\end{aligned}
$$

得到标准正交基.

## 方阵的特征值与特征向量

对于矩阵A，其[特征方程]()为：

$$
\vert A - \lambda E \vert = 0
$$

### 特征值的性质

- 设n阶矩阵$A = (a_{ij})$的特征值为$\lambda_1, \lambda_2, ..., \lambda_n$，则有：

A的[特征多项式]()：
$$
f(\lambda) = \vert A - \lambda E \vert = (\lambda_1 - \lambda)(\lambda_2 - \lambda)...(\lambda_n - \lambda) \\
$$
==矩阵的迹==：
$$
\lambda_1 + \lambda_2 + ... + \lambda_n = a_{11} + a_{22} + ... + a_{nn} 
$$
==矩阵行列式与特征值的关系==：
$$
\lambda_1 \lambda_2 ... \lambda_n = \vert A \vert
$$
由此还可推知A是可逆矩阵的充要条件是它的[n个特征值全不为零]()

- 若$\lambda$是A的特征值，则$\lambda^k$是$A^k$的特征值（特别的，[当A可逆时，$\frac{1}{\lambda}$是$A^{-1}$的特征值]()）；$\varphi(\lambda)$是$\varphi(A)$的特征值（其中$\varphi(\lambda) = a_0 + a_1\lambda + ... + a_m\lambda^m$是$\lambda$的多项式，$\varphi(A) = a_0E + a_1A + ... + a_mA^m$是[矩阵A的多项式]()）

### 特征值的相关定理

- 设$\lambda_1, \lambda_2, ..., \lambda_m$是方阵A的m个特征值，$p_1, p_2, ..., p_m$依次是与之对应的特征向量，若$\lambda_1, \lambda_2, ..., \lambda_m$互不相等，则$p_1, p_2, ..., p_m$线性无关（特征向量忠于特征值）

==推论== 设$\lambda_1, \lambda_2$是方阵A的两不同特征值，$xi_1, xi_2, ..., \xi_s$和$\eta_1, \eta_2, ..., \eta_t$分别是对应于$\lambda_1,\lambda_2$的线性无关的特征向量，则$xi_1, xi_2, ..., \xi_s, \eta_1, \eta_2, ..., \eta_t$线性无关

## 相似矩阵
$$
P^{-1}AP = B \quad （P为可逆矩阵）
$$
矩阵A，B相似

### 相关定理

- 若n阶矩阵A和B相似，则A与B的特征多项式相等，从而A与B的[特征值相同]().

==推论== 若n阶矩阵A与对角矩阵
$$
\Lambda = 
\begin{pmatrix}
\lambda_1 & & & \\
& \lambda_2 & & \\
& & \ddots & \\
& & & \lambda_n
\end{pmatrix}
$$
相似，则$\lambda_1, \lambda_2, ..., \lambda_n$是A的n个特征值

- 由$\lambda_1 \lambda_2 ... \lambda_n = \vert A \vert$知相似变换下矩阵的行列式不变

### 矩阵相似的判定

- 若矩阵A，B都和同一个对角矩阵$\varLambda$相似，则A，B相似.

### 对角化条件

n阶矩阵A与对角矩阵相似（即A能对角化）的充要条件是[A有n个线性无关的特征向量]()。

==推论== 若n阶矩阵A的[n个特征值互不相等]()，则A与对角矩阵相似（[反之不一定成立]()）

## 对称矩阵的对角化

### 对称矩阵特征值与特征向量的性质

#### 性质1

对称矩阵的特征值为实数

#### 性质2

设$\lambda_1, \lambda_2$是[对称矩阵]()A的两个特征值，$p_1, p_2$是对应的特征向量.若$\lambda_1 \ne \lambda_2$，则$p_1, p_2$正交

==注意== 非对称矩阵不同特征值对应的特征向量线性无关，但不一定正交

### 定理（P128）

设A为n阶[对称矩阵]()，则必有[正交矩阵]()P，使[$P^{-1}AP = P^TAP = \Lambda$]()，其中$\Lambda$是以A的n个特征值为对角元的对角矩阵

==推论== 设A为n阶对称矩阵，$\lambda$是A的特征方程的k重根（即k重特征值），则矩阵$A - \lambda E$的秩$R(A - \lambda E) = n - k$（$R(A - \lambda E) = R(\Lambda - \lambda E)$，两矩阵相似，秩相等），从而对应特征值$\lambda$恰有k个线性无关的特征向量

### ==对称矩阵对角化的步骤==

1. 求出A的全部互不相等的特征值$\lambda_1, ..., \lambda_s$，它们的重数依次为$k_1, ..., k_s(k_1 + ... + k_s = n)$
2. 对每个$k_i$重特征值$\lambda_i$，求方程$(A - \lambda_i E)x = 0$的基础解系，得$k_i$个线性无关的特征向量.再把它们正交化、单位化，得$k_i$个两两正交的单位特征向量.因$k_1 + ... + k_s = n$，故总共可得到n个两两正交的单位特征向量
3. 把这n个两两正交的单位特征向量构成正交矩阵P，便有[$P^{-1}AP = P^TAP = \Lambda$]()。[注意$\Lambda$中对角元的排列次序应与P中列向量的排列次序相对应]()

### ==利用对角矩阵计算矩阵的n次方==

若矩阵A与对角矩阵$\Lambda$相似，且有$P^{-1}AP = \Lambda$，则
$$
A^n = P^{-1}AP \cdot P^{-1}AP \dots P^{-1}AP \\
= P^{-1} \varLambda^n P
$$
（对角矩阵n次方的计算）其中，设对角矩阵$\Lambda$：
$$
\Lambda = 
\begin{pmatrix}
\lambda_1 & & & \\
& \lambda_2 & & \\
& & \ddots & \\
& & & \lambda_r
\end{pmatrix}
$$
则有：
$$
\Lambda^n = 
\begin{pmatrix}
\lambda_1^n & & & \\
& \lambda_2^n & & \\
& & \ddots & \\
& & & \lambda_r^n
\end{pmatrix}
$$
## 二次型及其标准形

### 定义

#### 标准形
$$
f(x) = k_1y_1^2 + k_2 y_2^2 + ... + k_n y_n^2
$$
将这种只含平方项的二次型称为二次型的[标准形]()（或法式）

#### 规范形

若标准形的系数$k_1, k_2, ..., k_n$只在$0, 1, -1$内取值，即有
$$
f(x) = y_1^2 + ... + y_p^2 - y_{p + 1}^2 - ... - y_r^2
$$
则称上式为二次型的[规范形]()

### 定理

任给二次型
$$
f = \sum_{i, j = 1}^n a_{ij}x_i x_j (a_{ij} = a_{ji})
$$
总有[正交变换$x = Py$]()，使$f$化为标准形
$$
f = \lambda_1 y_1^2  + \lambda_2 y_2^2 + ... + \lambda_n y_n^2
$$
其中$\lambda_1, \lambda_2, ..., \lambda_n$是$f(x)$的矩阵$A = (a_{ij})$的特征值

==注意== 通过普通可逆变换得到的标准形的系数不一定是原矩阵的特征值

==推论== 任给n元二次型$f(x) = x^TAx(A^T = A)$，总有可逆变换$x = Cz$，使$f(Cz)$为规范型.

## 正定二次型

==定义== 设二次型$f(x) = x^TAx$，若对任何$x \ne 0$，都有$f(x) > 0$（显然$f(0) = 0$，则称$f(x)$为[正定二次型]()，并称对称矩阵A是正定的；若对任何$x \ne 0$，都有$f(x) < 0$，则称$f(x)$为负定二次型，并称对称矩阵A是负定的.

==注意== 正定矩阵一般默认为对称矩阵.

==惯性定理== 设二次型$f(x) = x^TAx$的秩为r，且有两个可逆变换
$$
x = Cy, \quad x = Pz
$$
使得
$$
f = k_1y_1^2 + k_2y_2^2 + ... + k_ry_r^2 \quad (k_i \ne 0) \\
f = \lambda_1z_1^2 + \lambda_2z_2^2 + ... + \lambda_rz_r^2 \quad (\lambda_i \ne 0)
$$
则$k_1, ..., k_r$中正数的个数与$\lambda_1, ..., \lambda_r$中正数的个数相等.

==说明== 二次型的标准形中正系数的个数称为二次型的[正惯性系数]()，负系数的个数称为[负惯性系数]()

### 正定二次型的判定

- n元二次型$f(x) = x^TAx$为正定的充要条件是：它的标准形的n个系数全为正，即它的规范形的n个系数全为1，亦即它的正惯性指数等于n.

==推论== 对称矩阵A为正定的充要条件是：[A的特征值全为正]().

- ==赫尔维茨定理== 对称矩阵A为正定的充要条件是：[A的各阶主子式都为正]()，即
$$
a_{11} > 0, \
\begin{vmatrix}
a_{11} & a_{12} \\
a_{21} & a_{22}
\end{vmatrix} > 0, \
\cdots, \
\begin{vmatrix}
a_{11} & \cdots & a_{1n} \\
\vdots & & \vdots \\
a_{n1} & \cdots & a_{nn} 
\end{vmatrix} > 0
$$
对称矩阵A为负定的充要条件是：奇数阶主子式为负，偶数阶主子式为正，即
$$
(-1)^r
\begin{vmatrix}
a_{11} & \cdots & a_{12} \\
\vdots & & \vdots \\
a_{r1} & \cdots & a_{rr}
\end{vmatrix} > 0 
\quad (r = 1, 2, ..., n)
$$











