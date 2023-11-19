## 课堂随笔

- 向量相加可能是向量能移动远离原点的计算了
- 数字在线性代数中最常用的就是缩放向量，数字跟标量相差无异
- 向量位置叫为分量
- 线性代数紧紧围绕向量加法和向量数乘
- 当你考虑一个向量时，就把他看成箭头；当你考虑多个向量时，就把他们看出点
- ![](asset/Pasted%20image%2020231103165726.png)
- 取值范围看目标向量是否会影响其他向量所形成的张成空间，不影响则是线性相关，反之给张成空间增加了新的维度则称为线性无关![](asset/Pasted%20image%2020231103165706.png)
- ![](asset/Pasted%20image%2020231103170043.png)
- 变换类似于函数，接收（向量）输入，输出（向量）结果，它是运动的状态！
- 保持直线且原点位置不变便是下面的说法![](asset/Pasted%20image%2020231103222405.png)
- ![](asset/Pasted%20image%2020231103230759.png)
- ![](asset/Pasted%20image%2020231103231210.png)
- ![](asset/Pasted%20image%2020231103225803.png)
- ![](asset/Pasted%20image%2020231103231302.png)
- ![](asset/Pasted%20image%2020231103231351.png)
- ![](asset/Pasted%20image%2020231103231402.png)
- ![](asset/Pasted%20image%2020231103231915.png)也就是这两个线性相关向量所张成的一维空间
- 矩阵向量乘法就是计算线性变换作用于给定向量的一种途径
- 重要的一点：每当你看到一个矩阵时，你都可以把它解读为对空间的一种特定变换
- 左乘行变换，右乘列变换![](asset/Pasted%20image%2020231108145539.png)
- ![](asset/Pasted%20image%2020231108151156.png)
- 如何计算矩阵请参考视频 [04-矩阵乘法与线性变换复合的联系\_哔哩哔哩\_bilibili](https://www.bilibili.com/video/BV1ib411t7YR?p=5&spm_id_from=pageDriver&vd_source=1f9072e850dde202d6ddd4c60d9d334d) 05:40 处
- ![](asset/Pasted%20image%2020231108151900.png)
- 矩阵相乘的顺序不能变，不然会有影响（先剪切后旋转和先旋转后剪切的效应是不同的 在这里）![](asset/Pasted%20image%2020231108152037.png)
- 线代很多证明或思考使用变换相继的作用（想象空间变换）来进行比单纯符号证明会更有感悟
- 三维计算跟二维类似
- ![](asset/Pasted%20image%2020231108162935.png)
- 行列式 det 的值可以是负数，负数代表的含义是空间翻转，例如一张纸的正反面，反转后正面变成反面，反面变成正面。对应 i 帽和 j 帽的话，最开始 j 帽处于 i 帽的左边，如果进行了翻转，那么此时 j 帽便处于 i 帽的右边，det 的绝对值仍然代表缩放比例
- 行列式为 0，说明 i 帽和 j 帽处于一条直线或一个点
- 对于二维的行列式是面积缩放，对于三维的行列式则是体积的缩放（这里如果行列式为 0，那么可以压缩为一个平面或一条直线甚至一个点）![](asset/Pasted%20image%2020231108164046.png)
- 右手定则，变换后如果还能满足右手定则，则没有发生定向（翻转的意思）改变，反则变换后不满足右手只满足左手定则，则行列式为负，发生定向![](asset/Pasted%20image%2020231108164645.png)
- ![](asset/Pasted%20image%2020231108164757.png)
- [05-行列式\_哔哩哔哩\_bilibili](https://www.bilibili.com/video/BV1ib411t7YR?p=7&spm_id_from=pageDriver&vd_source=1f9072e850dde202d6ddd4c60d9d334d) 08:20 时间处演示了行列式计算的由来![](asset/Pasted%20image%2020231108165033.png)
- ![](asset/Pasted%20image%2020231109092137.png)
- ![](asset/Pasted%20image%2020231109093253.png)
- 所以更精确的秩的定义是列空间的维数![](asset/Pasted%20image%2020231109094522.png)
	- 满秩（Full rank）：当秩达到最大值时，意味着秩与列数相等
	- 零向量一定会被包含在列空间中，因为线性变换必须保持原点位置不变
	- 如果某矩阵线性变换后维度被压缩，则说明至少有某一方向上的向量（或者某一平面的向量）在线性变换后被压缩到原点变成零向量
- ![](asset/Pasted%20image%2020231109095753.png)
- 此时仍然为满秩，因为输出空间向量维数和输入向量维数相同![](asset/Pasted%20image%2020231109100915.png)因为矩阵有两列表面输入空间有两个基向量，有三行表明每一个基向量变换后都用三个独立的坐标来描述
- 下面矩阵代表这是一个从三维空间到二维空间的变换![](asset/Pasted%20image%2020231109102756.png) ![](asset/Pasted%20image%2020231109102925.png)
- ![](asset/Pasted%20image%2020231109103125.png)

> 考虑到后续章节可能难度上升，因此添加章节目录

### 07-点积与对偶性

![](asset/Pasted%20image%2020231109104416.png)
![](asset/Pasted%20image%2020231109151635.png)
解释点积，点积与顺序无关，无论哪个向量的投影乘另一个向量，结果都相同
![](asset/Pasted%20image%2020231109104602.png)
![](asset/Pasted%20image%2020231109105228.png)
若投影向量方向相反，则点积为负
![](asset/Pasted%20image%2020231109104652.png)
点积为 0 的情况
![](asset/Pasted%20image%2020231109104724.png) ^y3aq37

 [下面介绍为什么点积与顺序无关](线性代数的本质--3Blue1Brown.md#^y3aq37)

![](asset/Pasted%20image%2020231109144317.png)
当 w 和 v 向量长度相等时，无论谁的向量投影，结果很明显都相同，而当这种对称性被破坏时，例如上图的 v 向量长度增加至原来的两倍，用 w 做投影，那么则变为 2vw，因为 w 在 v 上的投影没变；如果用 v 做投影，那么 v 在 w 上的投影变为原来的二倍长度，而 w 没变，所以结果还是 2vw。总结就是对称性被破坏也不影响点积的最终值

**为什么点积的运算过程（对应坐标相乘并将结果相加），和投影有所联系？（难点）**

> 对偶性，详细动画讲解见：[07-点积与对偶性\_哔哩哔哩\_bilibili](https://www.bilibili.com/video/BV1ib411t7YR?p=10&spm_id_from=pageDriver&vd_source=1f9072e850dde202d6ddd4c60d9d334d) 05:00

多维空间线性变换压缩至一维空间，如果等距分布的点并未保持等距分布，则是非线性的，同时这些变换完全由 i 帽和 j 帽决定![](asset/Pasted%20image%2020231109152938.png)

![](asset/Pasted%20image%2020231109153141.png)

![](asset/Pasted%20image%2020231109160035.png)

OK，想到了一个很关键的问题，投影矩阵投影到一维空间中，仅用一个数即可表示
![](asset/Pasted%20image%2020231109160612.png)

![](asset/Pasted%20image%2020231109160727.png)

![](asset/Pasted%20image%2020231109160818.png)
![](asset/Pasted%20image%2020231109160847.png)
![](asset/Pasted%20image%2020231109161103.png)
![](asset/Pasted%20image%2020231109161324.png)
![](asset/Pasted%20image%2020231109161443.png)
![](asset/Pasted%20image%2020231109163352.png)

- 一个向量的对偶是它定义的线性变换
- 一个多维空间到一维空间的线性变换的对偶是多维空间中的某个特定向量
- 两个向量点乘，就是将其中一个向量转化为线性变换![](asset/Pasted%20image%2020231109163531.png)
- 不把向量看作是箭头，而看作是线性变换的物质载体，会更容易理解向量，向量彷佛是一个特定变换的概念性记号

**总结**：表面上，点积是理解投影的有利工具，并且方便检验两个向量的指向是否相同

#### 点积的意义

![](asset/Pasted%20image%2020231109170542.png)

### 08-01 叉积的标准介绍

先简单了解一下叉积

![](asset/Pasted%20image%2020231109164715.png)
![](asset/Pasted%20image%2020231109164826.png)
![](asset/Pasted%20image%2020231109164832.png)
也就是说顺序对叉积有影响
![](asset/Pasted%20image%2020231109164925.png)
实际上，基向量的顺序也就是定向的基础

复习一下：行列式即基于基向量面积缩放比例系数
![](asset/Pasted%20image%2020231109165530.png)
![](asset/Pasted%20image%2020231109165803.png)

叉积的规律![](asset/Pasted%20image%2020231109171008.png)

以上对叉积的描述并不算真正的叉积，真正的叉积描述如下：
![](asset/Pasted%20image%2020231109171102.png)
所以叉积的结果不是一个数，而是一个向量，向量的长度大小才是这个数

![](asset/Pasted%20image%2020231109171549.png)
![](asset/Pasted%20image%2020231109171828.png)
公式记忆：
![](asset/Pasted%20image%2020231109171911.png)

**这里让向量作为矩阵元是什么意思？**（符号上计算的技巧，但更重要的是对偶性，下一节将详细讲解）
![](asset/Pasted%20image%2020231109172020.png)
![](asset/Pasted%20image%2020231109172217.png)

### 08-02-以线性变换的眼光看叉积

![](asset/Pasted%20image%2020231110092143.png)
![](asset/Pasted%20image%2020231110092206.png)

<br />

![](asset/Pasted%20image%2020231110092852.png)是将这个向量投影到垂直于 v 和 w 的直线上，然后将投影长度与 v 和 w 张成的平行四边形的面积相乘![](asset/Pasted%20image%2020231110093115.png) ![](asset/Pasted%20image%2020231110093149.png) ![](asset/Pasted%20image%2020231110093729.png) ![](asset/Pasted%20image%2020231110093813.png)

### 09-基变换

基向量始终都是（1，0）和（0，1），相对于你自己的坐标系（坐标轴方向和网格间距可能有所不同）而言，同时所有基向量都拥有同一个原点（0，0），基向量 1 可能在基向量 2 的坐标描述会有所不同
![](asset/Pasted%20image%2020231110145041.png)
![](asset/Pasted%20image%2020231110145657.png)

---

**难点**：下图的抽象理论不太理解了（==懂了==）
补充：
- 任何一个新基的描述都需要借助一个基本基
- 矩阵看出汇率，向量看出欧元和人民币，进行换算
- 用我们的坐标系语言去模拟 Jennifer 的坐标系语言基向量
![](asset/Pasted%20image%2020231110152345.png)
![](asset/Pasted%20image%2020231110150800.png) ![](asset/Pasted%20image%2020231110150816.png)

---

基变换矩阵这一部分精彩 [09-基变换\_哔哩哔哩\_bilibili](https://www.bilibili.com/video/BV1ib411t7YR?p=13&spm_id_from=pageDriver&vd_source=1f9072e850dde202d6ddd4c60d9d334d) 11:00 时间处
![](asset/Pasted%20image%2020231110155301.png)
![](asset/Pasted%20image%2020231110155406.png)
![](asset/Pasted%20image%2020231110155503.png)
首先应用基变换，然后应用线性变换，最后应用基变换的逆，得到 Jennifer 描述的语言的向量
![](asset/Pasted%20image%2020231110155556.png)它接受用 Jennifer 语言描述的向量，并输出 Jennifer 语言描述的变换后的向量

![](asset/Pasted%20image%2020231110155927.png)结果就是在她的坐标系中描述的该向量旋转 90° 的结果

![](asset/Pasted%20image%2020231110160045.png)中间的矩阵代表一种你所见的变换，而外侧两个矩阵代表着转移作用，也就是视角上的转化，矩阵乘积仍然代表着同一种变换，只不过从其他人的视角来看

### 10-特征向量与特征值

![](asset/Pasted%20image%2020231110160719.png)
![](asset/Pasted%20image%2020231110161038.png)
![](asset/Pasted%20image%2020231110161259.png)
![](asset/Pasted%20image%2020231110161455.png)
特征值：即衡量特征向量在变换中拉伸或压缩比例的因子

特征向量的话是线性变换后不离开其张成空间位置的向量，只在原方向伸缩
举个例子：一个立方体旋转 30°，那么旋转轴就相当于特征向量，因为只有它旋转后没离开它所在的张成空间

求解 A 的特征向量和特征值
![](asset/Pasted%20image%2020231110162922.png)
![](asset/Pasted%20image%2020231110163116.png)
![](asset/Pasted%20image%2020231110163245.png)
![](asset/Pasted%20image%2020231110163555.png)
![](asset/Pasted%20image%2020231110163621.png)

![](asset/Pasted%20image%2020231110163828.png)
![](asset/Pasted%20image%2020231110163843.png)
![](asset/Pasted%20image%2020231110163934.png)
动画解析请见 [10-特征向量与特征值\_哔哩哔哩\_bilibili](https://www.bilibili.com/video/BV1ib411t7YR/?p=14&spm_id_from=pageDriver&vd_source=1f9072e850dde202d6ddd4c60d9d334d) 08:00 处

![](asset/Pasted%20image%2020231110164211.png)
![](asset/Pasted%20image%2020231110164705.png)
![](asset/Pasted%20image%2020231110164745.png)

![](asset/Pasted%20image%2020231110165257.png)
![](asset/Pasted%20image%2020231110165302.png)

特征基➡如果基向量都是特征向量

对角矩阵的幂运算比非对角矩阵的幂运算要方便快速很多，所以一般非对焦矩阵都是化成对角矩阵进行计算为宜

用特征基的好处：
![](asset/Pasted%20image%2020231110170822.png)这是因为它所处的坐标系的基向量在变换中只进行了缩放

> 所以说，如果你要计算这个矩阵的 100 次幂，一种更容易的做法是先变换到特征基，在那个坐标系中计算 100 次幂，然后再转换回标准坐标系

![](asset/Pasted%20image%2020231110171209.png)
比如说剪切变换，它的特征向量不够多，并不能张成全空间，但是如果你能找到一组特征基，矩阵运算就会变得非常轻松

### 11-抽象向量空间

![](asset/Pasted%20image%2020231110172153.png)

![](asset/Pasted%20image%2020231111094807.png)

线性组合的线性变换 == 线性变换的线性组合
线性变换保持向量加法运算和数乘运算

![](asset/Pasted%20image%2020231111095201.png)
![](asset/Pasted%20image%2020231111095346.png)
![](asset/Pasted%20image%2020231111095447.png)

[11-抽象向量空间\_哔哩哔哩\_bilibili](https://www.bilibili.com/video/BV1ib411t7YR/?p=15&vd_source=1f9072e850dde202d6ddd4c60d9d334d) 09:00后是通过例子来求函数矩阵的解的过程，可以看看
![](asset/Pasted%20image%2020231111100045.png)

![](asset/Pasted%20image%2020231111100216.png)

矩阵向量乘法和求导是一家人
![](asset/Pasted%20image%2020231111100517.png)

![](asset/Pasted%20image%2020231111100621.png)

只要你处理的对象集具有合理的数乘和相加概念，不管是空间中的箭头、一组数、函数的集合
![](asset/Pasted%20image%2020231111100811.png)
线性代数中所有关于向量、线性变换和其他的概念都应该适用于它

![](asset/Pasted%20image%2020231111100925.png)

![](asset/Pasted%20image%2020231111101338.png)这些规则被称为公理（Axioms）

![](asset/Pasted%20image%2020231111101543.png)

![](asset/Pasted%20image%2020231111101825.png)

![](asset/Pasted%20image%2020231111102021.png)

它可以是任何东西
![](asset/Pasted%20image%2020231111102045.png)

![](asset/Pasted%20image%2020231111102204.png)

### 12-克莱姆法则，几何解释

没听懂

[2023-11-11#克莱姆法则](学习日报/Day/2023-11-11.md#克莱姆法则)