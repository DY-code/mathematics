- 注意计算题

# 试题

- [计算机网络试题及答案（史上最全）](https://blog.csdn.net/weixin_43474701/article/details/118760202?ops_request_misc=%257B%2522request%255Fid%2522%253A%2522170088248616800192216926%2522%252C%2522scm%2522%253A%252220140713.130102334..%2522%257D&request_id=170088248616800192216926&biz_id=0&utm_medium=distribute.pc_search_result.none-task-blog-2~all~sobaiduend~default-1-118760202-null-null.142^v96^pc_search_result_base1&utm_term=%E8%AE%A1%E7%AE%97%E6%9C%BA%E7%BD%91%E7%BB%9C%E8%80%83%E8%AF%95%E8%AF%95%E9%A2%98&spm=1018.2226.3001.4187)

## 名词解释

## 简答

### 请简述以太网的工作原理和数据传输过程

以太网是总线型局域网，任何节点都没有可预约的发送时间，它们的发送是随机的，网络中不存在集中控制节点。以太网的节点发送数据是通过“广播”方式将数据送往共享介质，概括为“[先听后发，边听边发，冲突停止，延迟重发]()”。

### 试从多个方面比较共享式以太网和交换式以太网

共享式以太网：组建简单、便宜、但覆盖地理范围有限，网络总带宽固定，随着节点数的增加，冲突碰撞加大，浪费加大，不支持多速。
交换式以太网：增加了交换机，以分段方式将一个大型以太网分割成多个小型以太网，段与段之间通过交换设备沟通，由于分成小型网，节点数减少，冲突碰撞浪费减少，各段可按需要选择自己的网络速率。

## 计算

### Z4-15

![image-20231125125923328](C:\Users\Joker\AppData\Roaming\Typora\typora-user-images\image-20231125125923328.png)

![image-20231125125939380](C:\Users\Joker\AppData\Roaming\Typora\typora-user-images\image-20231125125939380.png)

# 第1章 概述

## 互联网的组成

## 1.5 计算机网络的类别

### 1.5.2 几种不同类别的网络

#### 按网络的作用范围进行分类

<img src="C:\Users\Joker\AppData\Roaming\Typora\typora-user-images\image-20231123205737967.png" alt="image-20231123205737967" style="zoom:67%;" />

## 1.6 计算机网络的性能

### 1.6.1 计算机网络的性能指标

#### 速率

#### 带宽

$$
\begin{cases}
数字 \rightarrow 最大传输能力 \ (bit/s) \\
\\
模拟 \rightarrow 传输频率 \ (Hz)
\end{cases}
$$

<img src="C:\Users\Joker\AppData\Roaming\Typora\typora-user-images\image-20230910102532817.png" alt="image-20230910102532817" style="zoom:67%;" />

#### 吞吐量

#### ==时延==

总时延 = [发送]()时延 + [传播]()时延 + [处理]()时延 + [排队]()时延

==注意== 容易产生的错误概念

<img src="C:\Users\Joker\AppData\Roaming\Typora\typora-user-images\image-20230910100311699.png" alt="image-20230910100311699" style="zoom:67%;" />

##### 组成

- 发送时延（也称传输时延）

<img src="C:\Users\Joker\AppData\Roaming\Typora\typora-user-images\image-20230910095645460.png" alt="image-20230910095645460" style="zoom:67%;" />

- 传播时延

<img src="C:\Users\Joker\AppData\Roaming\Typora\typora-user-images\image-20230910095743901.png" alt="image-20230910095743901" style="zoom:50%;" />

- 处理时延

<img src="C:\Users\Joker\AppData\Roaming\Typora\typora-user-images\image-20230910095826670.png" alt="image-20230910095826670" style="zoom: 67%;" />

- 排队时延

<img src="C:\Users\Joker\AppData\Roaming\Typora\typora-user-images\image-20230910095847369.png" alt="image-20230910095847369" style="zoom:67%;" />

##### 时延的产生地

<img src="C:\Users\Joker\AppData\Roaming\Typora\typora-user-images\image-20230910100144540.png" alt="image-20230910100144540" style="zoom:67%;" />

#### 时延带宽积

#### 往返时间RTT

#### 利用率

## 1.7 计算机网络的体系结构

### 1.7.3 ==具有五层协议的体系结构== P139

![image-20231120165931941](C:\Users\Joker\AppData\Roaming\Typora\typora-user-images\image-20231120165931941.png)

# 第2章 物理层

## 物理层的基本概念

## 2.2 数据通信的基础知识

### 2.2.1 数据通信系统的模型

### 2.2.2 有关信道的几个基本概念

#### ==调制== P13

- [基带]()调制
- [带通]()调制

![image-20231123233313763](C:\Users\Joker\AppData\Roaming\Typora\typora-user-images\image-20231123233313763.png)

#### ==曼彻斯特编码== P14

位中心[向上跳变]()代表0，[向下跳变]()代表1：

![image-20231120102603540](C:\Users\Joker\AppData\Roaming\Typora\typora-user-images\image-20231120102603540.png)

#### ==基本的带通调制方法==

- [调幅]()
- [调频]()
- [调相]()

![image-20231120102859581](C:\Users\Joker\AppData\Roaming\Typora\typora-user-images\image-20231120102859581.png)

### 2.2.3 信道的极限容量

#### 信噪比

信噪比 = 信号的平均功率 / 噪声的平均功率，记为$S / N$，用分贝作为度量单位（$dB$）：
$$
信噪比(dB) = 10\log_{10}(S/N) \ (dB)
$$

#### *香农公式* P28

带宽受限且有高斯白噪声干扰的信道的极限、无差错的信息传输速率：
$$
C = W\log_2(1 + S/N) \ (bit/s)
$$
==说明==

- 信道的带宽或信噪比越大，则信道的**极限传输速率**越高
- 只要信息传输速率低于信道的极限信息传输速率，就一定可以以某种方法实现无差错的传输
- 若信道带宽$W$或信道信噪比$S/N$无上限，则信道的极限传输速率无上限（实际信道不可能这样）

==注意== 在信道带宽已确定、信噪比和码元传输速率无法再提高的情况下，如何提高信息的传输速率：用编码的方法让每一个码元携带更多比特的信息量

## 2.3 物理层下面的传输媒体

### 2.3.1 *导引型传输媒体* P32

- 双绞线
- 同轴电缆

#### 光缆

##### 多模光纤与单模光纤

<img src="C:\Users\Joker\AppData\Roaming\Typora\typora-user-images\image-20231123231837788.png" alt="image-20231123231837788" style="zoom: 67%;" />

##### ==光纤优点== P44

1. 通信容量非常大
2. 传输损耗小，中继距离长
3. 抗电磁干扰性能好
4. 无串音干扰，保密性好
5. 体积小，重量轻

## 2.4 信道复用技术

### 2.4.1 ==频分复用==、==时分复用==和统计时分复用

- 频分复用：在[同样的时间]()里占用[不同的带宽资源]()
- 时分复用：在[不同的时间]()占用[相同的频带宽度]()

#### 频分复用

![image-20231120104844381](C:\Users\Joker\AppData\Roaming\Typora\typora-user-images\image-20231120104844381.png)

#### 时分复用

![image-20231120105035228](C:\Users\Joker\AppData\Roaming\Typora\typora-user-images\image-20231120105035228.png)

![image-20231120110715297](C:\Users\Joker\AppData\Roaming\Typora\typora-user-images\image-20231120110715297.png)

### 2.4.2 波分复用

### 2.4.3 ==码分复用==

![image-20231120110839281](C:\Users\Joker\AppData\Roaming\Typora\typora-user-images\image-20231120110839281.png)

## 宽带接入技术

# 第3章 数据链路层

## 3.1 使用点对点信道的数据链路层

### 3.1.2 ==三个基本问题== P11

- [封装成帧]()
- [透明传输]()
- [差错控制]()

#### 封装成帧

在一段数据的前后分别添加首部和尾部，构成一个帧。

#### 透明传输

如果数据中的某个字节的二进制代码恰好和SOH(Start Of Header)或EOT(End Of Transmission)一样，数据链路层就会错误地“找到帧的边界”。

- 解决透明传输问题

字节填充或字符填充：

![image-20231120111838849](C:\Users\Joker\AppData\Roaming\Typora\typora-user-images\image-20231120111838849.png)

![image-20231120111918526](C:\Users\Joker\AppData\Roaming\Typora\typora-user-images\image-20231120111918526.png)

#### 差错控制

##### ==循环冗余检验CRC（计算）==

假设待传送的一组数据$M$，含$k$个比特，在$M$的后面添加供差错检测用的$n$位冗余码一起发送。

- 冗余码的计算

模2减法（按位异或）：
$$
0 - 0 = 1 - 1 = 0 \\
0 - 1 = 1 - 0 = 1
$$
模2除法（二进制除法 + 模2减法），示例：

<img src="C:\Users\Joker\AppData\Roaming\Typora\typora-user-images\image-20231120112955780.png" alt="image-20231120112955780" style="zoom:67%;" />

冗余码的计算步骤：

![image-20231120113126096](C:\Users\Joker\AppData\Roaming\Typora\typora-user-images\image-20231120113126096.png)

示例：

![image-20231120113101013](C:\Users\Joker\AppData\Roaming\Typora\typora-user-images\image-20231120113101013.png)

##### ==循环冗余检验的原理说明== P22

检验方式：把收到的每一帧除以同样的除数P，检查得到的余数R：

<img src="C:\Users\Joker\AppData\Roaming\Typora\typora-user-images\image-20231120113801246.png" alt="image-20231120113801246" style="zoom:67%;" />

==注意==

- 仅用循环冗余检验CRC差错检测技术只能做到**无差错接受**
- 无差错接受：凡是接受的帧（不包括丢弃的帧），都能以非常接近1的概率认为这些帧在传输过程中没有产生差错。
- 要做到“可靠传输”（即发送什么就收到什么），必须加上确认和重传机制。

###### 帧检验序列FCS

**在数据后面添加上的冗余码**称为帧检验序列FCS

==注== 循环冗余检验CRC是一种常用的检错方法，帧检验序列FCS是添加在数据后面的冗余码。

## 3.2 使用广播信道的数据链路层

### 3.3.2 ==CSMA/CD协议== P37

[载波监听多点接入/碰撞检测]()（Carrier Sense Multiple Access with Collision Detection）

- 多点接入：许多计算机以多点接入的方式连接在[一根总线]()上
- 载波监听：每个站在[发送数据之前]()先检测总线上[是否有其他计算机在发送数据]()，若有则暂时不要发送数据，以免发生碰撞
- 碰撞检测：计算机边发送数据边[检测信道上的信号电压大小]()
- 争用期

![image-20231124000314180](C:\Users\Joker\AppData\Roaming\Typora\typora-user-images\image-20231124000314180.png)

#### ==CSMA/CD协议的要点== 

![image-20231120114715930](C:\Users\Joker\AppData\Roaming\Typora\typora-user-images\image-20231120114715930.png)

### 3.3.3 使用集线器的星形拓扑

#### ==集线器== P60

集线器的一些特点：

![image-20231120115324284](C:\Users\Joker\AppData\Roaming\Typora\typora-user-images\image-20231120115324284.png)

### 3.3.5 以太网的MAC层

#### ==MAC层的硬件地址== P62

在局域网中，[硬件地址]()又称为[物理地址]()，或[MAC地址]()。

48位的MAC地址：

![image-20231120115845427](C:\Users\Joker\AppData\Roaming\Typora\typora-user-images\image-20231120115845427.png)

## 3.4 扩展的以太网

### 3.4.2 在数据链路层扩展以太网

#### ==以太网交换机== P80

##### 以太网交换机的特点

![image-20231120161349096](C:\Users\Joker\AppData\Roaming\Typora\typora-user-images\image-20231120161349096.png)

![image-20231120161404727](C:\Users\Joker\AppData\Roaming\Typora\typora-user-images\image-20231120161404727.png)

##### 以太网交换机的优点

![image-20231120161453319](C:\Users\Joker\AppData\Roaming\Typora\typora-user-images\image-20231120161453319.png)

##### 以太网交换机的交换方式

![image-20231120161608969](C:\Users\Joker\AppData\Roaming\Typora\typora-user-images\image-20231120161608969.png)

### 3.4.3 ==虚拟局域网== P87

虚拟局域网VLAN（Virtual LAN）

- 虚拟局域网VLAN是由一些局域网网段构成的[与物理位置无关]()的逻辑组，这些网段具有某些共同的需求。每一个VLAN的帧都有一个明确的标识符，指明发送这个帧的计算机是属于哪一个VLAN

- 虚拟局域网是局域网给用户提供的一种服务，并不是一种新型局域网

# 第4章 网络层 ==重点==

## 4.1 网络层提供的两种服务

- 虚电路服务
- 数据报服务

![image-20230926234653866](C:\Users\Joker\AppData\Roaming\Typora\typora-user-images\image-20230926234653866.png)

### 虚电路服务

虚电路服务：面向连接

![image-20231124001648902](C:\Users\Joker\AppData\Roaming\Typora\typora-user-images\image-20231124001648902.png)

### ==数据报服务== P6

无连接的、尽最大努力交付的**数据报服务**

![image-20231120162419607](C:\Users\Joker\AppData\Roaming\Typora\typora-user-images\image-20231120162419607.png)

#### 尽最大努力交付

- 传输网络[不提供端到端的可靠传输服务]()
- 若需要可靠通信，则由主机中的运输层负责可靠交付（包括差错处理、流量控制等）

## 4.2 网际协议IP（Internet Protocol）

注：IP是网际协议的名字，与IP协议配套使用的还有三个协议：

- [地址解析协议ARP]()
- [网际控制报文协议ICMP]()
- 网际组管理协议IGMP（不涉及）

### 虚拟互连网络

### 4.2.2 分类的IP地址

#### IP地址及其表示方法

![image-20231123235054403](C:\Users\Joker\AppData\Roaming\Typora\typora-user-images\image-20231123235054403.png)

两级IP地址结构：

<img src="C:\Users\Joker\AppData\Roaming\Typora\typora-user-images\image-20230926235745138.png" alt="image-20230926235745138" style="zoom: 67%;" />

#### 常用的三种类别的IP地址

![image-20230926235812763](C:\Users\Joker\AppData\Roaming\Typora\typora-user-images\image-20230926235812763.png)

#### ==互联网中的IP地址（图，理解）== P40

- 在同一个局域网上的主机或路由器的**IP地址中的网络号**必须相同
- **路由器**总是具有两个或以上的IP地址，每一个接口都有一个不同网络号的IP地址

### 4.2.3 IP地址与硬件地址

<img src="C:\Users\Joker\AppData\Roaming\Typora\typora-user-images\image-20231123235400353.png" alt="image-20231123235400353" style="zoom: 67%;" />

![image-20231123235324016](C:\Users\Joker\AppData\Roaming\Typora\typora-user-images\image-20231123235324016.png)

#### ==图：从协议栈的层次上看数据的流动（理解）== P53

### 4.2.4 ==地址解析协议ARP== ==重要== P61

地址解析协议ARP（Address Resolution Protocol）

- IP地址--网络层地址（可变）
- MAC地址--数据链路层地址（不可变）

地址解析协议ARP的作用：由主机或路由器的IP地址，找出其相应的硬件MAC地址

![image-20230927000123417](C:\Users\Joker\AppData\Roaming\Typora\typora-user-images\image-20230927000123417.png)

#### 地址解析协议ARP要点

![image-20231120164857908](C:\Users\Joker\AppData\Roaming\Typora\typora-user-images\image-20231120164857908.png)

![image-20231120164909813](C:\Users\Joker\AppData\Roaming\Typora\typora-user-images\image-20231120164909813.png)

- ARP高速缓存的作用

存放最近获得的IP地址到MAC地址的绑定，以减少ARP广播的数量。

#### 使用ARP的四种典型情况

![image-20230927000255749](C:\Users\Joker\AppData\Roaming\Typora\typora-user-images\image-20230927000255749.png)

### 4.2.5 ==IP数据报的格式== P74

- 首部的前一部分是固定长度，共[20字节]()，是所有IP数据报必须具有的。

![image-20230927000419242](C:\Users\Joker\AppData\Roaming\Typora\typora-user-images\image-20230927000419242.png)

![image-20230927000446886](C:\Users\Joker\AppData\Roaming\Typora\typora-user-images\image-20230927000446886.png)

### 4.2.6 ==IP层转发分组的流程== P95

路由表的结构：目的网络地址 + 下一跳地址

![image-20231120170933288](C:\Users\Joker\AppData\Roaming\Typora\typora-user-images\image-20231120170933288.png)

查找路由表：由目的网络地址可以确定下一跳路由器

- 通过多次**间接交付**最终可以找到目的主机所在目的网络上的路由器
- 到达最后一个路由器时，向目的主机进行**直接交付**

==注== 路由表没有给出到某个网络的完整路径，而是指出应当先到哪个下一跳路由器。

## 4.3 划分子网

### 4.3.1 划分子网

#### 三级IP地址

![image-20230927000727302](C:\Users\Joker\AppData\Roaming\Typora\typora-user-images\image-20230927000727302.png)

![image-20230927000920093](C:\Users\Joker\AppData\Roaming\Typora\typora-user-images\image-20230927000920093.png)

划分子网所用的字段属于原IP地址的[主机号部分]()。

#### ==子网掩码（计算）== P109

网络地址 = IP地址 AND与 子网掩码 

![image-20230927001019714](C:\Users\Joker\AppData\Roaming\Typora\typora-user-images\image-20230927001019714.png)

##### 默认子网掩码

![image-20231120202840466](C:\Users\Joker\AppData\Roaming\Typora\typora-user-images\image-20231120202840466.png)

==注意== 一般情况下，[子网号不能为全0或全1]()

### 4.3.2 使用子网时分组的转发

#### ==例4-4== P122

![image-20231124102433432](C:\Users\Joker\AppData\Roaming\Typora\typora-user-images\image-20231124102433432.png)

![image-20231120204413452](C:\Users\Joker\AppData\Roaming\Typora\typora-user-images\image-20231120204413452.png)

## 4.4 ==网际控制报文协议ICMP== P128

- 网际控制报文协议ICMP（Internet Control Message Protocol），为IP层的协议。

- ICMP允许主机或路由器报告差错情况和提供有关异常情况的报告。

### 4.4.1 ICMP报文的种类

- ICMP差错报告报文

差错报告报文共有4种：

1. 终点不可达
2. 时间超过
3. 参数问题
4. 改变路由（重定向）

- ICMP询问报文

询问报文共两种：

1. 回送请求和回答报文
2. 时间戳请求和回答报文

### 4.4.2 ICMP的应用举例

#### ==PING==（Packet InterNet Groper）

- 用来测试两个主机之间的连通性
- 使用ICMP回送请求与回送回答报文
- PING是应用层直接使用网络层ICMP的例子，没有通过运输层的TCP或UDP

## 4.5 互联网的路由选择协议

### 有关路由选择协议的几个基本概念

#### 理想的路由算法

- 关于“最佳路由”

#### 分层次的路由选择协议

##### 自治系统AS

![image-20230927001934790](C:\Users\Joker\AppData\Roaming\Typora\typora-user-images\image-20230927001934790.png)

##### 路由选择协议

![image-20230927002014422](C:\Users\Joker\AppData\Roaming\Typora\typora-user-images\image-20230927002014422.png)

### 4.5.2 ==内部网关协议RIP（掌握）== P148

路由信息协议RIP（Routing Information Protocol）

![image-20230927002228837](C:\Users\Joker\AppData\Roaming\Typora\typora-user-images\image-20230927002228837.png)

#### RIP协议的三个特点

![image-20230927002213913](C:\Users\Joker\AppData\Roaming\Typora\typora-user-images\image-20230927002213913.png)

- RIP协议特点之一：好消息传播得快，坏消息传播得慢
- RIP存在的一个问题：当网络出现故障时，要经过比较长的时间（数分钟）才能将此信息传送到所有的路由器

#### RIP协议的优缺点

![image-20231120233707929](C:\Users\Joker\AppData\Roaming\Typora\typora-user-images\image-20231120233707929.png)

### 4.5.5 ==路由器的构成== P164

路由器的主要作用：

- 连通不同的网络
- 选择信息传送的线路

#### 路由器的结构

典型路由器的结构：

![image-20231120234255731](C:\Users\Joker\AppData\Roaming\Typora\typora-user-images\image-20231120234255731.png)

路由器的两大组成部分：

- [路由选择]()部分：也叫做控制部分，其核心构件是路由选择处理机，其任务是：根据选定的路由选择协议构造路由表，同时经常或定期地和相邻路由器交换路由信息，不断更新和维护路由表
- [分组转发]()部分：由[输入端口]()、[输出端口]()和[交换结构]()三部分组成；交换结构又称交换组织，作用是根据转发表对分组进行处理

#### 交换结构：路由器的关键构件

常用的交换方法：

- 通过存储器
- 通过总线
- 通过纵横交换结构

![image-20231120235011997](C:\Users\Joker\AppData\Roaming\Typora\typora-user-images\image-20231120235011997.png)

## 4.8 ==虚拟专用网VPN和网络地址转换NAT== P180

### 4.8.1 虚拟专用网VPN

#### 本地地址与全球地址

![image-20231120235239509](C:\Users\Joker\AppData\Roaming\Typora\typora-user-images\image-20231120235239509.png)

#### 专用IP地址

![image-20231120235352148](C:\Users\Joker\AppData\Roaming\Typora\typora-user-images\image-20231120235352148.png)

==注== 专用IP地址只能在局域网内部使用，只能用作本地地址

#### 虚拟专用网VPN

利用公用的互联网作为本机构各专用网之间的通信载体，这样的专用网称为**虚拟专用网VPN**（Virtual Private Network）

- 用隧道技术实现虚拟专用网![image-20231121000010886](C:\Users\Joker\AppData\Roaming\Typora\typora-user-images\image-20231121000010886.png)

### 4.8.2 网络地址转换NAT（原理，和NAPT的区别）

网络地址转换NAT（Network Address Translation）：解决在专用网上使用专用地址的主机与互联网上主机的通信问题（无需加密）

![image-20231121000735119](C:\Users\Joker\AppData\Roaming\Typora\typora-user-images\image-20231121000735119.png)

![image-20231121000807144](C:\Users\Joker\AppData\Roaming\Typora\typora-user-images\image-20231121000807144.png)

- 网络地址转换的过程

![image-20231121000605660](C:\Users\Joker\AppData\Roaming\Typora\typora-user-images\image-20231121000605660.png)

#### 网络地址与端口号转换NAPT

使用端口号的NAT称为**网络地址与端口号转换NAPT**（Network Address and Port Translation）

常用的NAT转换表同时利用上了运输层的端口号，可以使多个拥有本地地址的主机，共用一个NAT路由器上的全球IP地址，因而可以同时和互联网上的不同主机进行通信。

# 第5章 传输层

## 5.1 运输层协议概述

运输层的重要功能：复用和分用

两种不同的运输协议：

- 面向连接的TCP
- 无连接的UDP

### 5.1.2 ==运输层的两个主要协议== P13

- 用户数据包协议UDP（User Datagram Protocol）

<img src="C:\Users\Joker\AppData\Roaming\Typora\typora-user-images\image-20231007113720395.png" alt="image-20231007113720395" style="zoom:67%;" />

- 传输控制协议TCP（Transmission Control Protocol）

<img src="C:\Users\Joker\AppData\Roaming\Typora\typora-user-images\image-20231007113700640.png" alt="image-20231007113700640" style="zoom:67%;" />

## 用户数据报协议UDP

### UDP的主要特点

<img src="C:\Users\Joker\AppData\Roaming\Typora\typora-user-images\image-20231007144636763.png" alt="image-20231007144636763" style="zoom:67%;" />

<img src="C:\Users\Joker\AppData\Roaming\Typora\typora-user-images\image-20231007144647549.png" alt="image-20231007144647549" style="zoom:67%;" />

### UDP的首部格式

<img src="C:\Users\Joker\AppData\Roaming\Typora\typora-user-images\image-20231007144913897.png" alt="image-20231007144913897" style="zoom:67%;" />

## 5.3 传输控制协议TCP概述

### 5.3.1 TCP最主要的特点

==TCP面向流的概念（理解）== P39

面向字节流：

- TCP中“流”指的是流入或流出进程的字节序列
- ”面向字节流“的含义：虽然应用程序与TCP的交互是一次一个数据块，但TCP把应用程序交下来的数据看成仅仅是[一串无结构的字节流]()

![image-20231121160818723](C:\Users\Joker\AppData\Roaming\Typora\typora-user-images\image-20231121160818723.png)

## 5.4 ==可靠传输的工作原理== P46

### 5.4.1 停止等待协议

停止等待协议：每发送完一个分组就**停止发送**，等待对方的**确认**，在收到确认后再发送下一个分组。

- 无差错情况
- 出现差错

保证接收方正确收到数据：超时重传

- 确认丢失和确认迟到
- 信道利用率

停止等待协议的优点是简单，缺点是信道利用率太低：

![image-20231121162557587](C:\Users\Joker\AppData\Roaming\Typora\typora-user-images\image-20231121162557587.png)

提高传输效率：流水线传输，发送方可连续发送多个分组，不必每发完一个分组就停顿下来等待对方的确认。

### 5.4.2 连续ARQ协议

TCP协议的精髓：滑动窗口协议

![image-20231121163006191](C:\Users\Joker\AppData\Roaming\Typora\typora-user-images\image-20231121163006191.png)

- 发送方的发送窗口：位于发送窗口内的分组可以连续发送出去，不需要等待对方的确认
- 累积确认：不必对收到的分组逐个发送确认，而是对按序到达的最后一个分组发送确认，表示到这个分组为止的所有分组都已正确收到
- Go-back-N（回退N）

## TCP报文段的首部格式

<img src="C:\Users\Joker\AppData\Roaming\Typora\typora-user-images\image-20231007150057559.png" alt="image-20231007150057559" style="zoom:80%;" />

## 5.6 TCP可靠传输的实现

### 5.6.1 以字节为单位的滑动窗口

### 5.6.2 ==超时重传==时间的选择 P98

TCP超时重传时间的设置：

- 一个报文段发出的时间和收到相应确认的时间，两个时间之差为**报文段的往返时间RTT**
- 加权平均往返时间$RTT_s$：$RTT_s$的初值为第一次测量到的$RTT$样本，此后按以下公式迭代==要会算==：

$$
新的RTT_s = (1 - \alpha) \times 旧的RTT_s + \alpha \times 新的RTT样本
$$

其中$0 \le \alpha \le 1$，若$\alpha$接近于0，则RTT值更新慢，反之更新较快。

RFC 2988推荐$\alpha = 0.125$

- 超时重传时间RTO（Retransmission Time-Out）：略大于$RTT_s$

### 5.6.3 选择确认ACK

## TCP的流量控制

![image-20231124105316218](C:\Users\Joker\AppData\Roaming\Typora\typora-user-images\image-20231124105316218.png)

## 5.8 ==TCP的拥塞控制== ==重要== P118

### 5.8.1 拥塞控制的一般原理

- 拥塞控制与流量控制的区别
- 开环控制与闭环控制

![image-20231121171906884](C:\Users\Joker\AppData\Roaming\Typora\typora-user-images\image-20231121171906884.png)

### 5.8.2 TCP的拥塞控制方法

![image-20231121172212101](C:\Users\Joker\AppData\Roaming\Typora\typora-user-images\image-20231121172212101.png)

TCP拥塞控制算法（4种）：

- 慢开始
- 拥塞避免
- 快重传
- 快恢复

#### ==图：慢开始和拥塞避免算法的实现举例（重点大题，会画）== P139

![image-20231121173915696](C:\Users\Joker\AppData\Roaming\Typora\typora-user-images\image-20231121173915696.png)

- TCP连接初始化时，拥塞窗口cwnd置为1，慢开始门限ssthresh初始值置为16，此时$cwnd < ssthresh$，执行[慢开始算法]()，拥塞窗口cwnd随传输轮次按[指数规律]()增长
- 点1：当拥塞窗口增长到慢开始门限值ssthresh时，改为执行[拥塞避免算法]()，此时拥塞窗口将按[线性规律]()增长
- 点2：当拥塞窗口$cwnd = 24$，网络出现超时，发送方判断为网络拥塞，调整门限值$ssthresh = cwnd/2 = 12$，设置拥塞窗口$cwnd = 1$，重新进入[慢开始阶段]()
- 点4：发送方一连收到3个对同一个报文段的重复确认，（3-ACK），此时发送方改为执行[快重传]()和[快恢复算法]()，调整门限值$ssthresh = cwnd/2 = 8$，设置拥塞窗口$cwnd = ssthresh = 8$，直接执行[拥塞避免算法]()

快重传算法：发送方一连收到三个对报文段M的重复确认，立即重传报文段M

快恢复算法：

![image-20231121180000729](C:\Users\Joker\AppData\Roaming\Typora\typora-user-images\image-20231121180000729.png)

#### ==TCP拥塞控制流程图（理解）== P157

![image-20231121173755561](C:\Users\Joker\AppData\Roaming\Typora\typora-user-images\image-20231121173755561.png)

### 5.8.3 主动队列管理AQM

#### ==全局同步== P161

![image-20231123171717948](C:\Users\Joker\AppData\Roaming\Typora\typora-user-images\image-20231123171717948.png)

#### ==随机早期检测RED（特点）== P164

随机早期检测RED（Random Early Detection）

![image-20231123172014821](C:\Users\Joker\AppData\Roaming\Typora\typora-user-images\image-20231123172014821.png)

## 5.9 TCP的运输连接管理

# 第6章 应用层

## 6.1 域名系统DNS

### 6.1.1 域名系统概述

域名系统DNS（Domain Name System）

### 6.1.2 互联网的域名结构

顶级域名TLD（Top Level Domain）：

- 国家顶级域名nTLD
- 通用顶级域名gTLD
- 基础结构域名（又称反向域名，只有一个：arpa）

互联网的域名空间：

![image-20231124120220369](C:\Users\Joker\AppData\Roaming\Typora\typora-user-images\image-20231124120220369.png)

### 6.1.3 ==域名服务器==

域名服务器：[域名 $\rightarrow$ IP地址]()

域名服务器的四种类型：
1. 根域名服务器
2. 顶级域名服务器
3. 权限域名服务器
4. 本地域名服务器

## 6.2 文件传送协议

文件传送协议FTP（File Transfer Protocol）

### 6.2.1 FTP概述

### 6.2.2 FTP的基本工作原理

#### FTP特点

![image-20231124114255606](C:\Users\Joker\AppData\Roaming\Typora\typora-user-images\image-20231124114255606.png)

#### FTP使用的两个TCP连接

![image-20231124114324456](C:\Users\Joker\AppData\Roaming\Typora\typora-user-images\image-20231124114324456.png)

![image-20231124114356881](C:\Users\Joker\AppData\Roaming\Typora\typora-user-images\image-20231124114356881.png)

### 6.2.3 简单文件传送协议TFTP

## 6.4 万维网WWW

### 6.4.1 万维网概述

#### 万维网需解决的问题

<img src="C:\Users\Joker\AppData\Roaming\Typora\typora-user-images\image-20231124115600125.png" alt="image-20231124115600125" style="zoom:67%;" />

<img src="C:\Users\Joker\AppData\Roaming\Typora\typora-user-images\image-20231124115626569.png" alt="image-20231124115626569" style="zoom:67%;" />

<img src="C:\Users\Joker\AppData\Roaming\Typora\typora-user-images\image-20231124115646183.png" alt="image-20231124115646183" style="zoom:67%;" />

<img src="C:\Users\Joker\AppData\Roaming\Typora\typora-user-images\image-20231124115657040.png" alt="image-20231124115657040" style="zoom:67%;" />

### 6.4.2 统一资源定位符URL

统一资源定位符URL（Uniform Resource Locator）

### 6.4.3 超文本传送协议HTTP

超文本传送协议HTTP（HyperText Transfer Protocol）

### 6.4.4 万维网的文档

#### ==动态万维网文档== P91

动态万维网文档：由应用程序[动态创建]()

<img src="C:\Users\Joker\AppData\Roaming\Typora\typora-user-images\image-20231123173018348.png" alt="image-20231123173018348" style="zoom:67%;" />

### 6.4.5 万维网的信息检索系统

- ==全文检索搜索引擎==

<img src="C:\Users\Joker\AppData\Roaming\Typora\typora-user-images\image-20231123173438969.png" alt="image-20231123173438969" style="zoom:67%;" />

- ==分类目录搜索引擎==

<img src="C:\Users\Joker\AppData\Roaming\Typora\typora-user-images\image-20231123173448960.png" alt="image-20231123173448960" style="zoom:67%;" />

- ==垂直搜索引擎==

<img src="C:\Users\Joker\AppData\Roaming\Typora\typora-user-images\image-20231123173458148.png" alt="image-20231123173458148" style="zoom:67%;" />

## 6.5 电子邮件

### 6.5.2 简单邮件传送协议SMTP（Simple Mail Transfer Protocol）

<img src="C:\Users\Joker\AppData\Roaming\Typora\typora-user-images\image-20231125114355285.png" alt="image-20231125114355285" style="zoom:67%;" />

### 6.5.4 邮件读取协议POP3和IMAP

## 6.6 动态主机配置协议DHCP

动态主机配置协议DHCP（Dynamic Host Configuration Protocol）

### ==DHCP协议的工作过程==

![image-20231123193913497](C:\Users\Joker\AppData\Roaming\Typora\typora-user-images\image-20231123193913497.png)

![image-20231123193950631](C:\Users\Joker\AppData\Roaming\Typora\typora-user-images\image-20231123193950631.png)

# 第9章 无线网络和移动网络

WiFi信号满格为什么网速慢？

1. 无线路由器的[信号频道过于拥挤]()，导致网络速度下降。这是因为许多设备都默认连接2.4GHz频段，如果该频段上的设备过多，就会导致通信质量下降。
2. 家里的各种电器设备、智能终端和金属制品都可能[对Wi-Fi信号产生干扰]()，从而影响网络质量。尽管信号强度可能仍然满格，但由于受到干扰，实际的网络速度可能会变慢。
3. [路由器本身的性能问题]()也可能是导致网速慢的原因。例如，路由器的网络处理能力不足或者配置不当，都可能导致网速降低。

## 9.1 无线局域网WLAN

### 9.1.1 无线局域网的组成

无线局域网WLAN（Wireless Local Area Network）分为两大类：

- ==有固定基础设施的WLAN==

有接入点AP（Access Point）、基站

- ==无固定基础设施的WLAN==

==注== 802.11，俗称wifi

### 9.1.3 802.11局域网的MAC层协议

#### ==CSMA/CA协议（原理）== P30

CSMA/CA（Collision Avoidance，碰撞避免）协议是CSMA/CD协议（载波监听多点接入/碰撞检测）的改进

<img src="C:\Users\Joker\AppData\Roaming\Typora\typora-user-images\image-20231123195217984.png" alt="image-20231123195217984" style="zoom:67%;" />

#### 二进制指数退避算法

$$
时隙_i = rand(0,\ 2^{2 + i} - 1)
$$

<img src="C:\Users\Joker\AppData\Roaming\Typora\typora-user-images\image-20231123195356849.png" alt="image-20231123195356849" style="zoom:67%;" />

## 9.2 无线个人区域网WPAN

无线个人区域网WPAN（Wireless Personal Area Network）

## 9.3 无线城域网WMAN

无线城域网WMAN（Wireless Metropolitan Area Network）

## 9.4 蜂窝移动通信网

## 9.5 两种不同无线上网

# 第10章 工业控制网络

## 工业自动控制系统简介

## 10.2 传统工业控制网络

三种现场总线 + CAN总线

- Modbus现场总线
- Profibus现场总线：工厂自动化
- DeviceNet现场总线
- CAN总线：汽车工业

### 10.2.1 传统工业控制网络简介

现场总线的定义：指安装在制造或过程区域的现场装置与控制室内的自动控制装置之间[数字式]()、[串行]()、[多点通信]()的数据总线。

### 10.2.2 Modbus现场总线

### 10.2.3 Profibus现场总线

<img src="C:\Users\Joker\AppData\Roaming\Typora\typora-user-images\image-20231123202208563.png" alt="image-20231123202208563" style="zoom:50%;" />

### 10.2.4 DeviceNet现场总线

### 10.2.5 CAN总线

## 工业以太网



















































