### 考试题型

- 判断，10 * 1
- 填空，10 * 2
- 选择，10 * 2
- 计算，3 * 10
- 证明，2 * 10

9.4范式不考

### 重要知识点

- 蕴含等值式

$$
\alpha \rightarrow \beta \quad \Harr \quad \neg \alpha \or \beta
$$

$$
\neg(P \and Q) \quad \Harr \quad \neg P \or \neg Q \quad \Harr \quad P \rightarrow \neg Q
$$

- 判断命题的类型 & 等值演算：重言型，矛盾型，可满足型

- ==重要== 结点的度：有向图（出度，入度），无向图

- ==重要== 同构

- ==重要== 树和树叶：结点，定义

- ==重要== 判断映射类型

- ==重要== 证明一个代数系统是群
- ==重要== 阿贝尔群的定义
- 子群的判别
- 封闭，单位元，逆元
- ==重要== 幂集：集合间的关系
- ==重要== 笛卡尔集
- ==重要== 关系：定义（笛卡尔集的子集），关系的性质，闭包的理解
- ==非常重要== 关系的性质与闭包运算：判断关系的性质
- ==重要== 等价关系：自反，对称，可传递（如何判断）
- ==重要== 偏序：全序，定义，判断
- ==重要== 分划：两个条件，等价类

## 证明题

### ==重要考点== 证明代数系统是群

群需要满足的条件：

1. 运算满足结合律（在此之前还要证明运算是[封闭的]()）
2. 存在单位元
3. 任何元素都存在逆元

### 证明函数是双射

即证明：

1. 函数是内射
2. 函数是满射（值域中的所有元素，在定义域中都有元素对应）

### 证明关系为等价关系

即证明：

1. 是自反的
2. 是对称的
3. 是可传递的

# 知识点

## 重要公式

### 等价式的等值转换

$$
P \harr Q \Harr (P \and Q) \or (\neg P \and \neg Q) \\
\Harr (P \rightarrow Q) \and (Q \rightarrow P) 
$$

### 蕴含等值式

$$
\alpha \rightarrow \beta \quad \Harr \quad \neg \alpha \or \beta
$$

$$
\neg(P \and Q) \quad \Harr \quad \neg P \or \neg Q \quad \Harr \quad P \rightarrow \neg Q
$$

### 幂集的基数

若A是有限集，且$\#A = n$，则有$\#2^A = 2^{\#A} = 2^n$

### 笛卡尔积的基数

$$
\#(A \times B) = \#A \times \#B
$$

==另注== 集合A上不同关系的个数
$$
\#(2^{A \times A}) = 2^{\#(A \times A)} = 2^{(n^2)}
$$

### 从集合A到集合B函数的数量

记$B^A = \{ f \vert f: A \rightarrow B \}$，则$\#(B^A) = (\#B)^{\#A}$

### 完全图的边数

$$
边数m = C_n^2 = \frac{n(n - 1)}{2}
$$

其中，n为完全图的结点数。

==另注== n个结点的图G和其补图$\overline{G}$的边数之间存在如下关系：
$$
\#E(G) + \#E(\overline{G}) = \frac{n(n - 1)}{2}
$$

### 图的数量关系

- 结点的度之和

$$
\sum_{i = 1}^ndeg(v_i) = 2m
$$

### 树的数量关系

- 结点的度之和

$$
\sum_{i = 1}^ndeg(v_i) = 2m
$$

- 边数 = 节点数 - 1（树独有的性质，与环相对）

$$
m = n - 1
$$

## 重要定理

- 若$f: A \rightarrow B,\ \#A = \#B$，且$f$为满射，则$f$是双射。

### 子群的判别

设$<G;*>$是一个群，H是G的非空子集，若：

1. 对于任意的$a, b \in H$，有$a * b \in H$（运算封闭）
2. 对任意的$a \in H$，有$a^{-1} \in H$（存在单位元和逆元）

则$<H;*>$是$<G;*>$的子群。

### 判定哈密尔顿图的[充分]()条件

设G是具有n（$n \ge 3$）个结点的图，若G中任意两个不相邻的结点度数之和大于或等于n，则G是哈密尔顿图。

### 判定欧拉图的充要条件

一连通图G为欧拉图的充要条件是G的[每一结点的度均为偶数]()。

### 复合函数的性质

- 若f和g都是内射，则$g \cdot f$也是内射
- 若f和g都是满射，则$g \cdot f$也是满射
- 若f和g都是双射，则$g \cdot f$也是双射

==重点== 以下定理非常重要：

若$f: A \rightarrow B,\ g: B \rightarrow C$

- 若$g \cdot f$是内射，则f是内射
- 若$g \cdot f$是满射，则g是满射
- 若$g \cdot f$是双射，则f是内射，g是满射

# 第一章 集合

## 集合

### 常见集合的表示符号

<img src="C:\Users\Joker\AppData\Roaming\Typora\typora-user-images\image-20230617205813748.png" alt="image-20230617205813748" style="zoom:50%;" />

==易混==

- $Nm(m \ge 1): \{ 1, 2, 3, ..., m \}$
- $Zm(m \ge 1): \{ 0, 1, 2, ..., m - 1 \}$

### 集合的表示法

- 列举法（显示法）
- 描述法（隐式法）

### 关于集合的基数

- 定义1：不含任何元素的集合称为空集，记为$\varnothing$。

- 定义2：集合A中不同元素的数目称为集合A的基数。记为$\#A$（或$\vert A \vert$）。

- 当$\#A$为有限数时，称A为有限集。否则称A为无限集。

## 集合的包含与相等

<img src="C:\Users\Joker\AppData\Roaming\Typora\typora-user-images\image-20230617210445841.png" alt="image-20230617210445841" style="zoom:50%;" />

==注意==

- $\subseteq$：表示子集
- $\subset$：表示[真子集]()

## 集合的幂集

定义：设A是一个集合，[以A的所有子集为元素]()构成的集合，称为A的幂集，记为$2^A$。

==注== 

