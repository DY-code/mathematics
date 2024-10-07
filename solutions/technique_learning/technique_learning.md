ideas:

- ROS
- 使用树莓派搭建个人网站

学习网站

- [程序员鱼皮](https://space.bilibili.com/12890453)

### 学习路线参考

- 【|AI学习路线分享|做完这些，你已经成为机器学习方面的专家】 https://www.bilibili.com/video/BV16341177c1/?share_source=copy_web&vd_source=c6317e87993cd23a0e65d74c89d6599d

### tools

#### marktext

官网：https://www.marktext.cc/

github：https://github.com/marktext/marktext?tab=readme-ov-fil

### github

- [get started with github](https://docs.github.com/zh/get-started/start-your-journey/hello-world)

- personal access token for git on command line: [Managing your personal access tokens](https://docs.github.com/en/authentication/keeping-your-account-and-data-secure/managing-your-personal-access-tokens)

a temporary token: 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

###### github下载指定路径的文件

- [Github | 如何在Github上只下载一个文件或文件夹！？](https://blog.csdn.net/m0_72224305/article/details/127567759)

###### 使用git提交

简要步骤：

1. 获取已有的github仓库地址`[github_repository_url]`
2. 将仓库克隆到本地：

```
git clone [github_repository_url]
```

3. 在本地修改仓库后，执行`git add .`，将改动添加到本地仓库（用来准备下一次提交）
4. 将改动提交到本地仓库：

```
git commit -m "your_comment"
```

5. 将本地改动提交到github：

```
    git push origin [your_branch]
```

若提交到主分支，则执行：

```
git push origin main
```

参考：

- [提交文件到github的两种方法](https://blog.csdn.net/u013553529/article/details/59144904#:~:text=方法一：本地目录执行 git init，不执行 git clone 1 执行 git,） 3 执行 git push origin main 将本地工程提交到github)
- `git-add`：https://git-scm.com/docs/git-add

###### github加速：fast github

- [『FastGithub』一款.Net开源的稳定可靠Github加速神器，轻松解决GitHub访问难题](https://blog.csdn.net/qq_34202873/article/details/132543478)
- FastGithub for ubuntu chrome: [安装FastGithub从而实现加速github的步骤(Ubuntu)](https://blog.csdn.net/Lambert0320/article/details/132204181)

#### git

官网：https://git-scm.com/

### Linux

- [Linux官网](https://www.linux.org/)

- [Linux内核的官方网址](https://www.kernel.org/)

- [arm体系结构的源码网站](https://www.arm.linux.org.uk/developer/)

#### Linux命令

压缩和解压缩指定文件夹：

```
zip zipfile.zip ./path
unzip -o -d ./path myfile.zip
```

删除文件夹下的所有文件（夹）：

```
rm -rf *
```

#### 学习资料

- 怒肝 Linux 学习路线，这回不难 - 程序员鱼皮的文章 - 知乎https://zhuanlan.zhihu.com/p/420311740
- [【够全面够清晰】Linux超强学习路线图（思维导图）](https://blog.csdn.net/m0_61568580/article/details/121349408)

#### make/makefile

- 【译】一个简单的 make & makefile 教程 - JustSong的文章 - 知乎https://zhuanlan.zhihu.com/p/92010728
- 【[教程]Makefile的写法】 https://www.bilibili.com/video/BV1Mx411m7fm/?share_source=copy_web&vd_source=c6317e87993cd23a0e65d74c89d6599d

### markdown

- [Markdown输入公式、符号等语法汇总](https://blog.csdn.net/weixin_46098577/article/details/118308281?ops_request_misc=%257B%2522request%255Fid%2522%253A%2522164698148016780261973453%2522%252C%2522scm%2522%253A%252220140713.130102334.pc%255Fall.%2522%257D&request_id=164698148016780261973453&biz_id=0&utm_medium=distribute.pc_search_result.none-task-blog-2~all~first_rank_ecpm_v1~rank_v31_ecpm-11-118308281.pc_search_result_cache&utm_term=%E4%B8%8D%E7%AD%89%E4%BA%8E%E2%89%A0%E6%80%8E%E4%B9%88%E6%89%93&spm=1018.2226.3001.4187)

- 数学公式块中加粗字母，且不改变字体，示例：

$$
\pmb{x}
$$

###### 一些非常见用法

- 在正下方插入下标，示例：$\underset{x}{\min}$

- 其他特殊符号：$\mathbb{I}$

# LaTeX

官方文档：

- https://www.latex-project.org/help/documentation/

overleaf LaTeX教程：https://www.overleaf.com/learn/latex/Learn_LaTeX_in_30_minutes

书籍：

- 黄新刚LaTeX笔记：https://github.com/huangxg/lnotes

#### 页眉页脚设置

```latex
% 设置当前和随后的页面样式
\pagestyle{<style>}
% 仅设置当前页面的样式
\thispagestyle{<style>}
```

预定义的页面样式<style>：

- `empty`: no headers or footers on pages
- `plain`: no page headers, footers consist of a centered page number
- `headings`: no footers, headers contains class-specific information and page number
- `myheadings`: no footers, headers contains page number and user-supplied information

##### `fancyhdr` package

设置页眉和页脚：

```latex
\fancyhead[locations]{content}
\fancyfoot[locations]{content}
\fancyhf[locations]{content}
```

*locations*指定了*content*显示的位置，其位置定义以及示意图如下：

- `O(Odd) / E(Even)`：奇/偶数页（右/左页）
- `H(Header) / F(Footer)`：页眉/页脚
- `L(Left) / C(Center) / R(Right)`：左/中/右区域

![image-20240415170501537](images/image-20240415170501537.png)

使用示例：

```latex
\fancyhead{} % 清除页眉设置
\fancyhead[RO,LE]{this is header content} % 在 右页右边 和 左页左边 区域显示
```

#### counter的用法

在LaTeX中，counter相当于编程语言中的整型变量，可以用于对section等的计数

参考：https://www.overleaf.com/learn/latex/Counters

#### LaTeX的一些基础命令

##### 分页命令

```latex
\clearpage
\cleardoublepage
```

上述命令用于结束当前页并打印所有待显示的图片和表格。对于双面打印的文档，`\cleardoublepage`会将接下来的一页作为右边的页面（也就是奇数页码的页面，这意味着可能需要插入空白页）。

参考：

- https://latex2e.org/_005cclearpage-_0026-_005ccleardoublepage.html
- https://latex2e.org/Floats.html

##### 自定义命令

- `\newcommand`：定义新命令
- `\renewcommand`：重定义已有命令
- `\providecommand`：当命令不存在时，定义新命令；当命令已存在时，重新定义命令

#### 制作模板

overleaf 提供的教程：

- [Writing your own package](https://www.overleaf.com/learn/latex/Writing_your_own_package)
- [Writing your own class](https://www.overleaf.com/learn/latex/Writing_your_own_class)

overleaf 模板：https://cn.overleaf.com/latex/templates

参考资料：

- [如何写一个LaTeX类文件，并设计你自己的简历 ](https://www.cnblogs.com/super-zhang-828/p/7450133.html)

- [Can I write cls files in LaTeX instead of TeX?](https://stackoverflow.com/questions/3702222/can-i-write-cls-files-in-latex-instead-of-tex)

- [LaTeX2e for class and package writers guide](http://www.latex-project.org/guides/clsguide.pdf)

#### 字体设置

常见字号的对应关系参考：

- [Latex字体大小](https://blog.csdn.net/yhcwjh/article/details/116516011)

#### 图片和表格

- latex 表格单元格内分行的实现 - 大师姐的文章 - 知乎
  https://zhuanlan.zhihu.com/p/409241007

- 去掉图片和表格的标题中的冒号，并用空格代替：

```latex
% 去掉标题中的冒号 用空格代替
\usepackage{caption}
% 下面两行代码将冒号用空格代替，但是实测中空格没有添加成功
% \captionsetup[table]{labelsep=space} % 表
% \captionsetup[figure]{labelsep=space} % 图
% 采用自定义格式的方式进行修改
\DeclareCaptionLabelFormat{mylabel}{#1#2\hspace{1.5ex}}
\captionsetup[figure]{labelformat=mylabel,labelsep=none}
\captionsetup[table]{labelformat=mylabel,labelsep=none}
```

参考：[How to change spacing between caption numbering and text?](https://tex.stackexchange.com/questions/192449/how-to-change-spacing-between-caption-numbering-and-text)

#### 目录

使用tocloft宏包设置目录格式：

在目录中section和页码之间添加引导点：

```
\usepackage{tocloft}
\renewcommand{\cftsecleader}{\cftdotfill{\cftdotsep}}
```

其中，`\renewcommand`用于重定义命令，`\cftsecleader`用于定义section条目使用的引导线（通常定义为`\cftdotfill{\cft某dotsep}`），`\cftdotfill`命令用于绘制引导线，`\cftdotsep`命令指定了引导点之间的距离为默认距离。

有时为避免报错，可以在导入tocloft宏包时添加`subfigure`选项，即：

```
\usepackage[subfigure]{tocloft}
```

#### 摘要

设置摘要部分的字体样式：

```latex
\renewcommand{\abstractnamefont}{\fzlishu\bfseries\large} % 标题部分
\renewcommand{\abstracttextfont}{\fzkaiti} % 正文部分
```

参考：[Latex 摘要排版](https://blog.csdn.net/Happppppy_/article/details/106711999#:~:text=%E5%88%A9%E7%94%A8%E4%BB%A5%E4%B8%8B%E4%B8%A4%E4%B8%AA%E5%91%BD%E4%BB%A4%E8%AE%BE%E7%BD%AE%E6%91%98%E8%A6%81%E5%AD%97%E4%BD%93%EF%BC%9A%20renewcommand%7Babstractnamefont%7D%7Bfzlishubfserieslarge%7D%20renewcommand%7Babstracttextfont%7D%7Bfzkaiti%7D,1%202%20%E9%80%9A%E8%BF%87%E5%A6%82%E4%B8%8B%E5%91%BD%E4%BB%A4%E8%AE%BE%E7%BD%AE%E6%91%98%E8%A6%81%E6%A0%87%E9%A2%98%E4%B8%8E%E6%91%98%E8%A6%81%E5%86%85%E5%AE%B9%E7%9A%84%E9%97%B4%E8%B7%9D%EF%BC%9A%20setlength%7Babstitleskip%7D%7B-2em%7D)

### BibTex与文献数据库

##### 参考文献中作者名之间连接词“and”的处理

问题如下所示，可以看到除了连接词的问题，字体的样式也不统一。

![image-20240315202921321](images/image-20240315202921321.png)

可能的原因是unsrt格式无法对中文文献格式做特别处理，可采取的解决方法为：

注释掉参考文献导入处的格式设置代码：

```latex
% \bibliographystyle{unsrt}
```

并在导言区使用如下代码：

```latex
\usepackage{gbt7714}
% 如使用「顺序编码制」
\bibliographystyle{gbt7714-numerical}
% 如使用「著者-出版年制」方式的话，注释掉上一行，并将下一行取消注释
% \bibliographystyle{gbt7714-author-year}
```

最终效果：

![image-20240315214022958](images/image-20240315214022958.png)

参考：

- Latex中文文献中的作者连接词用的是"and"，请问如何处理？ - 知乎用户的回答 - 知乎
  https://www.zhihu.com/question/337951090/answer/772632131

##### 文献的引用次序问题

在BibTex的基本文献格式中，unsrt格式根据文献在正文中的引用次序来排序，即正文中引用文献的编号从上至下依次递增，参考文献处列出的文献条目次序也与引用次序一致。效果图和代码如下：

![image-20240315202921321](images/image-20240315202921321.png)

```latex
% test.tex
\documentclass{article}
% 中文支持
\usepackage[UTF8]{ctex}    

\begin{document}
引用了wangyi2018 \cite{name2}
引用了liangjun2015 \cite{name1}

% unsrt:保持引用次序
\bibliographystyle{unsrt}
% 插入ref.bib文件
\bibliography{ref}

\end{document}
```

```latex
% ref.bib
@article{name1,
author = {  刘翔月 and     张哲 and     蒋励 and     宋洪萱 and     姚殿祥 and     黄思怡 and     徐文杰 and     霍同林 and     周洪军 and     齐润泽 and     黄秋实 and     张众 and 王占山},

title = {极紫外光源用大口径Mo/Si多层膜厚度控制与热稳定性研究},
journal = {中国激光},
 pages = {1-16},
issn = {0258-7025},
}    

@article{name2,
author = {  乔志刚 and     高德辛 and     张牧子 and     赵姗姗 and     巫佳利 and     苏娟 and     陈胜功 and     景超 and     刘海玲 and     杨博 and 吴锜},

title = {用于温度传感器原位在线校准的水三相点自动复现控制系统},
journal = {红外与激光工程},
 pages = {1-4},
issn = {1007-2276},
}    
```

参考资料：

- 在LaTeX中如何引用参考文献 - MOON学术论文写作的文章 - 知乎
  https://zhuanlan.zhihu.com/p/265479955

###### 其他

- 论文参考文献规范格式详解 - 小咸鱼的文章 - 知乎
  https://zhuanlan.zhihu.com/p/29513792

## LaTeX Package

### listings

- [listings – Typeset source code listings using LATEX](https://ctan.org/pkg/listings#:~:text=To%20use%2C%20usepackage%20%7Blistings%7D%2C%20identify%20the%20language%20of,in%20the%20form%20appropriate%20for%20the%20current%20language.)

## 论文写作格式基础

### 摘要

中英文摘要应当基本对应，且通常需要放在独立的页面中

# python

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

- 查看指定文件夹下的所有路径以及文件数量

```python
import os
for dirname, _, filenames in os.walk('./datasets/mnist'):
     print(dirname) # 路径名
     print(len(filenames)) # 路径下的文件数量
```

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

# 深度学习

吴恩达：

- 【[双语字幕]吴恩达深度学习deeplearning.ai】 https://www.bilibili.com/video/BV1FT4y1E74V/?share_source=copy_web&vd_source=c6317e87993cd23a0e65d74c89d6599d

- 【(强推|双字)2022吴恩达机器学习Deeplearning.ai课程】 https://www.bilibili.com/video/BV1Pa411X76s/?p=150&share_source=copy_web&vd_source=c6317e87993cd23a0e65d74c89d6599d

配套资料：

1. https://github.com/robbertliu/deeplearning.ai-andrewNG
2. [【目录】【中文】【deplearning.ai】【吴恩达课后作业目录】](https://blog.csdn.net/u013733326/article/details/79827273)
3. [Deeplearning.ai深度学习教程中文笔记](https://github.com/fengdu78/deeplearning_ai_books)

李沐：

- [【完结】动手学深度学习 PyTorch版](https://space.bilibili.com/1567748478/channel/seriesdetail?sid=358497)

- 【李沐】动手学深度学习】 https://www.bilibili.com/video/BV18h411r7Z7/?share_source=copy_web&vd_source=c6317e87993cd23a0e65d74c89d6599d

源代码：

- 中文版：https://github.com/d2l-ai/d2l-zh?tab=readme-ov-file

- 英文版：https://github.com/d2l-ai/d2l-en

- 【PyTorch深度学习快速入门教程（绝对通俗易懂！）【小土堆】 https://www.bilibili.com/video/BV1hE411t7RN/?share_source=copy_web&vd_source=c6317e87993cd23a0e65d74c89d6599d

机器学习：

- [机器学习公式注解（南瓜书）](https://github.com/datawhalechina/pumpkin-book?tab=readme-ov-file)

### colab

- https://colab.research.google.com/

## pytorch

官网：https://pytorch.org/get-started/locally/

PyTorch官方文档：https://pytorch.org/docs/stable/index.html

- 【最详细的 Windows 下 PyTorch 入门深度学习环境安装与配置 CPU GPU 版 | 土堆教程】 https://www.bilibili.com/video/BV1S5411X7FY/?p=22&share_source=copy_web&vd_source=c6317e87993cd23a0e65d74c89d6599d
- 【PyTorch深度学习快速入门教程（绝对通俗易懂！）【小土堆】】 https://www.bilibili.com/video/BV1hE411t7RN/?share_source=copy_web&vd_source=c6317e87993cd23a0e65d74c89d6599d
- [狂肝两万字带你用pytorch搞深度学习！！！](https://blog.csdn.net/CltCj/article/details/120060543?ops_request_misc=%257B%2522request%255Fid%2522%253A%2522169620827216800184141626%2522%252C%2522scm%2522%253A%252220140713.130102334..%2522%257D&request_id=169620827216800184141626&biz_id=0&utm_medium=distribute.pc_search_result.none-task-blog-2~all~top_positive~default-1-120060543-null-null.142^v94^chatsearchT3_1&utm_term=pytorch&spm=1018.2226.3001.4187)

###### 常用包镜像

清华镜像：https://mirrors.tuna.tsinghua.edu.cn/anaconda/pkgs/main

北京外国语大学镜像：https://mirrors.bfsu.edu.cn/anaconda/pkgs/main

阿里巴巴镜像：http://mirrors.aliyun.com/anaconda/pkgs/main

南京大学镜像：https://mirror.nju.edu.cn/anaconda/pkgs/main/

- PyTorch镜像-pytorch, torchvision, torchaudio：

清华镜像：https://mirrors.tuna.tsinghua.edu.cn/anaconda/cloud/pytorch/win-64/

北京外国语大学镜像：https://mirrors.bfsu.edu.cn/anaconda/cloud/pytorch/win-64

阿里巴巴镜像：http://mirrors.aliyun.com/anaconda/cloud/pytorch/win-64/

南京大学镜像：https://mirror.nju.edu.cn/pub/anaconda/cloud/pytorch/win-64/

#### torchvision数据集使用

示例：

```python
import torchvision
from torch.utils.tensorboard import SummaryWriter

dataset_transform = torchvision.transforms.Compose([
    torchvision.transforms.ToTensor()
])

# 下载数据集到指定的路径 从训练集中创建数据集
# 将图片转换为tensor类型
train_set = torchvision.datasets.CIFAR10(root="./dataset", train=True, transform=dataset_transform, download=True)
test_set = torchvision.datasets.CIFAR10(root="./dataset", train=False, transform=dataset_transform,  download=True)

# 使用tensorboard展示前10张图片
writer = SummaryWriter("p10")
for i in range(10):
    img, target = test_set[i]
    writer.add_image("test_set", img, i)

writer.close()
```

#### Transforms

- 归一化`Normalize()`

计算公式：

```python
input[channel] = (input[channel] - mean[channel]) / std[channel]
```

- `Resize()`

- `Compose()`：把多个transforms步骤整合到一起

- `RandomCrop()`：随机裁剪

#### TensorBoard 数据可视化工具

- 本地启动TensorBoard：在命令行运行如下命令，可启动TensorBoard，其中dir_name为数据所在目录，默认为`logs`

```
tensorboard --logdir=<dir_name>
```

- 在jupyter notebook中启动TensorBoard，可使用如下代码：

```
%load_ext tensorboard  # 加载TensorBoard并允许将其用于可视化
%tensorboard --logdir logs  # 启动TensorBoard
```

在pytorch中的调用示例：

```python
from torch.utils.tensorboard import SummaryWriter
import random
import time

writer = SummaryWriter("logs")  # 创建一个log文件
for i in range(100):
    # add_scalar()添加数据，add_image()添加图片
    writer.add_scalar(tag="accuracy", # 可以暂时理解为图像的名字
                      scalar_value=i*random.uniform(0.8, 1),  # 纵坐标的值
                      global_step=i  # 当前是第几次迭代，可以理解为横坐标的值
                      )
    time.sleep(2 * random.uniform(0.5, 1.5))  # 模拟1~3秒完成一次迭代并计算准确率

writer.close()  # 训练结束后结束log写入
```

### pytorch notes

实用的两个工具（函数）：

- dir(): 查看工具箱的内容
- help(): 查看工具的使用方法

## 深度学习 notes

提高python程序执行效率的方法（尽量避免显式的for-loop）：

1. 向量化
2. 广播

#### 数学基础

##### 矩阵求导

列向量对行向量求导（一般使用分子布局）：
$$
\begin{aligned}
\frac{\partial y_{m \times 1}}{\partial x_{1 \times n}} &= 
\begin{bmatrix}
\frac{\partial y_1}{\partial x_{1 \times n}} \\
\frac{\partial y_2}{\partial x_{1 \times n}} \\
\vdots \\
\frac{\partial y_m}{\partial x_{1 \times n}} \\
\end{bmatrix} \\
&= \begin{bmatrix}
[\frac{\partial y_1}{\partial x_1},\ \frac{\partial y_1}{\partial x_2},\ ...,\ \frac{\partial y_1}{\partial x_n}] \\
[\frac{\partial y_2}{\partial x_1},\ \frac{\partial y_2}{\partial x_2},\ ...,\ \frac{\partial y_2}{\partial x_n}] \\
\vdots \\
[\frac{\partial y_m}{\partial x_1},\ \frac{\partial y_m}{\partial x_2},\ ...,\ \frac{\partial y_m}{\partial x_n}] \\
\end{bmatrix}
\end{aligned}_{m \times n}
$$
==注== 当分子为行向量时，默认作为列向量处理

常用矩阵求导公式：
$$
\frac{\partial (\pmb{x}^T\pmb{a})}{\partial \pmb{x}} = \frac{\partial (\pmb{a}^T\pmb{x})}{\partial \pmb{x}} = \pmb{a}
$$
参考：

- 矩阵求导的本质与分子布局、分母布局的本质（矩阵求导——本质篇） - Iterator的文章 - 知乎
  https://zhuanlan.zhihu.com/p/263777564

- 矩阵求导公式的数学推导（矩阵求导——基础篇） - Iterator的文章 - 知乎
  https://zhuanlan.zhihu.com/p/273729929

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

<img src="images/image-20240229204344149.png" alt="image-20240229204344149" style="zoom: 33%;" />

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

<img src="images/image-20240302105107689.png" alt="image-20240302105107689" style="zoom:50%;" />

- tanh: 

$$
tanh(z) = \frac{e^{z} - e^{-z}}{e^{z} + e^{-z}} \\
tanh'(z) = 1 - tanh^2(z)
$$

<img src="images/image-20240302105145302.png" alt="image-20240302105145302" style="zoom:50%;" />

- ReLU（Rectified Liner Unit，学习速度更快）: 

$$
ReLU(z) = \max(0,\ z) \\
ReLU'(z) = 
\begin{cases}
0,\ z < 0 \\
1,\ z \ge 0
\end{cases}
$$

<img src="images/image-20240302105202878.png" alt="image-20240302105202878" style="zoom:50%;" />

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

<img src="images/image-20240302105258320.png" alt="image-20240302105258320" style="zoom:50%;" />

#### forward propogation

以两层网络为例：

<img src="images/image-20240302101541463.png" alt="image-20240302101541463" style="zoom:50%;" />

- $a^{[l]}_{i}$：activation，表示网络中第$l$层第$i$个神经元的值，且$a^{[0]} = X$

- $a^{[l](i)}$：第$i$个训练样本下第$l$层的值

- $n^{[l]}$：第$l$层的节点数，$n^{[0]} = n_x,\ n^{[1]} = 4,\ n^{[2]} = 1$

- 变量的shape: 

$$
\begin{aligned}
W^{[l]} &:\ (n^{[l]},\ n^{[n-1]}) \\
b^{[l]} &:\ (n^{[l]},\ 1) \\
dW^{[l]} &:\ (n^{[l]},\ n^{[n-1]}) \\
db^{[l]} &:\ (n^{[l]},\ 1) \\
Z^{[l]} &:\ (n^{[l]},\ m) \\
A^{[l]} &:\ (n^{[l]},\ m)
\end{aligned}
$$

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

- $dZ^{[2]} = \frac{\partial J}{\partial Z^{[2]}},\ Z^{[2]}_{1 \times m}(m个样本)$

- $$
  \begin{aligned}
  A^{[2]} &= [A^{[2](1)},\ A^{[2](2)},\ ...,\ A^{[2](m)}] \\
  &= [a^{[2](1)},\ a^{[2](2)},\ ...,\ a^{[2](m)}]_{1 \times m} \\
  \end{aligned}
  $$

$$
\begin{aligned}
dZ^{[2]} &= [dz^{[2](1)},\ dz^{[2](2)},\ ...,\ dz^{[2](m)}]
\end{aligned}
$$

- $Y = [y^{(1)},\ y^{(2)},\ ...,\ y^{(m)}]_{1 \times m}$
- 第2层输出层只有1个节点，采用sigmoid函数，参考logistic regression部分，有：

$$
\frac{\partial \mathscr{l}}{\partial z} = a - y \\
dz = \frac{\partial J}{\partial z} = \frac{1}{m}\sum_{i=1}^m\frac{\partial \mathscr{l}^{(i)}}{\partial z} = \frac{1}{m}\sum_{i=1}^m(a^{(i)} - y^{(i)})
$$

![image-20240302120903407](images/image-20240302120903407.png)

![image-20240302175920902](images/image-20240302175920902.png)

#### gradient descent

![image-20240302181330158](images/image-20240302181330158.png)

对单个样本的梯度计算：
$$
\begin{aligned}
dz^{[2]} &= a^{[2]} - y \\
dW^{[2]} &= dz^{[2]}a^{[1]T} \\
db^{[2]} &= dz^{[2]} \\
dz^{[1]} &= W^{[2]T}dz^{[2]} * g^{[1]}{'}(z^{[1]}) \\
dW^{[1]} &= dz^{[1]}x^T \\
db^{[1]} &= dz^{[1]}
\end{aligned}
$$

==注意== "$*$"表示逐元素乘积（element-wize）

==说明== 

对于第$i$个样本，有：
$$
dz^{[2](i)} = a^{[2](i)} - y^{(i)}
$$
令：
$$
\begin{aligned}
dZ^{[2]} &= [dz^{[2](1)},\ dz^{[2](2)},\ ...,\ dz^{[2](m)}] \\
A^{[2]} &= [a^{[2](1)},\ a^{[2](2)},\ ...,\ a^{[2](m)}] \\
Y &= [y^{(1)},\ y^{(2)},\ ...,\ y^{(m)}]
\end{aligned}
$$
则向量化表示可写为：
$$
dZ^{[2]} = A^{[2]} - Y
$$

----------------------------------------------------------------------------------------------------------------

由于：
$$
Z^{[2]}_{1 \times m} = W^{[2]}_{1 \times 4}A^{[1]}_{4 \times m} + b^{[2]}
$$
则有：
$$
\frac{\partial Z^{[2]}_{1 \times m}}{\partial W^{[2]}_{1 \times 4}} = A^{[1]T}_{m \times 4}
$$
存在如下对应关系：
$$
z^{[2](i)} \sim a^{[2](i)} \sim \mathscr{l}(a^{[2](i)},\ y^{(i)}) \\
J = \frac{1}{m}\sum_{i=1}^m\mathscr{l}(a^{[2](i)},\ y^{(i)})
$$
故$J$可以看做向量$Z^{[2]}_{1 \times m}$的函数，对其求偏导数有：
$$
\begin{aligned}
\frac{\partial J}{\partial Z^{[2]}}|_{1 \times m} &= [\frac{\partial J}{\partial z^{[2](1)}},\ \frac{\partial J}{\partial z^{[2](2)}},\ ...,\ \frac{\partial J}{\partial z^{[2](m)}}] \\
&= \frac{1}{m}[\frac{\partial \mathscr{l}^{(1)}}{\partial z^{[2](1)}},\ \frac{\partial \mathscr{l}^{(2)}}{\partial z^{[2](2)}},\ ...,\ \frac{\partial \mathscr{l}^{(m)}}{\partial z^{[2](m)}}] \\
&= \frac{1}{m}dZ^{[2]}
\end{aligned}
$$
进而有：
$$
dW^{[2]}_{1 \times 4} = \frac{\partial J}{\partial Z^{[2]}}\frac{\partial Z^{[2]}}{\partial W^{[2]}} = \frac{1}{m}dZ^{[2]}_{1 \times m}A^{[1]T}_{m \times 4} \quad (a)
$$
事实上，对于单个样本$(i)$有：
$$
dW^{[2]}_{1 \times 4} = dz^{[2]}_{1 \times 1}a^{[1]T}|_{1 \times 4}
$$
可以将式$(a)$改写为如下形式：
$$
\begin{aligned}
dW^{[2]}_{1 \times 4} &= dZ^{[2]}_{1 \times m} A^{[1]T}_{m \times 4} \\
&= \frac{1}{m}[dz^{[2](1)},\ dz^{[2](2)},\ ...,\ dz^{[2](m)}]
\begin{bmatrix}
a^{[1](1)T} \\
a^{[1](2)T} \\
\vdots \\
a^{[1](m)T} \\
\end{bmatrix} \\
&= \frac{1}{m}\sum_{i=1}^m dz^{[2](i)}_{1 \times 1} a^{[1](i)T}|_{1 \times 4}
\end{aligned}
$$

### 深层神经网络

#### forward propagation

$$
z^{[l]}_{n^{[l]} \times 1} = W^{[l]}_{n^{[l]} \times n^{[l-1]}}a^{[l-1]}_{n^{[l-1]} \times 1} + b^{[l]}_{n^{[l]} \times 1} \\
a^{[l]}_{n^{[l]} \times 1} = g^{[l]}(z^{[l]}_{n^{[l]} \times 1})
$$

向量化：
$$
Z^{[l]}_{n^{[l]} \times m} = W^{[l]}_{n^{[l]} \times n^{[l-1]}}A^{[l-1]}_{n^{[l-1]} \times m} + b^{[l]}_{n^{[l]} \times 1} \\
A^{[l]}_{n^{[l]} \times m} = g^{[l]}(Z^{[l]}_{n^{[l]} \times m})
$$
注：$X = A^{[0]}$

#### backward propagation

$$
dW^{[l]} = \frac{\partial J}{\partial W^{[l]}} = \frac{1}{m}dZ^{[l]}A^{[l-1]T} \\
db^{[l]} = \frac{\partial J}{\partial b^{[l]}} = \frac{1}{m}\sum_{i=1}^mdZ^{[l](i)} \\
dA^{[l-1]} = \frac{\partial J}{\partial A^{[l-1]}} = W^{[l]T}dZ^{[l]}
$$

## 序列模型

### RNN

#### notation

$x^{(i)<t>}$：第$i$个样本中第$t$个元素

$T_x^{(i)}$：第$i$个训练样本的输入序列长度

$y^{(i)<t>}$：第$i$个训练样本输出序列中第$t$个元素

$T_y^{(i)}$：第$i$个训练样本输出序列的长度

#### notes

##### one-hot representation

使用一个向量来表示一个单词，其中只有一个元素是1，其余都为0

![image-20240310110313764](images/image-20240310110313764.png)

##### forward propagation

![image-20240307153440457](images/image-20240307153440457.png)
$$
a^{<t>} = g(W_{aa}a^{<t-1>} + W_{ax}x^{<t>} + b_a) \\
\hat{y}^{<t>} = g(W_{ya}a^{<t>} + b_y)
$$
simplified notation: 
$$
a^{<t>} = g(W_a[a^{<t-1>},\ x^{<t>}] + b_a) \\
\hat{y}^{<t>} = g(W_ya^{<t>} + b_y) \\
$$
其中：
$$
W_a = [W_{aa},\ W_{ax}] \\
[a^{<t-1>},\ x^{<t>}] = 
\begin{bmatrix}
a^{<t-1>} \\
x^{<t>}
\end{bmatrix} \\
W_{ya} = W_y
$$

##### summary of RNN types

![image-20240311092057576](images/image-20240311092057576.png)

#### 说明

RNN存在的问题：

- 梯度消失
- 梯度爆炸

### GRU

memory cell: 

<img src="images/image-20240311113034124.png" alt="image-20240311113034124" style="zoom: 50%;" />
$$
\begin{aligned}
\tilde{c}^{<t>} &= \tanh(W_c[c^{<t-1>},\ x^{<t>}] + b_c) \\
\Gamma_u &= \sigma(W_u[c^{<t-1>},\ x^{<t>}] + b_u) \\
c^{<t>} &= \Gamma_u * \tilde{c}^{<t>} + (1 - \Gamma_u) * c^{<t-1>}
\end{aligned}
$$

### LSTM

<img src="images/image-20240310100454479.png" alt="image-20240310100454479" style="zoom:50%;" />

<img src="images/image-20240310100552993.png" alt="image-20240310100552993" style="zoom:50%;" />

#### 参考

- [Understanding LSTM Networks](https://colah.github.io/posts/2015-08-Understanding-LSTMs/)
- [如何从RNN起步，一步一步通俗理解LSTM](https://blog.csdn.net/v_JULY_v/article/details/89894058?ops_request_misc=%257B%2522request%255Fid%2522%253A%2522171003374916800222894872%2522%252C%2522scm%2522%253A%252220140713.130102334..%2522%257D&request_id=171003374916800222894872&biz_id=0&utm_medium=distribute.pc_search_result.none-task-blog-2~all~top_positive~default-1-89894058-null-null.142^v99^pc_search_result_base7&utm_term=lstm&spm=1018.2226.3001.4187)

## 时间序列预测

- 【吴恩达团队Tensorflow2.0实践系列课程第四课】序列、时间序列和预测】 https://www.bilibili.com/video/BV1qE411u7z4/?share_source=copy_web&vd_source=c6317e87993cd23a0e65d74c89d6599d

### transformer

# 图像处理与计算机视觉

计算机视觉领域可使用的数据集：COCO

参考：[Dataset之COCO数据集：COCO数据集的简介、下载、使用方法之详细攻略](https://blog.csdn.net/qq_41185868/article/details/82939959)

### face_recognition

dlib的github官网：https://github.com/davisking/dlib

似乎找不到ubuntu下dlib的.whl文件，可以尝试手动编译安装

- [ubuntu20.04安装Dlib方法](https://zhuanlan.zhihu.com/p/449942621)

- [[已解决]face_recognition库安装，dlib库安装](https://blog.csdn.net/weixin_53236070/article/details/124306424)

## opencv

### opencv python

文档

- 官网教程：[OpenCV-Python Tutorials](https://docs.opencv.org/4.x/d6/d00/tutorial_py_root.html)

- 摄像头参数详解：[Flags for video I/O](https://docs.opencv.org/3.4/d4/d15/group__videoio__flags__base.html) 

教程：

- 【3h精通Opencv-Python】 https://www.bilibili.com/video/BV16K411W7x9/?share_source=copy_web&vd_source=c6317e87993cd23a0e65d74c89d6599d

#### 安装opencv-python

- 使用镜像文件安装opencv-python: https://blog.csdn.net/weixin_44756050/article/details/104825269
- opencv-python镜像文件网站：https://mirrors.tuna.tsinghua.edu.cn/pypi/web/simple/opencv-python/

镜像文件的文件名中，cp39代表python3.9，注意区分操作系统的类型（win/linux, 32/64）。下载镜像文件后，采用本地安装的方式，执行如下命令即可安装：

```
pip install opencv_python-4.5.4.60-cp39-cp39-win_amd64.whl
```

## yolo

作者的yolo网页：https://pjreddie.com/darknet/yolov1/

- [YOLO系列算法精讲：从yolov1至yolov8的进阶之路（2万字超全整理）](https://blog.csdn.net/wjinjie/article/details/107509243?ops_request_misc=%257B%2522request%255Fid%2522%253A%2522170901435516800211595559%2522%252C%2522scm%2522%253A%252220140713.130102334..%2522%257D&request_id=170901435516800211595559&biz_id=0&utm_medium=distribute.pc_search_result.none-task-blog-2~all~top_positive~default-1-107509243-null-null.142^v99^pc_search_result_base7&utm_term=yolo&spm=1018.2226.3001.4187)

- 【百万播放】零基础、快速学YOLO目标检测算法！完整学习路线一条龙，无脑通关！【YOLOv5|YOLO算法|目标检测算法】】 https://www.bilibili.com/video/BV1XW4y1a7f4/?p=14&share_source=copy_web&vd_source=c6317e87993cd23a0e65d74c89d6599d

### yolov1

- 【精读AI论文】YOLO V1目标检测，看我就够了】 https://www.bilibili.com/video/BV15w411Z7LG/?share_source=copy_web&vd_source=c6317e87993cd23a0e65d74c89d6599d

### yolov5

yolov5 github: https://github.com/ultralytics/yolov5?tab=readme-ov-file

### yolov7

yolov7 github: https://github.com/WongKinYiu/yolov7

## 数字图像处理

###### edge detection 边缘检测

在进行边缘检测之前往往需要对图像进行平滑和去噪，此外还有阈值处理等

- Sobel operators/kernels（B719）

<img src="images/image-20240414152342165.png" alt="image-20240414152342165" style="zoom:50%;" />

Sobel kernels拥有更好的图像平滑和噪声抑制的特性

# control theory

![Control_Map_ver5](images/Control_Map_ver5.png)

interesting theory: 

- kalman filter

# 机器人
