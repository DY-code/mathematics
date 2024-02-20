# 曲面曲线积分

## 特殊曲面积分的计算

- 计算第一型曲面积分：

$$
I = \iint_S\frac{1}{\sqrt{x^2 + y^2 + (z - \frac{a}{2})^2}}dS\\
其中，S: x^2 + y^2 + z^2 = a^2,a>0.
$$

解：

由坐标变换：
$$
\begin{cases}
x' = x\\
y' = y\\
z' = z - \frac{a}{2}
\end{cases}\Rightarrow
\begin{cases}
x = x'\\
y = y'\\
z = z' + \frac{a}{2}
\end{cases}
$$
原曲面积分变为：
$$
I = \iint_{S'}\frac{1}{\sqrt{x^2 + y^2 + z^2}}dS\\
S':x^2 + y^2 + (z + \frac{a}{2})^2 = a^2
$$
考虑如下曲线弧：
$$
y^2 + (z + \frac{a}{2})^2 = a^2,\quad y > 0
$$
其参数方程为：
$$
\begin{cases}
y = a\cos\theta\\
z = a\sin\theta - \frac{a}{2}
\end{cases}\quad\quad \theta: -\frac{\pi}{2} \rightarrow \frac{\pi}{2}
$$
其对应的弧微分为：
$$
ds = \sqrt{y_\theta'^2 + z_\theta'^2}d\theta = ad\theta
$$
将ds沿z轴旋转一周，得到的圆环面积微元为：
$$
dS = 2\pi x ds = 2\pi a^2\cos\theta d\theta
$$
且对于该面积微元有：
$$
r = \sqrt{x^2 + y^2 + z^2} = \sqrt{y^2 + z^2} = a\sqrt{\frac{5}{4} - \sin\theta}
$$
则：
$$
\begin{aligned}
I &= \iint_{S'} \frac{1}{\sqrt{x^2 + y^2 + z^2}}dS\\
&= \int_{-\frac{\pi}{2}}^{\frac{\pi}{2}}\frac{2\pi a^2\cos\theta}{a\sqrt{\frac{5}{4} - \sin\theta}} d\theta\\
&= -4\pi a\sqrt{\frac{5}{4} - \sin\theta}\quad\vert_{-\frac{\pi}{2}}^{\frac{\pi}{2}}\\
&= 4\pi a
\end{aligned}
$$

## 积分坐标变换

- 求由抛物线$y^2 = px,y^2 = qx(0 < p < q)$和双曲线$xy = a,xy = b(0 < a < b)$所围成的闭区域的面积.

解：考虑利用积分坐标变换，令
$$
u = \frac{y^2}{x}\\
v = xy
$$
由雅各布行列式有：
$$
J = \vert \frac{\partial(u,v)}{\partial(x,y)} \vert
= \vert\begin{vmatrix}
-\frac{y^2}{x^2} & \frac{2y}{x}\\
y & x
\end{vmatrix}\vert
= \frac{3y^2}{x} = 3u
$$
所以
$$
dudv = 3udxdy,\quad dxdy = \frac{1}{3u}dudv
$$
所求面积为：
$$
S = \iint_{D_{uv}}dudv = \int_p^qdu\int_a^b\frac{1}{3u}dv = \frac{b - a}{3}\ln\frac{q}{p}
$$

# 无穷级数

## 判断级数敛散性

- 判断级数

$$
\sum_{n=0}^{\infty}\frac{(n!)^2}{(2n)!}x^n
$$

在$x = 4$处的敛散性.

解：注意到有
$$
\begin{aligned}
\frac{(n!)^2}{(2n)!}4^n &= \frac{n!·1·2·3·...·n}{1·2·3·4·...·(2n - 1)·2n}2^n·2^n\\
&= \frac{n!·2·4·6·...·2n}{n!·1·3·...·(2n - 1)}\\
&= \frac{(2n)!!}{(2n - 1)!!} > 1
\end{aligned}
$$
所以该级数在$x = 4$处发散。



























