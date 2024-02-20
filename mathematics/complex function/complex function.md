# 复数与复变函数

## 复数及其运算

### 复数的代数运算

#### 复数运算律

##### 交换律

$$
z_1 + z_2 = z_2 + z_1, \quad z_1z_2 = z_2z_1
$$

##### 结合律

$$
z_1 + (z_2 + z_3) = (z_1 + z_2) + z_3, \quad (z_1z_2)z_3 = z_1(z_2z_3)
$$

##### 分配律

$$
z_1(z_2 + z_3) = z_1z_2 + z_1z_3
$$

#### 共轭复数的性质

- $\overline{z_1 \pm z_2} = \overline{z_1} \pm \overline{z_2}$
- $\overline{z_1 z_2} = \overline{z_1} \ \overline{z_2}$
- $\overline{(\frac{z_1}{z_2})} = \frac{\overline{z_1}}{\overline{z_2}}$

- $\overline{\overline{z}} = z$
- $z + \overline{z} = 2Rez$
- $z - \overline{z} = 2iImz$
- $z\overline{z} = (Rez)^2 + (Imz)^2 = \vert z \vert ^ 2$

==常用变换==
$$
x = \frac{z + \overline{z}}{2} \\
y = \frac{z - \overline{z}}{2i}
$$

$$
  \overline{z_1}z_2 = \overline{z_1\overline{z_2}}
$$

### 复数的模

对于复数的模，有以下各式成立：

- $$
  \vert z \vert = \vert \overline{z} \vert, \quad z\overline{z} = \vert z \vert^2
  $$

- $$
  \vert x \vert \le \vert z \vert, \quad \vert y \vert \le \vert z \vert, \quad \vert z \vert \le \vert x \vert + \vert y \vert
  $$

- $$
  \vert z_1 + z_2 \vert \le \vert z_1 \vert + \vert z_2 \vert
  $$

- $$
  \vert z_1 - z_2 \vert \ge \vert \ \vert z_1 \vert - \vert z_2 \vert \ \vert
  $$

### 辐角

#### 主值$\arg z \ (z \ne 0)$的确定

$$
\arg \ z = 
\begin{cases}
\arctan \frac{y}{x}, \quad x > 0\\
\\
\frac{\pi}{2}, \quad x = 0, \ y > 0\\
\\
-\frac{\pi}{2}, \quad x = 0, \ y < 0\\
\\
\arctan \frac{y}{x} + \pi, \quad x < 0, \ y \ge 0\\
\\
\arctan \frac{y}{x} - \pi, \quad x < 0, \  y < 0
\end{cases}
$$

==注意== 

1. $\arg z \in (-\pi, \pi]$
2. 当$z = 0$时由于零向量方向任意，其辐角主值为任意值
3. 辐角表示为：$Arg \ z$， 辐角主值表示为：$\arg \ z$
4. “[二加三减]()”：当$z$在第二象限时，辐角主值$\arg z = \arctan\frac{y}{x} + \pi$；当$z$在第三象限时，$\arg z = \arctan\frac{y}{x} - \pi$

#### 关于辐角的结论

- 若负数$z_1,\ z_2$不全为0，则有：

$$
\vert z_1 z_2 \vert = \vert z_1 \vert · \vert z_2 \vert \\
Arg\ (z_1 z_2) = Arg\ z_1 + Arg\ z_2 \\
\vert \frac{z_1}{z_2} \vert = \frac{\vert z_1 \vert}{\vert z_2 \vert} \\
Arg\ \frac{z_1}{z_2} = Arg\ z_1 - Arg\ z_2 \quad （注意该式表示数集相等）
$$

- 两个复数乘积的模等于它们模的乘积，两个复数乘积的辐角等于它们辐角的和；两个复数商的模等于它们模的商，两个复数商的辐角等于它们辐角之差
- 两个复数相乘就是把模数相乘，辐角相加

- 函数$f(z) = \arg z$在原点和负实轴上不连续，在其余位置都连续

### 复数的乘幂与方根

#### 乘幂

$$
z^n = [r(\cos\theta + i\sin\theta)]^n = r^n(\cos n\theta + i\sin n\theta)
$$

##### [利莫佛公式]()

$$
(\cos\theta + i\sin\theta)^n = \cos n\theta + i\sin n\theta
$$

#### 方根