- 空集是集合A的子集，因而$\varnothing \in 2^A$
- 一般而言，一个集合的幂集总是包含该集合本身：$A \in 2^A$
- 空集的幂集不再是空集：$\varPhi \in 2^\varPhi = \{\varPhi\}$
- 幂集的二进制表示方法：见PPT，S1P13

- 定理（集合的基数）：若A是有限集，且$\#A = n$，则有$\#2^A = 2^{\#A} = 2^n$

- 幂集的补集：$(2^A)' = 2^U - 2^A$

## 集合的运算

<img src="C:\Users\Joker\AppData\Roaming\Typora\typora-user-images\image-20230618093130043.png" alt="image-20230618093130043" style="zoom:50%;" />

## 集合的成员表

## 集合运算的定律

### 集合运算的十条定律

![image-20230411154427243](C:\Users\Joker\AppData\Roaming\Typora\typora-user-images\image-20230411154427243.png)

![image-20230411154439564](C:\Users\Joker\AppData\Roaming\Typora\typora-user-images\image-20230411154439564.png)

### 集合恒等式的几种证明方法

#### 根据定义进行证明

证明集合$S = H$，即证明：
$$
S \subseteq H \ 且 \ H \subseteq S
$$

#### 利用已有的集合恒等式证明新的恒等式

利用已有的集合运算定律证明新的恒等式。

#### 利用集合成员表证明集合恒等式

## 集合的分划

### 分划

- 交集 = 空集
- 并集 = 全集

<img src="C:\Users\Joker\AppData\Roaming\Typora\typora-user-images\image-20230618091611867.png" alt="image-20230618091611867" style="zoom: 33%;" />

### 细分

<img src="C:\Users\Joker\AppData\Roaming\Typora\typora-user-images\image-20230618091737531.png" alt="image-20230618091737531" style="zoom: 67%;" />

## 集合的标准形式

利用成员表求集合的最大集与最小集标准形式时：

- 最大集的标准形式应关注“0”所在位置，最大集标准形式为并集的[交集]()，有0则0
- 最小集的标准形式应关注“1”所在位置，最小集标准形式为交集的[并集]()，有1则1

### 最小集的标准形式

最小集表示为
$$
M_{\delta_1 \delta_2...\delta_r} = \overline{A}_1 \cap \overline{A}_2 \cap ... \cap \overline{A}_r \\
\delta_i = 
\begin{cases}
0,\ 当\overline{A}_i = A_i' \\
\\
1,\ 当\overline{A}_i = A_i \\
\end{cases}
$$
==注== 

- 例如：$A_1 \cap A_2 \cap A_3' \cap A_4 = M_{1101}$
- 最小集和最大集的$\delta_i$表示方式正好相反。

<img src="C:\Users\Joker\AppData\Roaming\Typora\typora-user-images\image-20230618091839512.png" alt="image-20230618091839512" style="zoom: 33%;" />

#### 定理1

<img src="C:\Users\Joker\AppData\Roaming\Typora\typora-user-images\image-20230618091947990.png" alt="image-20230618091947990" style="zoom: 33%;" />

#### 定理2

由$A_1, A_2, ..., A_r$所产生的每个非空集S恒可表示为若干个不同的最小集的并集。

### 最大集的标准形式

$$
\overline{M}_{\delta_1 \delta_2...\delta_r} = \overline{A}_1 \cup \overline{A}_2 \cup ... \cup \overline{A}_r \\
\delta_i = 
\begin{cases}
0,\ 当\overline{A}_i = A_i \\
\\
1,\ 当\overline{A}_i = A_i' \\
\end{cases}
$$

例如，$A_1 \cup A_2 \cup A_3' \cup A_4 = \overline{M}_{0010}$

<img src="C:\Users\Joker\AppData\Roaming\Typora\typora-user-images\image-20230618092218282.png" alt="image-20230618092218282" style="zoom: 50%;" />

#### 定理3

由$A_1, A_2, ..., A_r$所产生的任一集合S或为全集或为由$A_1, A_2, ..., A_r$所产生的若干不同的最大集的交。

### 关于集合的标准形式的进一步说明

#### 定理4

S是$A_1, A_2, ..., A_r$产生的集合，不记次序，则其最大（小）集的标准形式是唯一的。

#### 定理5

由$A_1, A_2, ..., A_r$产生的集合相等的充要条件是它们的最大（小）集的标准形式是一样的。

# 第二章 关系

## 笛卡尔积

### 有序n元组 & 序偶

<img src="C:\Users\Joker\AppData\Roaming\Typora\typora-user-images\image-20230618101657464.png" alt="image-20230618101657464" style="zoom:50%;" />

### 笛卡尔积

设$A_1, A_2, ..., A_n$为任意集合，称以下集合为笛卡尔积，并记为：
$$
A_1 \times A_2 \times ... \times A_n = \{ (a_1, a_2, ..., a_n) \vert a_i \in A_i, i = 1, 2, ..., n \}
$$
==注== 

- 一般情况下，$A \times B \ne B \times A$
- $\phi \times B = A \times \phi = \phi$
- 记号：$A \times A = A^2$

### 笛卡尔积的基数

$$
\#(A \times B) = \#A \times \#B
$$

### 与笛卡尔积有关的一些恒等式

类似于分配律：
$$
A \times (B \cup C) = (A \times B) \cup (A \times C) \\
(B \cup C) \times A = (B \times A) \cup (C \times A) \\
A \times (B \cap C) = (A \times B) \cap (A \times C) \\
(B \cap C) \times A = (B \times A) \cap (C \times A) \\
$$

## 关系的定义

<img src="C:\Users\Joker\AppData\Roaming\Typora\typora-user-images\image-20230618102226793.png" alt="image-20230618102226793" style="zoom: 33%;" />

### 元素与“关系”

- 若$(a, b) \in \rho$，则称a与b有关系$\rho$，记作$a\rho b$

- 若$(a, b) \notin \rho$，则称a与b无关系$\rho$，记作$a\rho' b$

### 几种特殊的关系

#### 空关系

对任意集合$A, B, \phi \subseteq A \times B, \phi \subseteq A \times A$，所以$\varPhi$是由A到B的关系，$\varPhi$也是A上的关系，称为空关系。