设$z = r(\cos\theta + i\sin\theta), w = \rho(\cos\phi + i\sin\phi)$，由$\omega^n = z$：
$$
\omega = \sqrt[n]{z} = \sqrt[n]{r}(\cos\frac{\theta + 2k\pi}{n} + i\sin\frac{\theta + 2k\pi}{n}), \quad (k = 0, \pm1, \pm2, ...)
$$
当$k = 0, 1, 2, ..., n-1$时得到n个不同的根，分别为：
$$
\begin{aligned}
& \omega_0 = \sqrt[n]{r}(\cos\frac{\theta}{n} + i\sin\frac{\theta}{n}) \\
& \omega_1 = \sqrt[n]{r}(\cos\frac{\theta + 2\pi}{n} + i\sin\frac{\theta + 2\pi}{n}) \\
& \dots \ \dots \\
& \omega_{n-1} = \sqrt[n]{r}[\cos\frac{\theta + 2(n - 1)\pi}{n} + i\sin\frac{\theta + 2(n - 1)\pi}{n}] \\
\end{aligned}
$$
==注== 复数n次方根的几何意义是：以原点为中心，以$\sqrt[n]{\vert z \vert}$为半径的圆内接正n边形的n个顶点

### 例题

#### 解方程

![](C:\Users\Joker\Documents\TyporaFiles\Curriculum\复变函数\image\解方程_1.jpg)

![](C:\Users\Joker\Documents\TyporaFiles\Curriculum\复变函数\image\解方程_2.jpg)

#### 求正三角形的另一个顶点

![](C:\Users\Joker\Documents\TyporaFiles\Curriculum\复变函数\image\求正三角形的顶点.jpg)

## 复变函数

### 复平面的点集

#### 区域

连通的开集称为区域

#### 简单曲线（若尔当曲线）

除起点终点外没有重点的连续曲线称为简单曲线

### 复变函数的极限与连续

#### 极限

设$f(z) = u(x, y) + iv(x, y), A = u_0 + iv_0,z_0 = x_0 + iy_0,z = x + iy$，则
$$
\lim_{z \rightarrow z_0}f(z) = A
$$
的充要条件是
$$
\lim_{x \rightarrow x_0,y \rightarrow y_0}u(x, y) = u_0, \quad \lim_{x \rightarrow x_0,y \rightarrow y_0}v(x, y) = v_0
$$
==说明== 该定理表明一个复变函数的极限问题可以转化成两个二元实变函数的极限问题

##### 极限有关结论

- 若$z \rightarrow z_0$时$f(z)$极限存在，则极限必定唯一
- 若$z \rightarrow z_0$时$f(z)$极限存在，则$f(z)$必在$z_0$的某去心邻域内有界
- 若

$$
\lim_{z \rightarrow z_0}f(z) = A, \quad \lim_{z \rightarrow z_0}g(z) = B
$$

则
$$
\lim_{z \rightarrow z_0}(f(z) \pm g(z)) = A \pm B \\
\lim_{z \rightarrow z_0}f(z)g(z) = AB, \quad \lim_{z \rightarrow z_0}
\frac{f(z)}{g(z)} = \frac{A}{B} \quad (B \ne 0)
$$

- 若

$$
\lim_{z \rightarrow z_0}g(z) = A
$$

且在$z_0$的某去心邻域内
$$
g(z) \ne A, \quad \lim_{h \rightarrow A}f(h) = B
$$
则
$$
\lim_{z \rightarrow z_0}f[g(z)] = B
$$

#### 连续

复变函数$f(z) = u(x, y) + iv(x, y)$在$z_0 = x_0 + iy_0$处[连续的充要条件]()是：$u(x, y),v(x, y)$在$(x_0, y_0)$处连续

==定理== 

- 如果复变函数$f(z),g(z)$在点$z_0$处连续，则其和、差、积、商（分母$z_0$不为零）在$z_0$处连续
- 如果复变函数$h = g(z)$在点$z_0$处连续，$\omega = f(z)$在点$h_0 = g(z_0)$处连续，则复合函数$\omega = f[g(z)]$在$z_0$处连续

==重要结论==

函数$f(z) = \arg z$在原点和负实轴上不连续，在其余位置都连续（P15）

# 解析函数

## 复变函数的导数与微分

==重要结论==

- $f(z) = \vert z \vert^2$仅在$z = 0$处可导，在其他点都不可导
- 函数$f(z) = \overline{z}$在复平面上处处连续，但处处不可导

### 求导法则

常用求导公式：

- $c' = 0$，其中c为复常数
- $(z^n)' = nz^{n-1}$，n为正整数
- $(f(z) \pm g(z))' = f'(z) \pm g'(z)$
- $(f(z) \dot\ g(z))' = f'(z)g(z) + f(z)g'(z)$
- $[\frac{f(z)}{g(z)}]' = \frac{1}{g^2(z)}[f'(z)g(z) - f(z)g'(z)]$
- $\{f[g(z)] \}' = f'(w)g'(z)$，其中$w = g(z)$
- $f'(z) = \frac{1}{\phi'(w)}$，其中$w = f(z)$与$z = \phi(w)$是两个互为反函数的单值函数，且$\phi'(w) \ne 0$

## 解析函数

### 函数解析的充要条件

设函数$f(z) = u(x, y) + iv(x, y)$在区域D内有定义，$z = x + iy \in D$，$f(z)$在点z可导的充要条件是：$u(x, y), v(x, y)$在点z可微，并且满足以下[柯西-黎曼方程]()：
$$
\frac{\partial u}{\partial x} = \frac{\partial v}{\partial y}, \quad \frac{\partial u}{\partial y} = -\frac{\partial v}{\partial x}
$$
当$f(z)$在点z可导时有：
$$
\begin{aligned}
f'(z) &= \frac{\partial u}{\partial x} + i\frac{\partial v}{\partial x} \\
&= \frac{\partial v}{\partial y} - i\frac{\partial u}{\partial y}
\quad (= \frac{1}{i}\frac{\partial u}{\partial y} + \frac{\partial v}{\partial y})\\
&= \frac{\partial u}{\partial x} - i\frac{\partial u}{\partial y} \\
&= \frac{\partial v}{\partial y} + i\frac{\partial v}{\partial x}
\end{aligned}
$$

### 函数解析的判定

==注意==

- 函数在一点解析，则函数在该点可导，反之不一定成立
- 函数在某区域解析等价于函数在该区域可导

==重要结论==

- 所有多项式在复平面内处处解析
- 对任何一个有理分式$\frac{P(z)}{Q(z)}$，它在除去使得分母为零的点外的区域内是解析的，使分母为零的点是它的奇点

#### 函数在一点解析

设函数$f(z) = u(x, y) + iv(x, y)$在区域D内有定义，$z_0 \in D$，$f(z)$在点$z_0$解析的充要条件是：存在点$z_0$的一个邻域$U(z_0, \delta)$，使得$u(x, y), v(x, y)$在$U(z_0, \delta)$内可微，并且满足柯西-黎曼方程

#### 函数在区域D解析

设函数$f(z) = u(x, y) + iv(x, y)$在区域D内有定义，$f(z)$在区域D解析的充要条件是：$u(x, y), v(x, y)$在D内可微，并且处处满足柯西-黎曼方程

==注== $f(z)$在区域D解析的[充分条件]()是：$u(x, y), v(x, y)$在D内[偏导数连续]()，并且处处满足柯西-黎曼方程

### 解析函数的运算法则

- 在区域D内两个解析函数的和、差、积、商（除去分母为零的点外）在D内解析
- 设$h = g(z)$在z平面上的区域D内解析，$w = f(h)$在w平面上的区域G内解析，并且当$z \in D$时，$h = g(z) \in G$，则$w = f(g(z))$在D内解析

## 初等函数

### 复指数函数

$$
z = x + yi \\
e^z = e^{x + yi} = e^x(\cos y + i\sin y)
$$

==注== （复）指数函数为单值函数

#### 性质

- 解析性：$w = e^z$在整个复平面上解析，且$(e^z)' = e^z$
- 可加性

$$
e^{z_1}e^{z_2} = e^{z_1 + z_2} \\
\frac{e^{z_1}}{e^{z_2}} = e^{z_1 - z_2}
$$

- 周期性

$$
e^{z + 2k\pi i} = e^z \\
e^z是以2k\pi i为周期的周期函数
$$

- $$
  \vert e^z \vert = e^x \\
  Arg(e^z) = y + 2k\pi \quad (k = 0,\pm 1, \pm 2, ...)
  $$

- $$
  \lim_{z \rightarrow \infty}e^z 不存在，即e^{\infty}无意义
  $$

### 对数函数

$$
若：z = e^w \quad (z \ne 0) \\
则称w为z的对数函数，记作： w = Lnz \quad (z \ne 0) \\
$$

对数函数w可表示为：
$$
w = Lnz = \ln\vert z \vert + i(\arg z + 2k\pi) \quad k = 0,\pm1,\pm2,...
$$
==注== 对数函数为多值函数

#### 对数函数的主值函数

$$
\ln z = \ln\vert z \vert + i\arg z
$$

==注== 

- 对数函数与其主值函数的表示存在大小写的不同

- 在应用对数函数时，一般指代除去原点及负实轴平面内的某一单值分支（主值）

#### 性质

$Ln z$与其主值$\ln z$存在如下关系：

$$
Lnz = \ln z + 2k\pi i \quad (k = 0,\pm1,\pm2,...)
$$

$Ln z$的运算性质：

$$
Ln(z_1 \cdot z_2) = Ln z_1 + Ln z_2 \\
Ln \frac{z_1}{z_2} = Ln z_1 - Ln z_2 \quad (z_2 \ne 0)
$$

在除去负实轴以及原点的复平面内，主值分支与其他各分支处处连续，处处可导，且有