#### 普遍关系

$$
A \times A = U_A = \{ (a_i, a_j) \vert a_j, a_j \in A \}
$$

#### 恒等关系

$$
I_A = \{ (a, a) \vert a \in A \}
$$

### 关系的定义域和值域

<img src="C:\Users\Joker\AppData\Roaming\Typora\typora-user-images\image-20230618103805497.png" alt="image-20230618103805497" style="zoom:50%;" />

### 逆关系

<img src="C:\Users\Joker\AppData\Roaming\Typora\typora-user-images\image-20230618103910977.png" alt="image-20230618103910977" style="zoom:50%;" />

## 关系的表示

### 集合表示法

用集合的列举法或描述法来表示关系。

### 矩阵表示法

<img src="C:\Users\Joker\AppData\Roaming\Typora\typora-user-images\image-20230618104034465.png" alt="image-20230618104034465" style="zoom:50%;" />

### 关系图表示法

关系图由结点和边组成。

## 关系的运算

### 关系的并、交、补运算

### 关系的复合运算

<img src="C:\Users\Joker\AppData\Roaming\Typora\typora-user-images\image-20230618104158421.png" alt="image-20230618104158421" style="zoom:50%;" />

### 关系复合运算的性质

#### 定理1

设$\rho$是由A到B的关系，则：
$$
I_A \cdot \rho = \rho \cdot I_B = \rho
$$

#### 定理2 结合律

$$
(\rho_1 \cdot \rho_2) \cdot \rho_3 = \rho_1 \cdot (\rho_2 \cdot \rho_3)
$$

==注== 不加括号的表达式$\rho_1 \cdot \rho_2 \dots \cdot \rho_n$唯一地表示同一个关系。当$\rho_1 = \rho_2 = \dots = \rho_n = \rho$时，则有如下记号：
$$
\rho_1 \cdot \rho_2 \dots \cdot \rho_n = \rho^n
$$

### 求复合关系的几种方法

#### 根据复合关系的定义求复合关系

#### 运用关系矩阵的运算求复合关系

<img src="C:\Users\Joker\AppData\Roaming\Typora\typora-user-images\image-20230618104706233.png" alt="image-20230618104706233" style="zoom:50%;" />

==注== 求关系矩阵的乘积时，加法运算和乘法运算应改为布尔加和布尔乘法。

#### 利用关系图求复合关系

见PPT，S2P42

## 关系的性质

### ==重点== 集合A上关系的性质

![image-20230618105009218](C:\Users\Joker\AppData\Roaming\Typora\typora-user-images\image-20230618105009218.png)

==注意== 

- 自反 & 反自反：[针对所有元素]()
- 对称 & 反对称 & 可传递：针对部分元素
- 对称、反对称两者不矛盾，可同时存在。

### 利用关系矩阵和关系图判断关系的性质

#### 关系矩阵

![image-20230618105113175](C:\Users\Joker\AppData\Roaming\Typora\typora-user-images\image-20230618105113175.png)

#### 关系图

<img src="C:\Users\Joker\AppData\Roaming\Typora\typora-user-images\image-20230618105157116.png" alt="image-20230618105157116" style="zoom:50%;" />

## 集合A上关系的闭包

### 闭包的定义

#### 自反闭包 $r(\rho) = \rho \cup I_A$

设$\rho$是集合A上的关系，定义A上的关系$r(\rho) = \rho \cup I_A$称为$\rho$的自反闭包。

#### 对称闭包 $s(\rho) = \rho \cup \widetilde{\rho}$

设$\rho$是集合A上的关系，定义A上的关系$s(\rho) = \rho \cup \widetilde{\rho}$称为$\rho$的对称闭包。

#### 传递闭包 $t(\rho)$

设$\rho$是集合A上的关系，由下式定义的A上的关系：
$$
t(\rho) = \bigcup_{i = 1}^\infty \rho^i = \rho \cup \rho^2 \cup \rho^3 \cup ...
$$
称为$\rho$的传递闭包。

==注== 当A是有限集时，A上只有有限个不同的关系，因此，存在某个正整数m，使得：
$$
t(\rho) = \bigcup_{i = 1}^m \rho^i
$$
事实上，可以证明，若$\#A = n$，则有：
$$
t(\rho) = \bigcup_{i = 1}^n \rho^i
$$

### 闭包的性质

#### 自反闭包

设$\rho$是集合A上的关系，则$\rho$的自反闭包$r(\rho)$具有以下性质：

1. $\rho \subseteq r(\rho)$
2. $r(\rho)$是自反的
3. 对于A上任何关系$\rho_r$，若$\rho_r$自反且$\rho \subseteq \rho_r$，则$r(\rho) \subseteq \rho_r$

#### 对称闭包

设$\rho$是集合A上的关系，则$\rho$的对称闭包$s(\rho)$具有以下性质：

1. $\rho \subseteq s(\rho)$
2. $s(\rho)$是对称的
3. 对于A上任何关系$\rho_s$，若$\rho_s$对称且$\rho \subseteq \rho_s$，则$s(\rho) \subseteq \rho_s$

#### 传递闭包

设$\rho$是集合A上的关系，则$\rho$的传递闭包$t(\rho)$具有以下性质：

1. $\rho \subseteq t(\rho)$
2. $t(\rho)$是可传递的
3. 对于A上任何关系$\rho_t$，若$\rho_t$[可传递]()且$\rho \subseteq \rho_t$，则$t(\rho) \subset \rho_t$

## 等价关系

### 等价关系的定义

- 自反：$\forall a \in A,\ a \rho a$
- 对称：$\forall a, b \in A,\ 若a \rho b,\ 则b \rho a$
- 可传递：$\forall a, b, c \in A,\ 若a \rho b,\ b \rho c,\ 则有a \rho c$

集合A上的关系$\rho$，如果它是[自反的]()，[对称的]()，且[可传递的]()，则称$\rho$是A上的[等价关系]()。

### 等价类

<img src="C:\Users\Joker\AppData\Roaming\Typora\typora-user-images\image-20230618110054072.png" alt="image-20230618110054072" style="zoom: 50%;" />