$$
（\ln z)' = \frac{1}{z}
$$

### 幂函数

$$
z^\mu = e^{\mu Lnz}, \quad (z \ne 0, z \ne e)
$$

==注意== 
- 当$z$为正实变数，$\mu$为实数时，与普通幂函数一致，即$f(x) = x^\mu$
- 由于$Lnz$的多值性，$z^\mu = e^{\mu Lnz} = e^{\mu \ln z}e^{2k\pi\mu i}$，所以$z^\mu$一般是多值的

#### ==易错==[幂函数的计算]()

![image-20221112153705988](C:\Users\Joker\AppData\Roaming\Typora\typora-user-images\image-20221112153705988.png)

### 三角函数与双曲函数

#### 三角函数

$$
\cos z = \frac{e^{iz} + e^{-iz}}{2} (偶函数) \\
\sin z = \frac{e^{iz} - e^{-iz}}{2i} (奇函数) \\
$$

复数三角函数也以$2\pi$为周期

==注意==

当$y \rightarrow \infty$时，$\vert \sin iy \vert$和$\vert \cos iy \vert$都趋于无穷大，因此，[$\vert \sin z \vert \le 1, \vert \cos z \vert \le 1$在复数范围内不再成立]()。

##### 三角函数求导

$$
(\sin z)' = \cos z \\
(\cos z)' = -\sin z
$$

##### 三角函数常用结论

$$
\sin z = 0 \quad \Rightarrow \quad z = k\pi, (k \in Z) 
$$

#### 双曲函数

$$
sh z = \frac{e^z - e^{-z}}{2} \\
ch z = \frac{e^z + e^{-z}}{2} \ne 0
$$

复数双曲函数以$2\pi i$为周期

##### 双曲函数求导

$$
(shz)' = chz \\
(chz)' = shz
$$

#### 三角函数与双曲函数的变换公式

$$
\begin{cases}
\cos yi = chy\\
\sin yi = ishy \\
\\
ch yi = \cos y \\
sh yi = i \sin y
\end{cases}
$$

由此可以得到一些常用公式：
$$
\sin(x + iy) = \sin x chy + i\cos x shy
$$

#### 反三角和反双曲函数

$$
\arcsin z = -i Ln(iz + \sqrt{1 - z^2}) \\
\arccos z = -i Ln(z + \sqrt{z^2 - 1}) \\
\arctan z = -\frac{i}{2} Ln \frac{1 + iz}{1 - iz} \\
arcshz = Ln(z + \sqrt{z^2 + 1}) \\
arcchz = Ln(z + \sqrt{z^2 - 1}) \\
arcthz = \frac{1}{2} Ln\frac{1 + z}{1 - z}
$$

# 复积分

## 复积分的性质

第二类曲线积分的性质对复积分同样成立.

- $$
  \int_Cf(z)dz = -\int_{C^-}f(z)dz
  $$

- 线性性质：$\forall k, l \in C$，函数$f(z), g(z)$沿C可积，则

$$
\int_C[kf(z) + lg(z)]dz = k\int_Cf(z)dz + l\int_Cg(z)dz
$$

- 积分路径的可加性：若C是由按段光滑曲线$C_1, C_2, ..., C_n$依次相互连接所组成的有向曲线，则

$$
\int_Cf(z)dz = \sum_{k = 1}^{n}\int_{C_k}f(z)dz
$$

- ==估值不等式==：

$$
\vert \int_Cf(z)dz \vert \le \int_C \vert f(z) \vert ds \le ML \\
（L为积分曲线C的长度）
$$

上式中间部分是实变函数$\vert f(z) \vert$沿曲线C的第一类曲线积分.

## 柯西积分定理（P48）

设$w = f(z)$在[单连通区域D上解析]()，C为D内任一条[闭曲线]()（不必为简单闭曲线），则：
$$
\oint_Cf(z)dz = 0
$$
==推论== 

- 设$f(z)$在单连通区域D上解析，C为D内任一条起于$z_0$而终于$z$的简单曲线，则$\int_Cf(z)dz$与积分路径无关，而只由点$z_0$和$z$确定. 通常将此积分记为：

$$
\int_{z_0}^zf(\zeta)d\zeta
$$

- 将解析性假定用较弱的连续性假定替代，有：如果$f(z)$在简单闭曲线C上连续，在其内部解析，则

$$
\oint_Cf(z)dz = 0
$$

## 复合闭路定理（P50）

设$f(z)$在复合闭路$\Gamma = C_0 + \sum_{i = 1}^nC^-_i$及其围成的多连通区域D上解析，则：

- $$
  \int_{C_0}f(z)dz = \sum_{k = 1}^n \int_{C_k}f(z)dz
  $$

- $$
  \oint_{\Gamma}f(z)dz = 0
  $$

### 闭路变形原理（P51）

给定区域D上的一个解析函数$f(z)$沿闭曲线C上的积分：
$$
A = \oint_Cf(z)dz
$$
当闭曲线C在区域D内连续变形且变形过程中不经过函数$f(z)$的原点时，该积分的值不变.

==重要结论== 利用闭路变形原理可以得到：
$$
\oint_C\frac{dz}{(z - z_0)^n} = 
\begin{cases}
2 \pi i, \quad n = 1 \\
0, \quad n \ne 1
\end{cases}
$$
其中，C为任意绕$z_0$的简单正向闭曲线，且C所围区域内只有一个奇点$z_0$.

## 牛顿-莱布尼兹公式（P52）

如果$f(z)$是单连通区域D内的解析函数，那么变上限积分所确定的函数
$$
\varphi(z) = \int_{z_0}^z f(\zeta)d\zeta
$$
也是D内的解析函数，且$\varphi'(z) = f(z), \forall z \in D$.

设$G(z)$为$f(z)$的一个原函数，则
$$
\int_{z_0}^z f(\zeta)d\zeta = G(z) - G(z_0) = G(\zeta)\vert_{\zeta = z_0}^{z}
$$
其中，$z_0,z$为D内任意给定两点.

## 柯西积分公式

设$f(z)$在闭合回路（或复合闭路）$\Gamma$所围成的区域D上解析，在$\Gamma$上连续，则对$\forall z \in D$有：
$$
f(z) = \frac{1}{2\pi i} \oint_{\Gamma}\frac{f(\xi)}{\xi - z}d\xi \\
或\quad \oint_{\Gamma}\frac{f(\xi)}{\xi - z_0}d\xi = 2\pi i f(z_0) \\
z_0是\Gamma所包围的区域内\frac{f(z)}{z - z_0}的一个奇点
$$
该公式表明解析函数在区域内的性质完全由它在边界上的性质决定，这是解析函数的一个重要特征.

### （推论）平均值公式

设函数$f(z)$在圆域$\vert z - z_0 \vert < R$上解析，在圆周$\vert z - z_0 \vert = R$连续，则
$$
f(z_0) = \frac{1}{2\pi}\int_0^{2\pi}f(z_0 + Re^{i\theta})d\theta
$$
即解析函数在圆心处的值等于它在圆周上的平均值.

## 高阶导数公式

解析函数的导数仍是解析函数，且它的n阶导数可表示为
$$
f^{(n)}(z) = \frac{n!}{2\pi i} \oint_C \frac{f(\xi)}{(\xi - z)^{n + 1}}d\xi \quad (n = 1,2,...)
$$
其中，C是在函数$f(z)$的解析区域D内绕$z$的任何一条正向简单闭曲线，且内部完全含于D.

高阶导数公式的常用形式：
$$
\oint_C\frac{f(z)}{(z - z_0)^{n + 1}}dz = \frac{2\pi i}{n!}f^{(n)}(z_0)
$$


## 解析函数与调和函数的关系

### 调和函数

如果函数$\varphi(x, y)$在区域D内具有二阶连续偏导数，并且满足[拉普拉斯方程]()：
$$
\frac{\partial^2 \varphi}{\partial^2 x} + \frac{\partial^2 \varphi}{\partial^2 y} \equiv 0
$$
则称函数$\varphi(x, y)$为区域D上的二元调和函数

### 共轭调和函数

设$u(x, y), v(x, y)$是区域D上的调和函数且$u + iv$为D上的解析函数，则称函数$v$是$u$的共轭调和函数.

==注== 共轭调和函数位置（顺序）不可调换

该定义也可表述为：若调和函数$u(x, y), v(x, y)$在区域D上满足$C.-R.$方程：
$$
\frac{\partial u}{\partial x} = \frac{\partial v}{\partial y},\quad \frac{\partial u}{\partial y} = -\frac{\partial v}{\partial x}
$$
则$v$是$u$的共轭调和函数.

#### 利用共轭调和函数判断解析函数

函数$f(z) = u(x, y) + iv(x, y)$为解析函数的[充要条件]()为：$v(x, y)$是$u(x, y)$的共轭调和函数

### 定理3.5.1（P60）

若函数$f(z) = u(x, y) + i v(x, y)$在区域D上解析，则$u(x, y), v(x, y)$为D上的调和函数，其逆命题不成立.

### 计算实例

求以函数$u(x,y) = y^3 - 3x^2y$为实部的解析函数：

因为

$$
\frac{\partial u}{\partial x} = \frac{\partial v}{\partial y} = -6xy \\
\frac{\partial u}{\partial y} = -\frac{\partial v}{\partial x} = -3y^2 + 3x^2
$$

得到