#### 等价类的性质

1. $\forall a \in A,\ [a]_\rho \ne \varphi$
2. $\forall a, b \in A,\ 若a\rho b,\ 则[a]_\rho = [b]_{\rho}$
3. $\forall a,b \in A,\ 若a\rho'b,\ 则[a]_\rho \cap [b]_\rho = \varphi$

同一等价类中的元素相互等价，不同等价类中的元素互不等价。

### 等价关系与分划

集合A上的等价关系与集合A上的分划具有一一对应关系。

![image-20230618110334118](C:\Users\Joker\AppData\Roaming\Typora\typora-user-images\image-20230618110334118.png)

![image-20230618110350229](C:\Users\Joker\AppData\Roaming\Typora\typora-user-images\image-20230618110350229.png)

![image-20230618110525137](C:\Users\Joker\AppData\Roaming\Typora\typora-user-images\image-20230618110525137.png)

## 偏序关系

### 偏序关系的定义

- 自反
- 反对称
- 可传递

![image-20230618110630379](C:\Users\Joker\AppData\Roaming\Typora\typora-user-images\image-20230618110630379.png)

### 偏序关系的次序图

### 全序和良序

全序：元素之间都存在关系

良序：所有子集存在“最小值”

![image-20230618110737676](C:\Users\Joker\AppData\Roaming\Typora\typora-user-images\image-20230618110737676.png)

# 第三章 函数

## 函数

### 函数的概念

- 不允许一对多，可以多对一
- 定义域中的所有元素要有定义
- 值域中的元素可以没有原像（没有定义域中的元素对应）

#### 函数

![image-20230618145113917](C:\Users\Joker\AppData\Roaming\Typora\typora-user-images\image-20230618145113917.png)

#### 函数的定义域和值域

![image-20230618145158597](C:\Users\Joker\AppData\Roaming\Typora\typora-user-images\image-20230618145158597.png)

#### 函数的相等

![image-20230618164846234](C:\Users\Joker\AppData\Roaming\Typora\typora-user-images\image-20230618164846234.png)

==注== 从集合A到集合B函数的数量

记$B^A = \{ f \vert f: A \rightarrow B \}$，则$\#(B^A) = (\#B)^{\#A}$

<img src="C:\Users\Joker\AppData\Roaming\Typora\typora-user-images\image-20230618164944053.png" alt="image-20230618164944053" style="zoom: 33%;" />

### 几种特殊的函数

![image-20230618165055943](C:\Users\Joker\AppData\Roaming\Typora\typora-user-images\image-20230618165055943.png)

## 函数的复合运算

### 复合函数

$$
(g \cdot f)(a) = g(f(a))
$$

![image-20230618165210035](C:\Users\Joker\AppData\Roaming\Typora\typora-user-images\image-20230618165210035.png)

==注意== 复合函数$g \cdot f$即复合关系$f \cdot g$，其中f为起始的关系，g为末尾的关系。

### 函数复合运算的性质

- 设$f: A \rightarrow B$，则有$f \cdot I_A = I_B \cdot f = f$
- 结合律：$(h \cdot g) \cdot f = h \cdot (g \cdot f)$

==注== 不加括号的表达式$f_1 \cdot f_2 \cdot \dots \cdot f_n$唯一地表示一个函数。特别的有：
$$
f \cdot f \cdot \dots \cdot f = f^n
$$

### 复合函数的性质

#### 定理3-3

<img src="C:\Users\Joker\AppData\Roaming\Typora\typora-user-images\image-20230618165612289.png" alt="image-20230618165612289" style="zoom:50%;" />

#### ==重要== 定理3-4

![image-20230618165700439](C:\Users\Joker\AppData\Roaming\Typora\typora-user-images\image-20230618165700439.png)

## 逆函数

### 逆函数的定义

<img src="C:\Users\Joker\AppData\Roaming\Typora\typora-user-images\image-20230618193429530.png" alt="image-20230618193429530" style="zoom: 67%;" />

### 逆函数的性质

- 逆函数是双射，双射函数才有逆函数

- $(f^{-1})^{-1} = f$


- 设$f: A \rightarrow B$，则有：

$$
f^{-1} \cdot f = I_A \\
f \cdot f^{-1} = I_B
$$

- 设$f: A \rightarrow B$，$g: B \rightarrow A$，f, g之间存在如下关系：

$$
g \cdot f = I_A,\ f \cdot g = I_B
$$

则f, g互为逆函数。

## 集合的基数

### 集合的同基

![image-20230618170244875](C:\Users\Joker\AppData\Roaming\Typora\typora-user-images\image-20230618170244875.png)

### 可数集

若A是可数集，则有$A \sim N$，即A，N之间存在双射。

==注== 

- 可数集一定是无限集。
- 所有正有理数的集合$Q_+$，所有负有理数的集合$Q_-$和所有有理数的集合Q都是可数集。整数集I是可数集。
- 可数集的基数记为$\chi_0$（阿列夫零），有$\#N = \chi_0$。
- ==推论== $N^2$是可数集，即$N \times N \sim N$

构造双射$h: N \times N \rightarrow N$，h的定义如下：
$$
h(i, j) = \frac{(i + j - 2)(i + j - 1)}{2} + i
$$

### 不可数集

实数集R是不可数集。

不可数集的基数记为$\chi_1$（阿列夫壹），即有$\#R = \chi_1$。

# 第四章 代数系统

## 运算

<img src="C:\Users\Joker\AppData\Roaming\Typora\typora-user-images\image-20230618194018445.png" alt="image-20230618194018445" style="zoom: 33%;" />

### 运算的封闭性

<img src="C:\Users\Joker\AppData\Roaming\Typora\typora-user-images\image-20230618194347712.png" alt="image-20230618194347712" style="zoom: 40%;" />

==注== 定义在集合A上的运算在A上一定是封闭的，在A的子集上则不一定封闭。

### 二元运算的常见性质

- 可交换
- 可结合
- 可分配

### 与二元运算相关的特殊元素

#### 单位元