$$
v(x, y) = x^3 - 3xy^2 + c\\
w(x, y) = y^3 - 3x^2y + i(x^3 - 3xy^2 + c)
$$

令$y = 0$，并用$z$替换$x$，即得（[解析函数的特性]()）

$$
w = f(z) = i(z^3 + c)
$$

# 复变函数的级数

## 复数列的极限

### 复数列收敛与实数列收敛的关系

复数列$\{\alpha_n\} (n = 1, 2, ...)$收敛于$\alpha$的充要条件是
$$
\lim_{n \rightarrow \infty} a_n = a, \quad \lim_{n \rightarrow \infty} b_n = b
$$

该结论说明：可将复数列的敛散性转化为判别两个实数列的敛散性

## 复数项级数

判别复数项级数敛散性的基本方法是利用极限
$$
\lim_{n \rightarrow \infty}S_n = S,\quad S_n为部分和数列
$$

### 复数项级数与实数项级数收敛的关系

级数
$$
\sum_{n = 1}^\infty \alpha_n = \sum_{n = 1}^\infty(a_n + ib_n)
$$
收敛的充要条件是$\sum_{n=1}^\infty a_n, \sum_{n=1}^\infty b_n$都收敛

### 级数收敛的必要条件

复数项级数$\sum_{n=1}^\infty \alpha_n$收敛的必要条件是：
$$
\lim_{n \rightarrow \infty} \alpha_n = 0
$$
==重要结论== 
$$
\lim_{n \rightarrow \infty} \alpha_n \ne 0 \quad \Rightarrow \quad 
\sum_{n = 1}^\infty \alpha_n 发散
$$

### 绝对收敛与条件收敛

如果$\sum_{z = 1}^\infty \vert \alpha_n \vert$收敛，则$\sum_{z = 1}^\infty \alpha_n$绝对收敛，非绝对收敛的收敛级数称为条件收敛

#### 绝对收敛级数的性质

如果$\sum_{n=1}^\infty \vert \alpha_n \vert$收敛，则$\sum_{n=1}^\infty \alpha_n$也收敛，反之不一定成立

## 幂级数

### 幂级数的敛散性

#### 阿贝尔定理

如果级数$\sum_{n = 1}^\infty c_nz_n$在$z = z_0(\ne 0)$收敛，则对满足$\vert z \vert < \vert z_0 \vert$的$z$，级数必绝对收敛；如果在$z = z_0$级数发散，则对满足$\vert z \vert > \vert z_0 \vert$的$z$，级数必发散

### 收敛半径的计算

#### 比值法

$$
R = \lim_{n \rightarrow \infty}\vert \frac{c_n}{c_{n + 1}} \vert
$$

#### 根值法

$$
R = \lim_{n \rightarrow \infty} \frac{1}{\sqrt[n]{\vert c_n \vert}}
$$

### 幂级数的运算和性质

#### 幂级数的运算

- 设

$$
f(z) = \sum_{n = 0}^\infty a_nz^n, R = r_1 \\
g(z) = \sum_{n = 0}^\infty b_nz^n, R = r_2
$$

则有

$$
f(z) \pm g(z) = \sum_{n = 0}^\infty (a_n \pm b_n)z^n \\
f(z) \cdot g(z) = \sum_{n = 0}^\infty (a_nb_0 + a_{n - 1}b1 + ... + a_0b_n)z^n \\
其中，\vert z \vert < R, R = \min\{r_1, r_2\}
$$

- 若当$\vert z \vert < r$时， $f(z) = \sum_{n = 0}^\infty a_nz^n$，又设在$\vert z \vert < R$内$g(z)$解析且满足$\vert g(z) \vert < r$，则当$\vert z \vert < R$时有

$$
f[g(z)] = \sum_{n = 0}^\infty a_n[g(z)]^n
$$

说明：该运算常用于将函数展开成幂级数

#### 幂级数的性质

设幂级数$\sum_{n = 0}^\infty c_n(z - \alpha)^n$的收敛半径为R，则
- 它的和函数$f(z)$在$\vert z - \alpha \vert < R$解析
- （逐项求导）当$\vert z - \alpha \vert < R$时，有

$$
f'(z) = \sum_{n = 1}^\infty nc_n(z - \alpha)^{n-1}
$$

- （逐项积分）设C为$\vert z - \alpha \vert < R$内的一条逐段光滑曲线，则

$$
\int_C f(z)dz = \sum_{n = 0}^\infty c_n\int_C(z - \alpha)^ndz
$$

## 泰勒级数

### Taylor级数展开定理

$f(z)$在圆$K: \vert z - z_0 \vert < R$内解析，则$f(z)$可在K内展成幂级数：