<img src="C:\Users\Joker\AppData\Roaming\Typora\typora-user-images\image-20230618202810923.png" alt="image-20230618202810923" style="zoom: 45%;" />

##### 定理 单位元的唯一性

<img src="C:\Users\Joker\AppData\Roaming\Typora\typora-user-images\image-20230618203014528.png" alt="image-20230618203014528" style="zoom: 45%;" />

#### 零元

<img src="C:\Users\Joker\AppData\Roaming\Typora\typora-user-images\image-20230618203911701.png" alt="image-20230618203911701" style="zoom: 40%;" />

##### 定理 零元的唯一性

<img src="C:\Users\Joker\AppData\Roaming\Typora\typora-user-images\image-20230618204034846.png" alt="image-20230618204034846" style="zoom:33%;" />

#### 幂等元

<img src="C:\Users\Joker\AppData\Roaming\Typora\typora-user-images\image-20230618204149804.png" alt="image-20230618204149804" style="zoom: 40%;" />

==注== 零元和单位元都是幂等元，故[幂等元并不唯一]()。

#### 元素的逆元

<img src="C:\Users\Joker\AppData\Roaming\Typora\typora-user-images\image-20230618204310652.png" alt="image-20230618204310652" style="zoom: 50%;" />

==注== 逆元针对集合中的每个元素。

##### 定理 逆元的唯一性

![image-20230618204442694](C:\Users\Joker\AppData\Roaming\Typora\typora-user-images\image-20230618204442694.png)

##### 定理4

![image-20230618204648898](C:\Users\Joker\AppData\Roaming\Typora\typora-user-images\image-20230618204648898.png)

## 代数系统

![image-20230619091448170](C:\Users\Joker\AppData\Roaming\Typora\typora-user-images\image-20230619091448170.png)

代数系统的要素：

- 非空集合
- 封闭的运算

### 整环

<img src="C:\Users\Joker\AppData\Roaming\Typora\typora-user-images\image-20230619091555000.png" alt="image-20230619091555000" style="zoom:50%;" />

### 子代数

要素：

- 非空子集
- 运算封闭

![image-20230619091703692](C:\Users\Joker\AppData\Roaming\Typora\typora-user-images\image-20230619091703692.png)

## 代数系统的同态和同构

### 同态

#### 同态的概念

<img src="C:\Users\Joker\AppData\Roaming\Typora\typora-user-images\image-20230620161602695.png" alt="image-20230620161602695" style="zoom: 67%;" />

==注== 同态：先运算后取像 = 先取像后运算，两集合中“对应元素的运算结果仍然对应”。

![image-20230619092520218](C:\Users\Joker\AppData\Roaming\Typora\typora-user-images\image-20230619092520218.png)

#### 特殊函数定义的特殊同态

$$
同态h 
\begin{cases}
h是内射 \rightarrow 单一同态 \\
\\
h是满射 \rightarrow 满同态 \\
\\
h是双射 \rightarrow 同构 \\
\end{cases}
$$

### 满同态的性质

<img src="C:\Users\Joker\AppData\Roaming\Typora\typora-user-images\image-20230619095026532.png" alt="image-20230619095026532" style="zoom:50%;" />

==注== e是$V_1$的单位元，猜想：$h(e)$是$V_2$的单位元。

### 同构

<img src="C:\Users\Joker\AppData\Roaming\Typora\typora-user-images\image-20230619095132308.png" alt="image-20230619095132308" style="zoom:50%;" />

==注== 构成同构的两个条件：

1. 同态
2. 双射

# 第五章 群

## 半群和独异点

### 半群

- 非空集合
- 二元运算满足结合律
- 代数系统（半群是一个代数系统）

### 独异点

- 半群
- 运算有单位元

==注== 对独异点$<S; *>$，$\forall a \in S,\ a^0 = e,\ a^{n + 1} = a^n * a$。

### 子半群和子独异点

- 子代数（非空子集，[运算封闭]()）
- 包含单位元（针对子独异点）

==注== 证明子集合为子独异点（PPT S5P44）

- 证明是子代数，运算封闭
- 证明子集中存在单位元

#### 循环独异点

<img src="C:\Users\Joker\AppData\Roaming\Typora\typora-user-images\image-20230619111003269.png" alt="image-20230619111003269" style="zoom: 50%;" />

## 群的定义

### 群

![image-20230619142256198](C:\Users\Joker\AppData\Roaming\Typora\typora-user-images\image-20230619142256198.png)

群需要满足的条件：

1. 运算满足结合律（运算要封闭，即群是一个代数系统）
2. 存在单位元
3. 任何元素都存在逆元

==注== 若群的运算可交换，则称为阿贝尔群。

### 循环群

#### 群中元素的幂

<img src="C:\Users\Joker\AppData\Roaming\Typora\typora-user-images\image-20230619142917404.png" alt="image-20230619142917404" style="zoom:50%;" />

#### 循环群

![image-20230619143151385](C:\Users\Joker\AppData\Roaming\Typora\typora-user-images\image-20230619143151385.png)

==注== 生成元不唯一。

#### 群的阶和元素的周期

<img src="C:\Users\Joker\AppData\Roaming\Typora\typora-user-images\image-20230619143541241.png" alt="image-20230619143541241" style="zoom:40%;" />

##### 定理

![image-20230619143724964](C:\Users\Joker\AppData\Roaming\Typora\typora-user-images\image-20230619143724964.png)

## 群的性质

### 相约性

- 设$<G;*>$是一个群，则对任意的$a, b \in G$：

存在唯一的元素$x \in G$，使$a * x = b$；

存在唯一的元素$y \in G$，使$y * a = b$。

- 设$<G;*>$是一个群，则对任意的$a, b, c \in G$：

若$a * c = a * c$，则$b = c$；

若$b * a = c * a$，则$b = c$。

### 元素运算后求逆元等于元素分别求逆元后颠倒次序相运算

设$<G;*>$是一个群，则对任意的$a, b \in G$，有：
$$
(a * b)^{-1} = b^{-1} * a^{-1}
$$
对任意$a_1, a_2, ..., a_n \in G$，有：
$$
(a_1 * a_2 * ... * a_n)^{-1} = a_n^{-1} * a_{n - 1}^{-1} * ... * a_1^{-1}
$$

### 元素的周期

- 群$<G;*>$中的元素a若具有有限周期r，则当且仅当k是r的整数倍时，$a^k = e$。
- 群中任一元素与它的逆元具有相同的周期，$T(a) = T(a^{-1})$。
- 在有限群中，每个元素均具有有限周期，且周期不超过群的阶（即[元素的个数]()）。

## 子群及其陪集

### 子群的定义

<img src="C:\Users\Joker\AppData\Roaming\Typora\typora-user-images\image-20230619145041105.png" alt="image-20230619145041105" style="zoom:50%;" />

### 子群的判别

<img src="C:\Users\Joker\AppData\Roaming\Typora\typora-user-images\image-20230619145454998.png" alt="image-20230619145454998" style="zoom:50%;" />

- 设$<G;*>$是一个群，H是G的非空子集，若：

1. 对于任意的$a, b \in H$，有$a * b \in H$（运算封闭）
2. 对任意的$a \in H$，有$a^{-1} \in H$（存在单位元和逆元）

则$<H;*>$是$<G;*>$的子群。

<img src="C:\Users\Joker\AppData\Roaming\Typora\typora-user-images\image-20230619145834124.png" alt="image-20230619145834124" style="zoom:50%;" />

- 设$<G;*>$是一有限群，若$<H;*>$是$<G;*>$的子代数，则$<H;*>$是$<G;*>$的子群。
- 设$<G;*>$是一个群，若$<H;*>$是$<G;*>$的有限子代数，则$<H;*>$是$<G;*>$的子群。

### 子群的等价定义

<img src="C:\Users\Joker\AppData\Roaming\Typora\typora-user-images\image-20230619151358726.png" alt="image-20230619151358726" style="zoom:50%;" />

### 陪集

<img src="C:\Users\Joker\AppData\Roaming\Typora\typora-user-images\image-20230619151527723.png" alt="image-20230619151527723" style="zoom:50%;" />

<img src="C:\Users\Joker\AppData\Roaming\Typora\typora-user-images\image-20230619151842250.png" alt="image-20230619151842250" style="zoom:50%;" />

<img src="C:\Users\Joker\AppData\Roaming\Typora\typora-user-images\image-20230619152109766.png" alt="image-20230619152109766" style="zoom:50%;" />

<img src="C:\Users\Joker\AppData\Roaming\Typora\typora-user-images\image-20230619152241169.png" alt="image-20230619152241169" style="zoom:50%;" />

# 第八章 图论

## 图的基本概念

### 图的定义及其表示

#### 图的定义

![image-20230619155931759](C:\Users\Joker\AppData\Roaming\Typora\typora-user-images\image-20230619155931759.png)

#### 图的表示方法

- 图解表示法
- 矩阵表示法

### 完全图与补图

#### 完全图

![image-20230619160058931](C:\Users\Joker\AppData\Roaming\Typora\typora-user-images\image-20230619160058931.png)

==注== 

- 完全图记作$K_n$。
- 单独一个结点也是完全图。
- 完全图的边数

![image-20230619160255896](C:\Users\Joker\AppData\Roaming\Typora\typora-user-images\image-20230619160255896.png)

#### 补图

![image-20230619160146283](C:\Users\Joker\AppData\Roaming\Typora\typora-user-images\image-20230619160146283.png)

==注== n个结点的图G和其补图$\overline{G}$的边数之间存在如下关系：
$$
\#E(G) + \#E(\overline{G}) = \frac{n(n - 1)}{2}
$$

### 连通图

#### 结点的度

![image-20230619160405380](C:\Users\Joker\AppData\Roaming\Typora\typora-user-images\image-20230619160405380.png)

==注== 图G中所有结点的度之和是边数m的两倍，即有：
$$
\sum_{i = 1}^n deg(v_i) = 2m
$$
==推论== 在任何图中，度为奇数的结点个数为偶数。

#### 其他概念

![image-20230619160605184](C:\Users\Joker\AppData\Roaming\Typora\typora-user-images\image-20230619160605184.png)

==注== 开路和回路中的结点可以重复，真路和环中的结点不可以重复。

#### 连通图

在图G中，若任意两个结点都是连接的，则称G是[连通图]()。否则，称G为非连通图。

仅有一个结点的图定义为连通图。

### 子图与分图

#### 子图

![image-20230619160801424](C:\Users\Joker\AppData\Roaming\Typora\typora-user-images\image-20230619160801424.png)

==注== 生成子图与原图的结点集保持一致。

#### 分图

![image-20230619161035227](C:\Users\Joker\AppData\Roaming\Typora\typora-user-images\image-20230619161035227.png)

#### 割点与割边

![image-20230619161141957](C:\Users\Joker\AppData\Roaming\Typora\typora-user-images\image-20230619161141957.png)

![image-20230619161210873](C:\Users\Joker\AppData\Roaming\Typora\typora-user-images\image-20230619161210873.png)

### 短程与距离

![image-20230619161249475](C:\Users\Joker\AppData\Roaming\Typora\typora-user-images\image-20230619161249475.png)

![image-20230619161312901](C:\Users\Joker\AppData\Roaming\Typora\typora-user-images\image-20230619161312901.png)

#### 定理

![image-20230619161347861](C:\Users\Joker\AppData\Roaming\Typora\typora-user-images\image-20230619161347861.png)

### 图的同构

<img src="C:\Users\Joker\AppData\Roaming\Typora\typora-user-images\image-20230619161428739.png" alt="image-20230619161428739" style="zoom:50%;" />

## 图的矩阵表示

### 图的邻接矩阵

<img src="C:\Users\Joker\AppData\Roaming\Typora\typora-user-images\image-20230619161624319.png" alt="image-20230619161624319" style="zoom:50%;" />

#### 定理

设G是具有结点集$\{ v_1, v_2, ..., v_n \}$和邻接矩阵A的图，则矩阵$A^l\ (l = 1, 2, ...)$的第i行j列的元素$a_{ij}^{(l)}$表示图G中[连接结点$v_i$到$v_j$长度为$l$的路的数目]()。