$$
f(z) = \sum_{n = 0}^\infty c_n(z - z_0)^n \\
其中，c_n = \frac{1}{n!}f^{(n)}(z_0), n = 1, 2, ...
$$

说明：任何解析函数展成幂级数的结果就是泰勒级数，因而解析的泰勒级数唯一

### 泰勒级数与幂级数的关系

- 定理1

函数$f(z)$在点$z_0$解析的充要条件是函数$f(z)$可在$z_0$的邻域内展幂级数

- 定理2

幂级数的和函数在收敛圆周上至少有一个奇点

- 结论

如果$z_0$是$f(z)$的解析点，则$f(z)$可在$z_0$的邻域内展成$z - z_0$的幂级数，其收敛半径是函数$f(z)$的距离$z_0$最近的奇点与$z_0$的距离

### 将函数展开成泰勒级数

- 直接法

$$
c_n = \frac{1}{n!}f^{(n)}(z_0), n = 1, 2, ...
$$

- [间接法]()

常用泰勒展开式：

$$
\sin z = \sum_{n = 0}^\infty (-1)^n\frac{z^{2n + 1}}{(2n + 1)!} \quad R = \infty \\
\cos z = \sum_{n = 0}^\infty (-1)^n \frac{z^{2n}}{(2n)!} \quad R = \infty \\
e^z = \sum_{n = 0}^\infty \frac{z^n}{n!} \\
\frac{1}{1 + z} = \sum_{n = 0}^\infty (-1)^n z^n \quad \vert z \vert < 1 \\
\frac{1}{1 - z} = \sum_{n = 0}^\infty z^n \quad \vert z \vert < 1 \\
\ln(1 + z) = \sum_{n = 0}^\infty (-1)^n \frac{z^{n + 1}}{n + 1} \quad \vert z \vert < 1
$$

## 解析函数的唯一性定理

设$f(z),g(z)$在区域D内解析，$\{z_n\}(n = 1, 2, ...)$是D内的点列，当$m \ne n$时，$z_m \ne z_n$，且$z_n \rightarrow z_0, z_0 \in D$，若对一切n，都有$f(z_n) = g(z_n)$，则$\forall z \in D, f(z) = g(z)$

==说明== 解析函数的唯一性定理说明了解析函数的一个重要特性：
在区域D上的两个解析函数，只要在D内的某一部分（子区域或孤段）上的值相等，则它们在整个区域D上的值必相等

# 留数

==定义== 若$z_0$是函数$f(z)$的一个孤立奇点，则$f(z)$在以$z_0$为中心的圆环域内洛朗级数中负幂项$c_{-1}(z - z_0)^{-1}$的系数定义为留数$(c_{-1})$，且有：
$$
c_{-1} = \frac{1}{2\pi i}\oint_Cf(z)dz = Res[f(z), z_0]
$$
其中C为$z_0$的某个去心领域内包含$z_0$的任意一条简单闭曲线.

## 有限孤立奇点的分类

==重要结论== 有理函数的奇点只能是可去奇点或极点

- 可去奇点

==定理== $z_0$为$f(z)$的可去奇点的充要条件是
$$
\lim_{z \rightarrow z_0}f(z) = A
$$

- 极点

==定理== $z_0$为$f(z)$极点的充要条件是
$$
\lim_{z \rightarrow z_0}f(z) = \infty
$$

- 本性奇点

==定理== $z_0$是$f(z)$的本性奇点的充要条件是$\lim_{z \rightarrow z_0} f(z)$不存在

## 零点级数的判断

- 若函数$f(z)$可写为如下形式：

$$
f(z) = (z - z_0)^m\varphi(z), \quad (\varphi(z_0) \ne 0)
$$

则$z_0$是$f(z)$的m级零点

- $z_0$是$f(z)$的m级零点充要条件是$f(z)$在$z_0$处解析，且$f^{(k)}(z_0) = 0(k = 0, 1, 2, ..., m - 1)$，但$f^{(m)}(z_0) \ne 0$.（逐级求导并判断导数是否为零）

==注意== 解析函数的零点必定是孤立的

## 极点级数的判断

- $z_0$为$f(z)$的m级极点的充要条件是：$\exist g(z)$，满足

$$
f(z) = \frac{g(z)}{(z - z_0)^m}
$$

其中$g(z_0) \ne 0$，$g(z)$在$z_0$处解析

- $z_0$是$f(z)$的m级极点的充要条件是$z_0$是$\frac{1}{f(z)}$的m级零点
- 若$f(z)$为有理函数：

$$
f(z) = \frac{P(z)}{Q(z)}
$$

且$z_0$是$P(z)$的m级极点，是$Q(z)$的n级极点，$n > m$，则$z_0$是$f(z)$的$n - m$级极点（若$n \le m$则$z_0$为可去极点）