邻接矩阵的作用：

1. 判断G中任意两个结点是否相连接
2. 计算两结点之间的距离

### 图的连接矩阵

<img src="C:\Users\Joker\AppData\Roaming\Typora\typora-user-images\image-20230619161947355.png" alt="image-20230619161947355" style="zoom:50%;" />

可以通过图G的邻接矩阵A得到连接矩阵C（见PPT，S8P25）。

## 欧拉图和哈密尔顿图

### 欧拉图

欧拉图：通过图G的[每条边一次且仅一次]()的回路称为欧拉回路。存在欧拉回路的图，称为欧拉图。

欧拉路：通过图G的每条边一次且仅一次的[开路]()称为欧拉路。

#### 定理

- 一连通图G为欧拉图的充要条件是G的[每一结点的度均为偶数]()。
- 连通图G具有连接结点$v_i$到$v_j$的欧拉路的充要条件是，$v_i$和$v_j$是G中[仅有的具有奇数度的结点]()。

### 哈密尔顿图

- 哈密尔顿图：通过图G的[每个结点]()一次且仅一次的环称为哈密尔顿环。具有哈密尔顿环的图称为哈密尔顿图。
- 哈密尔顿路：通过图G的每个结点一次且仅一次的[开路]()称为哈密尔顿路。

#### 定理

##### 判定哈密尔顿图的必要条件

![image-20230619162711370](C:\Users\Joker\AppData\Roaming\Typora\typora-user-images\image-20230619162711370.png)

该定理给出了判断哈密尔顿图的[必要条件]()，若一个图不满足该条件，则它不是哈密尔顿图。

##### 判定哈密尔顿图（路）的充分条件

- 设G是具有n个结点的图，若G中任意两个不相邻的结点度数之和大于或等于$n - 1$，则G中存在哈密尔顿路。
- 设G是具有n（$n \ge 3$）个结点的图，若G中任意两个不相邻的结点度数之和大于或等于n，则G是哈密尔顿图。

上述两定理分别给出了判断哈密尔顿路和哈密尔顿图的[充分条件]()，不是必要条件。

## 树

### 树的定义

<img src="C:\Users\Joker\AppData\Roaming\Typora\typora-user-images\image-20230619164048001.png" alt="image-20230619164048001" style="zoom:50%;" />

<img src="C:\Users\Joker\AppData\Roaming\Typora\typora-user-images\image-20230619164508837.png" alt="image-20230619164508837" style="zoom:50%;" />

### 树的性质

- 若T是一$(n, m)$（n表示结点数，m表示边数）树，则$m = n - 1$

- ![image-20230620234907694](C:\Users\Joker\AppData\Roaming\Typora\typora-user-images\image-20230620234907694.png)


- 具有两个或更多结点的树至少有两片树叶（度为1的结点）。

### 生成树与最小生成树

#### 生成树

![image-20230619164617579](C:\Users\Joker\AppData\Roaming\Typora\typora-user-images\image-20230619164617579.png)

#### 构造连通图的生成树的方法

- 破环法
- 避环法

#### 最小生成树

##### 带权图

<img src="C:\Users\Joker\AppData\Roaming\Typora\typora-user-images\image-20230619164839017.png" alt="image-20230619164839017" style="zoom:50%;" />

##### 最小生成树

![image-20230619164925710](C:\Users\Joker\AppData\Roaming\Typora\typora-user-images\image-20230619164925710.png)

==注== 最小生成树通常不唯一。

## 二部图

### 二部图的定义

![image-20230619165524224](C:\Users\Joker\AppData\Roaming\Typora\typora-user-images\image-20230619165524224.png)

==注== 

- 二部图记作$K_{r, t}$
- 二部图不一定是连通图。

#### 定理

![image-20230619170904163](C:\Users\Joker\AppData\Roaming\Typora\typora-user-images\image-20230619170904163.png)

### 匹配

![image-20230619165854316](C:\Users\Joker\AppData\Roaming\Typora\typora-user-images\image-20230619165854316.png)

![image-20230619170758989](C:\Users\Joker\AppData\Roaming\Typora\typora-user-images\image-20230619170758989.png)

## 平面图

<img src="C:\Users\Joker\AppData\Roaming\Typora\typora-user-images\image-20230619171217188.png" alt="image-20230619171217188" style="zoom:50%;" />

### 平面图的判别

- 观察法
- 欧拉公式判断法

连通图G为平面图的两个[必要条件]()（不具有充分性）：

1. $n - m + k = 2$
2. $m \le 3n - 6\ (m \ge 2)$

其中，n为结点数，m为边数，k为面数。

![image-20230619171631301](C:\Users\Joker\AppData\Roaming\Typora\typora-user-images\image-20230619171631301.png)

![image-20230619171720618](C:\Users\Joker\AppData\Roaming\Typora\typora-user-images\image-20230619171720618.png)

- 库拉托斯基定理判别法

## 有向图

![image-20230619174847502](C:\Users\Joker\AppData\Roaming\Typora\typora-user-images\image-20230619174847502.png)

### 与无向图类似的概念

#### 可达

![image-20230619175009162](C:\Users\Joker\AppData\Roaming\Typora\typora-user-images\image-20230619175009162.png)

#### 可达矩阵

与无向图中的连接矩阵相对应。

#### 结点的度

- 结点v的出度，记作$deg^+(v)$
- 结点v的入度，记作$deg^-(v)$

- 结点v的度：$deg(v) = deg^+(v) + deg^-(v)$

#### 连通性

- 连通或弱连通
- 单向连通
- 强连通

<img src="C:\Users\Joker\AppData\Roaming\Typora\typora-user-images\image-20230619175304430.png" alt="image-20230619175304430" style="zoom:50%;" />

### 与无向图类似的性质

- 设G是具有n个结点的有向图，若从结点$v_i$到$v_j$可达，则其短程是一条长度不大于$n - 1$的真路。
- ==记忆== 设G是具有n个结点和邻接矩阵A的有向图，则$A^l\ (l = 1, 2, ...)$的第i行第j列的元素表示从结点$v_i$到$v_j$长为$l$的路的条数。
- 一个连通（弱连通）有向图[具有欧拉回路的充要条件]()是G的[每一个结点的入度和出度相等]()。[具有欧拉路的充要条件]()是除两个结点外，每个结点的入度等于出度。对于这两个结点，一个结点的出度比入度多一，另一个结点的出度比入度少一。

## 有向树

<img src="C:\Users\Joker\AppData\Roaming\Typora\typora-user-images\image-20230619200557486.png" alt="image-20230619200557486" style="zoom:50%;" />

![image-20230619200653500](C:\Users\Joker\AppData\Roaming\Typora\typora-user-images\image-20230619200653500.png)

### 有向树中的一些概念

<img src="C:\Users\Joker\AppData\Roaming\Typora\typora-user-images\image-20230619200933127.png" alt="image-20230619200933127" style="zoom:50%;" />

### 二元树

![image-20230619201243416](C:\Users\Joker\AppData\Roaming\Typora\typora-user-images\image-20230619201243416.png)

<img src="C:\Users\Joker\AppData\Roaming\Typora\typora-user-images\image-20230619201341234.png" alt="image-20230619201341234" style="zoom: 50%;" />

### 周游二元树

- 先根周游：$根 \rightarrow 左子树 \rightarrow 右子树$
- 中根周游：$左子树 \rightarrow 根 \rightarrow 右子树$
- 后根周游：$左子树 \rightarrow 右子树 \rightarrow 根$

### 有向树中的一些数量关系

- $m = n - 1$，即边数 = 结点数 - 1（和无向树一致）
- 设T是一棵完全m元树，树叶结点数为$n_0$，分支结点（有分支的结点）数为$t$，则有：

$$
(m - 1)t = n_0 - 1
$$

<img src="C:\Users\Joker\AppData\Roaming\Typora\typora-user-images\image-20230619202418379.png" alt="image-20230619202418379" style="zoom: 33%;" />

- 设T是一棵二元树，$n_0$表示树叶结点数（出度为1的结点数），$n_2$表示出度为2的结点数，则有：

$$
n_0 = n_2 + 1
$$

- 完全二元树有奇数个结点。

==注== 完全二元树的边数为偶数。

# 第九章 命题逻辑

## 命题

## 命题公式

### 命题的类型

- 重言式/永真式：若公式$\alpha$的所有完全指派均是成真指派，则公式$\alpha$称为重言式或永真式。
- 矛盾式/永假式：若公式$\alpha$的所有完全指派均是成假指派，则公式$\alpha$称为矛盾式或永假式。
- 可满足式：若公式$\alpha$中有成真指派，则公式$\alpha$称为可满足式。

==注== 

- $\alpha$是可满足式的等价定义是：$\alpha$至少存在一个成真指派。
- 重言式一定是可满足式，但反之不真。若公式$\alpha$是可满足式，且它至少存在一个可满足式，则称$\alpha$为非重言式的可满足式。

## 等值演算

==经验== 把合取$\and$看做加法$+$，析取$\or$看做乘法$\times$。

### 等值式

设$\alpha,\ \beta$是两个命题公式，若$\alpha,\ \beta$构成的等价式$\alpha \harr \beta$为重言式，则称公式$\alpha,\ \beta$是等值的，记作$\alpha \Harr \beta$。

==注== 判断两公式$\alpha,\ \beta$是否等值，可以用真值表法判断$\alpha \harr \beta$是否为重言式。

### 16组重要的等值式

#### 1）双重否定律

$$
\alpha \Harr \neg(\neg \alpha)
$$

否定的否定 = 本身

#### 2）等幂律

$$
\alpha \Harr \alpha \or \alpha, \quad \alpha \Harr \alpha \and \alpha
$$

#### 3）交换律

$$
\alpha \or \beta \Harr \beta \or \alpha, \quad \alpha \and \beta \Harr \beta \and \alpha
$$

#### 4）结合律

$$
(\alpha \or \beta) \or \gamma \Harr \alpha \or (\beta \or \gamma) \\
(\alpha \and \beta) \and \gamma \Harr \alpha \and (\beta \and \gamma) 
$$

#### 5）分配律

$$
\alpha \or (\beta \and \gamma) \Harr (\alpha \or \gamma) \and (\beta \or \gamma)\\
\alpha \and (\beta \or \gamma) \Harr (\alpha \and \gamma) \or (\beta \and \gamma)
$$

#### 6）德摩根律

$$
\neg(\alpha \or \beta) \Harr \neg \alpha \and \neg \beta \\
\neg(\alpha \and \beta) \Harr \neg \alpha \or \neg \beta
$$

#### 7）吸收律

$$
\alpha \or (\alpha \and \beta) \Harr \alpha \\
\alpha \and (\alpha \or \beta) \Harr \alpha
$$

#### 8）零一律

$$
\alpha \or 1 \Harr 1, \quad \alpha \and 0 \Harr 0
$$

#### 9）同一律

$$
\alpha \or 0 \Harr \alpha,\quad \alpha \and 1 \Harr \alpha
$$

#### 10）排中律

$$
\alpha \or \neg \alpha \Harr 1
$$

#### 11）矛盾律

$$
\alpha \and \neg \alpha \Harr 0
$$

#### 12）蕴含等值式 ==重点==

$$
\alpha \rightarrow \beta \Harr \neg \alpha \or \beta
$$

#### 13）假言易位

$$
\alpha \rightarrow \beta \Harr \neg \beta \rightarrow \neg \alpha
$$

#### 14）等价等值式

$$
\alpha \harr \beta \Harr (\alpha \rightarrow \beta) \and (\beta \rightarrow \alpha) \\
\alpha \harr \beta \Harr (\alpha \and \beta) \or (\neg \alpha \and \neg \beta)
$$

#### 15）等价否定等值式

$$
\alpha \harr \beta \Harr \neg \alpha \harr \neg \beta
$$

#### 16）归谬论

$$
(\alpha \rightarrow \beta) \and (\alpha \rightarrow \neg \beta) \Harr \neg \alpha
$$











