==注意== 若$R(z)$为有理函数，则存在多项式$P(z),Q(z)$，使得
$$
R(z) = \frac{P(z)}{Q(z)}
$$

## 留数定理

函数$f(z)$在区域D内除有限个孤立奇点$z_1, z_2, ..., z_n$处处解析，C是D内包围诸奇点的一条简单正向闭曲线，则
$$
\oint_Cf(z)dz = 2\pi i\sum_{k=1}^n Res[f(z), z_k]
$$
==注意== $f(z)$在C上及C内部处处解析

## 留数的计算

- 如果$z_0$为$f(z)$的可去奇点，则

$$
Res[f(z), z_0] = 0
$$

- 如果$z_0$为$f(z)$的本性奇点，则需将$f(z)$展开为洛朗级数求$c_{-1}$

- 如果$z_0$为$f(z)$的极点，则有如下计算规则：

==规则1== 如果$z_0$为$f(z)$的一级极点，则
$$
Res[f(z), z_0] = \lim_{z \rightarrow z_0}(z - z_0)f(z)
$$
==规则2== 设$f(z) = \frac{P(z)}{Q(z)}$, $P(z), Q(z)$都解析，如果$P(z_0) \ne 0, Q(z_0) = 0, Q'(z_0) \ne 0$，则$z_0$为$f(z)$的一级极点，且有
$$
Res[f(z), z_0] = \frac{P(z_0)}{Q'(z_0)}
$$
==规则3== 如果$z_0$为$f(z)$的m级极点，则
$$
Res[f(z), z_0] = \frac{1}{(m - 1)!} \lim_{z \rightarrow z_0} \frac{d^{m - 1}}{dz^{m - 1}}[(z - z_0)^mf(z)]
$$

==注== 在应用规则3时，有时为了计算方便可以把m取的比实际的级数高

## 无穷远点的留数

若$z = \infty$是$f(z)$的孤立奇点，则

$$
Res[f(z), \infty] = -Res[f(\frac{1}{z})\frac{1}{z^2}, 0]
$$

### 有限孤立奇点与无穷远点留数的关系

设函数$f(z)$在扩充复平面上除去$z_1, z_2, ..., z_n, \infty$外解析，则有

$$
\sum_{k = 1}^n Res[f(z), z_k] + Res[f(z), \infty] = 0
$$

即有：

$$
\sum_{k = 1}^n Res[f(z), z_k] = -Res[f(z), \infty] = Res[f(\frac{1}{z})\frac{1}{z^2}, 0]
$$

## 应用留数计算定积分

思想方法：把定积分转化为一个复变函数沿某条封闭路线的积分

两个重要工作：

- 积分区域的转化
- 被积函数的转化

### 三角有理式的积分

$$
\int_0^{2\pi}R(\cos\theta, \sin\theta)d\theta
$$

令$z = e^{i\theta}$，则有
$$
\cos\theta = \frac{z^2 + 1}{2z} \\
\sin\theta = \frac{z^2 - 1}{2iz} \\
d\theta = \frac{dz}{iz}
$$
代入积分式：
$$
\begin{aligned}
\int_0^{2\pi}R[\cos\theta, \sin\theta]d\theta &= \oint_{\vert z \vert = 1}R[\frac{z^2 + 1}{2z}, \frac{z^2 - 1}{2iz}]\frac{dz}{iz} \\
&= \oint_{\vert z \vert = 1} f(z)dz \\
&= 2\pi i\sum_{k = 1}^n Res[f(z), z_k]
\end{aligned}
$$

### 有理函数的无穷积分

$$
\int_{-\infty}^{+\infty}f(x)dx
$$

==定理== 设函数$f(z)$在上半平面$Imz > 0$上除去有限个孤立奇点$z_1, z_2, ..., z_n$外解析，在$Imz \ge 0$上除去这些点外连续。若取$f(x) = \frac{P(x)}{Q(x)}$为实系数有理函数，其中$P(x), Q(x)$为互质多项式，且
- 分母$Q(x)$的次数至少比分子的次数高两次
- $Q(x)$在x轴上无零点（在实轴上）

则有：
$$
\int_{-\infty}^{+\infty}f(x)dx = 2\pi i \sum_{k = 1}^n Res[f(z), z_k]
$$

### 有理函数与三角函数乘积的积分

==定理== 设函数$f(z)$在上半平面$Imz > 0$上除去有限个孤立奇点$z_1, z_2, ..., z_n$外解析，在$Imz \ge 0$上除去这些点外连续。若$f(z)$是x的有理函数且分母的次数至少比分子的次数高一次，且$f(z)$在实轴上无孤立奇点，则
$$
\int_{-\infty}^{+\infty}f(x)e^{aix}dx = 2\pi i \sum_{k = 1}^n Res[f(z), z_k]
$$





































