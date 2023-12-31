## 01-概论

### 积分

讲述圆面积计算公式的由来

![](asset/Pasted%20image%2020231113150853.png)
![](asset/Pasted%20image%2020231113150901.png)
所以，选的 dr 越小，近似就越准确

思想：将圆切割成无限个同心圆，每一个同心圆如果摊开的话是一个梯形，我们近似为矩形，矩形长为 2πdr，宽为 dr，然后将每个矩形相加![](asset/Pasted%20image%2020231113151754.png)这里直线的函数为 2πr，然后选取越来越小的 dr![](asset/Pasted%20image%2020231113151901.png)那么各个矩形的和便相当于图像下的面积（==极限状态下没有误差==） 

---

其他不规则图形的求解呢？（采用近似法）

分割 --> 近似 --> 求和 --> 极限

![](asset/Pasted%20image%2020231113153926.png)

![](asset/Pasted%20image%2020231113154504.png)

### 导数

对任意函数通用

![](asset/Pasted%20image%2020231113155124.png)
或者严格来说，导数是当 dx 越来越小时这个比值趋向的值。粗略的讲 它衡量的是函数对取值的微小变化有多敏感

某个图像下方面积函数的导数，能够还原出定义这个图像的函数
![](asset/Pasted%20image%2020231113155929.png)
它将积分和导数这两个概念联系起来，并且表明，某种意义上，两者互为逆运算

## 02-导数的悖论

> 本节通过计算的方式来理解导数

![](asset/Pasted%20image%2020231113160815.png)

导数值相当于瞬时变化率（这里的瞬时并不是指某一个时间点，因为只有某一点是没有变化的作用的，这里是翻译的问题，所以瞬时应当指时刻（某一很短的时间间隔））

![](asset/Pasted%20image%2020231113161953.png)

![](asset/Pasted%20image%2020231113162251.png)
所以说，导数纯数学上真正的完全并不是沿图像两点间的斜率，而是经过图像上某一点的切线的斜率

尽管说“瞬时的变化”没有任何意义，但我们可以让 dt 非常非常的接近 0，这样可以让时间点的变化率变得有意义了，我们不用触及瞬时变化的矛盾就可以绕开它了，同时这个技巧还有一个直观的表现方法，即求函数图上过某一点的切线斜率；

==同时也别把求切线看成求什么“某一点瞬时的变化率”，而是要把它看做是求“某一点附近的变化率”的最佳近似==

![](asset/Pasted%20image%2020231113164018.png)

单纯解一个数学题，我们对函数 s(t) 求导 用的符号就写作 ds/dt 
![](asset/Pasted%20image%2020231113164230.png)
![](asset/Pasted%20image%2020231113164251.png)

dt 越小越容易求解，因为 dt 本身接近于 0，所以我们把带有 dt 的项都消除掉了（近似看成 0，忽略）
![](asset/Pasted%20image%2020231113164646.png)
然后这里我们把 2 替换成一般情况，替换为变量 t，便得到了求导公式
![](asset/Pasted%20image%2020231113164833.png)

![](asset/Pasted%20image%2020231113165014.png)
在实际求导操作中，你不用每次都这么推一遍，$t^3$ 的导函数是 $3t^2$  这是学了微积分后大家立刻就能反应过来的，不用每次都重头推导

没有运动，但有运动的趋势
![](asset/Pasted%20image%2020231113170854.png)

![](asset/Pasted%20image%2020231113170913.png)

![](asset/Pasted%20image%2020231113170949.png)
![](asset/Pasted%20image%2020231113171013.png)
**是指在第 0 秒附近车速的最佳近似 是匀速 0 米每秒**

变化不存在瞬时，导数是变化率的最佳近似（==导数测量的是“瞬时变化率” 这个说法是矛盾的，以后不要用==）

## 03-用几何来求导

> 本节通过几何的方式来理解导数

微小变化量才是导数的本质

![](asset/Pasted%20image%2020231114142218.png)
![](asset/Pasted%20image%2020231114142230.png)
对于微小的值来说，一个可靠的经验准则是你可以忽略掉任何包含多于一个 dx 的项（所以上图的 $dx^2$ 可以忽略）换言之一个微小变化量的平方就是一个小到可以忽略的变化量，而最终得到的结果就是 df 等于 dx 的多少多少倍

理论上，dx 趋近无穷小的时候，三个大面的面积趋向 100%，而至于棱条和小块(如图)
![](asset/Pasted%20image%2020231114142736.png)
![](asset/Pasted%20image%2020231114142938.png)
![](asset/Pasted%20image%2020231114143028.png)

幂函数求导公式：
![](asset/Pasted%20image%2020231114143139.png)

![](asset/Pasted%20image%2020231114143243.png)
![](asset/Pasted%20image%2020231114143809.png)

![](asset/Pasted%20image%2020231114151200.png)

下图中可得出 sinθ 的导数就是余弦函数
$$
dy/dx = d(sin(θ))/dθ
$$
![](asset/Pasted%20image%2020231114151329.png) ^xe9utj

![](asset/Pasted%20image%2020231114152603.png) 

> 解答一下：（首先θ可表示角度也可表示弧度（[上图中写弧长有勘误](学习日报/Day/2023-11-14.md#θ是不是可表示角度也可表示弧长？)））这里求圆的时候为什么是以θ来求斜率呢？dy/dx 为什么要变为的 d(sinθ)/dθ，因为疑惑 dx 不应该是 x 轴上的变化量吗，怎么是弧长的变化量?
> 
> 实际上，dx 中的 x 表示自变量，而这里函数是 d(sinθ)，自变量是θ（弧度），所以要用 d(sinθ)/dθ 不是用 x 轴长的变化量
> 
> 但话又说回来，dθ其实跟 dx（这里的 x 是 x 轴的变量）也是有直接关系的，x 轴上的变量移动（值改变）改变了 θ 的值


## 04-直观理解链式法则和乘积法则

加法法则：两个函数和的导数，就是它们导数的和
![](asset/Pasted%20image%2020231114160647.png)
![](asset/Pasted%20image%2020231114160852.png)

![](asset/Pasted%20image%2020231114161816.png)
一般情况下 df 表示 y 轴方向上的微小变化量，dx 表示 x 轴方向上的微小变化量（但也有其他情况，比如圆的求导 df 和 dθ（代表弧度）但实际上 dθ 也是 dx，只是需要将圆展开，取值范围在(0,2π)，不过通过可视化的圆来用坐标系表示的话，此时的 dx 不代表 dθ，只有展开成的坐标系时 dθ 才是 dx）

==有点被下图误导了，可视化的圆本不该画坐标系的，因为这里的 dθ 不等同于该坐标系的 dx，需要重新基于 dθ 画 dx，才能将 dθ 等同于 dx==
![微积分的本质--3Blue1Brown](微积分的本质--3Blue1Brown.md#^xe9utj)

乘积法则的理解，用图像并不是可视化的最佳方式，在不同层次的数学中，一个相当常见的做法是如果你要处理两个东西的乘积，通过面积来理解会有好处 [04-直观理解链式法则和乘积法则\_哔哩哔哩\_bilibili](https://www.bilibili.com/video/BV1ob411y7L9/?p=4&vd_source=1f9072e850dde202d6ddd4c60d9d334d) 04:45 有动画效果展示
![](asset/Pasted%20image%2020231114162839.png)
![](asset/Pasted%20image%2020231114195249.png)
![](asset/Pasted%20image%2020231114200200.png)==补充一下，这里 x 代表一个整体（原函数）看成 y==

![](asset/Pasted%20image%2020231114201004.png)
![](asset/Pasted%20image%2020231114201104.png)
口诀：左乘右导，右乘左导

口诀的动画演示见 [04-直观理解链式法则和乘积法则\_哔哩哔哩\_bilibili](https://www.bilibili.com/video/BV1ob411y7L9/?p=4&vd_source=1f9072e850dde202d6ddd4c60d9d334d) 08:10 处
![](asset/Pasted%20image%2020231114201237.png)
![](asset/Pasted%20image%2020231114202443.png)
常数本身不会虽自变量变化而变化，所以不会产生对应的增量


![](asset/Pasted%20image%2020231114202907.png)
这里我们换另一种可视化来研究

复合函数，里层函数的增量，传递到外层函数
![](asset/Pasted%20image%2020231114203818.png)

这里可以使用换元法将 $x^2$ 看成 h，那么 d(sin(h))=cos(h)dh，再带入 $x^2$
![](asset/Pasted%20image%2020231114204305.png)

这就是链式法则（复合函数的求解）
![](asset/Pasted%20image%2020231114204631.png)

从符号层面看，你往这个导数里代入的仍旧是内层函数

![](asset/Pasted%20image%2020231114204754.png)
层层嵌套求导

![](asset/Pasted%20image%2020231114204910.png)
它是我们试图求出的总量，但是我们可以对中间变量 h 求导
![](asset/Pasted%20image%2020231114204945.png)

![](asset/Pasted%20image%2020231114205224.png)
这是通过一连串事件得到的，dh 的消去并不只是符号上的技巧，而是真实地反映出了我们在求导数时，各种微小变化量发生了什么

![](asset/Pasted%20image%2020231114205404.png)
加法法则、乘法法则、链式法则，来处理简单函数组合出的函数的导数

> 小结：[04-直观理解链式法则和乘积法则\_哔哩哔哩\_bilibili](https://www.bilibili.com/video/BV1ob411y7L9/?p=4&vd_source=1f9072e850dde202d6ddd4c60d9d334d) 这期视频真的很赞，通过不同的动画讲解了三种法则的来源，同时理解和实操是两回事，在理解的基础上要加强实操（理论代替不了实操），做题做题再做题，练起来！

## 05-指数函数求导

下面例子中将增长率视为要增长到下一天数的数量趋势（补充：下图所说到的情况不完全正确，但至少我们考虑一整天内的变化时是这样的，包含小数点的可能不适用）
![](asset/Pasted%20image%2020231115143745.png) ^ee8u1m


一目了然的图说明指数函数
![](asset/Pasted%20image%2020231115144030.png)
![](asset/Pasted%20image%2020231115144111.png)

dt 取值越小，越趋近于某个常数
![](asset/Pasted%20image%2020231115144311.png)

[前情提要](微积分的本质--3Blue1Brown.md#^ee8u1m) ，显然的，此函数在小得多的时间段内的变化率
![](asset/Pasted%20image%2020231115144624.png)而比例就是这个怪怪的常数 0.6931

![](asset/Pasted%20image%2020231115145040.png)
这个性质并不是指数 2 独有的，更换底数的大小，也是趋向某一个常数，只不过值不同，同时还有下面的规律
![](asset/Pasted%20image%2020231115150614.png)

![](asset/Pasted%20image%2020231115150723.png) ![](asset/Pasted%20image%2020231115150815.png) ![](asset/Pasted%20image%2020231115151047.png) ![](asset/Pasted%20image%2020231115150858.png)
就好像在问为什么 π 正好是圆的周长比上它的直径一样![](asset/Pasted%20image%2020231115151151.png)因为这个数就是这么定义来的

所有的指数函数都和它们的导数成比例，但只有单单的一个 e，是那个使比例系数为 1 的特殊数字，也就意味着 $e^t$ 就等于它自身的导数

$e^t$ 的图像有以下特殊性质![](asset/Pasted%20image%2020231115151925.png)

$e^{某常数*t}$ 的导数就等于常数乘以函数本身 [数学语法-指数函数写法示例](学习日报/Day/2023-11-15.md#x%20的2t%20次方要怎么写)
![](asset/Pasted%20image%2020231115152752.png)因为这是复合函数的链式法则求解

![](asset/Pasted%20image%2020231115153056.png)![](asset/Pasted%20image%2020231115153102.png)

这里算 $2^t 可以先将 e^{ln(2)} 看成一个整体 h，算完 h 后再算 h^t$
![](asset/Pasted%20image%2020231115153358.png)
![](asset/Pasted%20image%2020231115153844.png)

ln(2)的值如下：
![|250](asset/Pasted%20image%2020231115154203.png)

amazing！常数 C 竟是底数的自然对数 C=ln(A) （原函数 $A^t 求导等于 ln^A*A^t$）
$同时 ln^e = 1$
![](asset/Pasted%20image%2020231115154348.png) ![](asset/Pasted%20image%2020231115154723.png) ![](asset/Pasted%20image%2020231115155029.png)
![](asset/Pasted%20image%2020231115155343.png)

将指数函数写成含有 e 的形式的好处是指数上的这个常数就有了一目了然的含义![](asset/Pasted%20image%2020231115155757.png)

此外 在凉爽的房间里放一杯热水，水变凉的速率就和水与房间的温差成正比，或者换个说法 温差的变化率就和温差本身成正比；再假设你拿钱做投资，那么金额的增长率就和任意时间点都金额成正比，在以上所有例子中，变化率都和数量本身成正比，因此该数量随时间的变化，看起来就会像指数函数。尽管指数函数有很多种写法
![](asset/Pasted%20image%2020231115160151.png)

> 小结：无论用于计算还是直观判断，指数函数的底数选择 e 都是最好的


## 06-隐函数求导是怎么回事

![](asset/Pasted%20image%2020231115162116.png)
![](asset/Pasted%20image%2020231115162132.png)因为函数的定义是一个输入对应唯一一个输出，圆的同一 x 取值可能有两个 y 值对应，所以圆曲线不是函数
![](asset/Pasted%20image%2020231115162157.png)
![](asset/Pasted%20image%2020231115163041.png)
![](asset/Pasted%20image%2020231115163323.png)
![](asset/Pasted%20image%2020231115163540.png)
![](asset/Pasted%20image%2020231115164219.png)
![](asset/Pasted%20image%2020231115164501.png)
![](asset/Pasted%20image%2020231115165350.png)
![](asset/Pasted%20image%2020231115171021.png)
![](asset/Pasted%20image%2020231115171047.png)
此时我们不管这个变化还会不会留在圆上，我们就在 xy 平面上往任意方向走了微小的一步，给 S 求导就是在问 “走这一步，S 的值变化了多少”
![](asset/Pasted%20image%2020231115171305.png)
![](asset/Pasted%20image%2020231115171440.png)
![](asset/Pasted%20image%2020231115171512.png)
它实际上表示你从（x，y）点开始，走了（dx，dy）这一小段距离之后，$x^2+y^2$ 的值相应变化了多少 [全微分是什么](学习日报/Day/2023-11-15.md#全微分)

求 ln(x) 的导数
![](asset/Pasted%20image%2020231115172617.png)

[隐函数求导的含义](学习日报/Day/2023-11-15.md#隐函数求导)


## 07-极限(含洛必达法则)

> 微积分需要连续，而连续需要无穷小，但是没人能探明无穷小的样子

![](asset/Pasted%20image%2020231116103713.png)

![](asset/Pasted%20image%2020231116143326.png)

![](asset/Pasted%20image%2020231116143846.png)
只不过右边式子解释了求 df 的含义![](asset/Pasted%20image%2020231116144143.png)
![](asset/Pasted%20image%2020231116144211.png)

这里其实 h 就是 dx
![](asset/Pasted%20image%2020231116144505.png)并记住 随时考虑 dx 逼近于零时的情况

用具体有限小的变化量来描述导数，其实跟上面导数的正式定义是等价的
我们讨论极限时 讨论的是当变量逼近于零的时候的影响，而非无穷小的变化量的影响 [将变量逼近于零是否等同无穷小](学习日报/Day/2023-11-16.md#将变量逼近于零是否等同无穷小)

![](asset/Pasted%20image%2020231116145530.png)

用示例理解极限（洛必达法则，0/0 的情况，将函数比值求极限转化为导数比值（二者是约等于的关系））使用该法则的唯一约束条件就是 它们在 x=a 点可导
![](asset/Pasted%20image%2020231116150637.png)
![](asset/Pasted%20image%2020231116150703.png)

![](asset/Pasted%20image%2020231116151118.png)
求极限的情况的话![](asset/Pasted%20image%2020231116151157.png)
![](asset/Pasted%20image%2020231116151342.png)
![](asset/Pasted%20image%2020231116151433.png)变化量 dx 取的越小，这个比值就越精确，所以这个比值就等于极限值的精确值

这就是洛必达法则
![](asset/Pasted%20image%2020231116151753.png)

![](asset/Pasted%20image%2020231116151930.png)


## 08-积分与微积分的基本定理

积分其实就是求导的逆运算

[“积分是导数的累积，等于原函数” 这句话对吗？](学习日报/Day/2023-11-16.md#“积分是导数的累积，等于原函数”%20这句话对吗？)

求原函数也可以叫求反导数

[08-积分与微积分的基本定理\_哔哩哔哩\_bilibili](https://www.bilibili.com/video/BV1ob411y7L9?p=8&vd_source=1f9072e850dde202d6ddd4c60d9d334d) 03:26 讲解了求积分的过程 很不错的动画，将恒定速度从大到小逐渐求极限

定积分和不定积分也很好理解，区别就是有没有在一个具体的取值范围内讨论

![](asset/Pasted%20image%2020231116154644.png)
它不止出现在我们每个相加的量里，还表示了每个步长之间的间距

![](asset/Pasted%20image%2020231116154852.png)
是因为我们现在所用的这个符号指的并不是具体的 dt 的加和，而是指在 dt 趋近于 0 的时候 加和趋近的值
![](asset/Pasted%20image%2020231116155040.png)

![](asset/Pasted%20image%2020231116155206.png)

![](asset/Pasted%20image%2020231116155911.png)

通过积分所求得的原函数，应该在其项后面增加一个常数项 C，因为常数的导数为 0，增长常数项对所求原函数的影响只有使得原函数图像上下移动而已![](asset/Pasted%20image%2020231116160654.png)

同时这里还有一个条件没用，它将最终决定我们使用哪一个原函数，那就是积分的下限![](asset/Pasted%20image%2020231116161445.png) ![](asset/Pasted%20image%2020231116161502.png)

[牛顿-莱布尼茨公式以及莱布尼茨公式的区别](学习日报/Day/2023-11-16.md#牛顿-莱布尼茨公式%20_百度百科%20https%20baike%20baidu%20com%20item%20E7%2089%209B%20E9%20A1%20BF-%20E8%208E%20B1%20E5%20B8%2083%20E5%20B0%20BC%20E8%208C%20A8%20E5%2085%20AC%20E5%20BC%208F%207451942)

![](asset/Pasted%20image%2020231116162720.png)

> 牛顿-莱布尼茨公式将不可能/棘手的问题化简为减法计算，求出原函数并计算终点和起点之间的差值得出问题的解，很妙。洛必达法则则通过求导数比值来反求原复杂的复合函数比值，其中利用了极限的思想，逼近于 0 来近似得到问题的解（dx 越小结果越精确），通过这样的方式求解 0/0 型的函数（函数比值的分子分母在某一点处的值都为 0，所以才间接求导数来求原函数的解），也很妙

![](asset/Pasted%20image%2020231116163712.png)
![](asset/Pasted%20image%2020231116163833.png)
![](asset/Pasted%20image%2020231116163922.png)
![](asset/Pasted%20image%2020231116163951.png)

## 09-面积与斜率有什么关系

![](asset/Pasted%20image%2020231116164213.png)
![](asset/Pasted%20image%2020231116164237.png)
![](asset/Pasted%20image%2020231116164355.png)
世界上种种周期现象都可以用正弦曲线来描述

![](asset/Pasted%20image%2020231116164601.png)

> 以往求平均值我们可能想到用有限个数来平均求值，但对于如下图分割成无限个小面积这种或无数多个数的问题求平均值，我们可以用积分来求解
> 
> [积分和微分是什么，有什么区别？](学习日报/Day/2023-11-16.md#积分和微分是什么，有什么区别？)

![](asset/Pasted%20image%2020231116165258.png)
![](asset/Pasted%20image%2020231116165315.png)
这意味着把形如 sin(x) * dx 的项加了起来，对应着不同 x 的值，于是分子看上去就是积分的表达式，随着取的点的数量增加，求出的平均值就越来越接近 sin(x) 从 0 到 π 的积分除以区间的长度π

> 补充：$cos'(x) = -sin(x)$

![](asset/Pasted%20image%2020231116172436.png)


请注意 求平均值 2/π 归结到底就是![](asset/Pasted%20image%2020231117143256.png)这里求的就是斜率

另一种思考方式是将这个分式看做![](asset/Pasted%20image%2020231117143446.png)
那么，这里还有一个问题，为什么这个斜率代表 sin(x) 在 0 到 π 之间的平均值？

> 因为 sin(x) 是-cos(x) 上的斜率，它给出了 -cos(x) 在每个点上的斜率，所以 sin(x) 的平均值就是原函数从 x=0 到 x=π 所有切线斜率的平均值

![](asset/Pasted%20image%2020231117144439.png)
![](asset/Pasted%20image%2020231117144622.png)
![](asset/Pasted%20image%2020231117144631.png)
![](asset/Pasted%20image%2020231117144752.png)
但这恰好对应了取越来越多的点，近似出越来越准确的平均值

计算任意函数 f(x) 的积分 归根结底就是寻找 f(x) 的原函数 一般用 F(x) 表示
![](asset/Pasted%20image%2020231117145047.png)

> 所以，函数平均值问题的求解方法就是：用新的函数从 a 到 b 的高度变化，除以 a 到 b 的长度。换句话说，也就是原函数在这个区间起点和终点连线的斜率

使用积分的情况：
1. 当你觉得手上的问题，可以通过细分然后再相加的方式估算的话，那么试一试积分
2. 求有限数的平均值，然后你想要把这个想法推广到连续变量 也就是无限个数量中的话，可以试试用积分来描述这个问题![](asset/Pasted%20image%2020231117145839.png)

### 09脚注-高阶导数

![](asset/Pasted%20image%2020231117150117.png)

[急动度跟加速度的关系](学习日报/Day/2023-11-17.md#急动度跟加速度的关系)

下图这么写，只是一个记法而不是做计算，容易看出对函数进行几次微分
![](asset/Pasted%20image%2020231117151126.png)

![](asset/Pasted%20image%2020231117151334.png)

![](asset/Pasted%20image%2020231117151505.png) ![](asset/Pasted%20image%2020231117151527.png)

![](asset/Pasted%20image%2020231117151651.png)
![](asset/Pasted%20image%2020231117152303.png)

> 高阶导数最大的作用就是帮助我们得到函数的近似

<br />

## 10-泰勒级数

> 泰勒级数是数学中极其强大的函数近似工具

物理单摆球模型运用泰勒级数近似替换
![](asset/Pasted%20image%2020231117153027.png)
![](asset/Pasted%20image%2020231117153218.png)
各种缘由就在于 多项式可比别的函数要友好得多，它又好计算 又好求导 还好积分

泰勒级数通过多次求导来确定系数 [10-泰勒级数\_哔哩哔哩\_bilibili](https://www.bilibili.com/video/BV1ob411y7L9?p=11&vd_source=1f9072e850dde202d6ddd4c60d9d334d)  `03:10-05:21` 通过实际例子演示泰勒级数的动画做的很好
![](asset/Pasted%20image%2020231117153841.png)
![](asset/Pasted%20image%2020231117154226.png)
![](asset/Pasted%20image%2020231117154602.png)
![](asset/Pasted%20image%2020231117154614.png)
![](asset/Pasted%20image%2020231117154715.png)
这样一来，利用这 3 个给定的系数，当 x 的取值在 0 附近增减时，你近似函数值的变化率和近似变化率的变化率 就可以尽可能地接近函数 cos(x) 自身

![](asset/Pasted%20image%2020231117155001.png)
![](asset/Pasted%20image%2020231117155041.png)
换句话说，$1-\frac{1}{2x^2}$ 不仅仅是 cos(x) 在 x=0 处的最佳的二次近似函数，同时也是最佳的三次近似函数（[用markdown的代码块书写数学分式的语法](学习日报/Day/2023-11-17.md#用%20markdown%20的代码块书写数学分式的语法)）

![](asset/Pasted%20image%2020231117160320.png)从上图可以看出，但函数越高阶时，给定范围内求得的函数图像越接近我们要近似的目标图像（比只有最高阶 $x^2$ 时的函数跟接近目标函数）

![](asset/Pasted%20image%2020231117160909.png)
![](asset/Pasted%20image%2020231117161213.png)
![](asset/Pasted%20image%2020231117161345.png)

![](asset/Pasted%20image%2020231117161445.png)
![](asset/Pasted%20image%2020231117161459.png)
这对于任何点都是通用的，虽然这么一来式子变复杂了许多，但我们做的无非是让 π 点变得像之前的 0 点一样![](asset/Pasted%20image%2020231117161751.png)

![](asset/Pasted%20image%2020231117162100.png) ![](asset/Pasted%20image%2020231117162115.png)

这里的 f(x) 指的是要近似的目标函数
![](asset/Pasted%20image%2020231117162247.png)每一项要除以该项对应的阶乘，是因为求导造成系数增大对应阶乘倍，要把这个影响消除，就要除以该项对应的阶乘

![](asset/Pasted%20image%2020231117162514.png)

可以看看写法有什么差别
![](asset/Pasted%20image%2020231117162836.png)

下面以 $e^x$ 举例
![](asset/Pasted%20image%2020231117163003.png)

**下面用几何来解释泰勒级数的二次项**
![](asset/Pasted%20image%2020231117163454.png)

下面两张图的内容可以琢磨一下，看一下能懂了（忘了就重新回来看）
![](asset/Pasted%20image%2020231117163837.png)
![](asset/Pasted%20image%2020231117163846.png)
![](asset/Pasted%20image%2020231117164214.png)

![](asset/Pasted%20image%2020231117164443.png)

![](asset/Pasted%20image%2020231117164533.png)在数学中我们将无限多项的和叫做级数
![](asset/Pasted%20image%2020231117164537.png)
这里要小心对待所谓的无穷级数，因为累加“无限多”的项其实并没有意义

但如果一个级数加的越多，它的和越接近某个确定的数值的话，我们就可以说这个级数“收敛”到那个值

$e^x$ 是一个例外
![](asset/Pasted%20image%2020231117165051.png)

级数收敛到某个数，也可以叫等于

sin、cos 之类的一些重要函数等价于其泰勒级数，但有的函数 用某一取值的导数所构建的级数，只能在附近的范围内收敛

![](asset/Pasted%20image%2020231117165448.png)
![](asset/Pasted%20image%2020231117165457.png)
![](asset/Pasted%20image%2020231117165520.png)
![](asset/Pasted%20image%2020231117165533.png)
![](asset/Pasted%20image%2020231117165542.png)
![](asset/Pasted%20image%2020231117165554.png)
![](asset/Pasted%20image%2020231117165610.png)
![](asset/Pasted%20image%2020231117165620.png)
![](asset/Pasted%20image%2020231117165630.png)
![](asset/Pasted%20image%2020231117165643.png)
某种意义上讲 我们在 x=1 取得的导数信息并不能拓展到更广的取值范围 像这种累加更多的项 和并不能逼近一个值的级数 我们说它是“发散”的
![](asset/Pasted%20image%2020231117165857.png)

![](asset/Pasted%20image%2020231117165929.png)能够让多项式的和收敛的最大取值范围![](asset/Pasted%20image%2020231117170003.png)

![](asset/Pasted%20image%2020231117170038.png)
![](asset/Pasted%20image%2020231117170101.png)

> 小结：![](asset/Pasted%20image%2020231117170504.png)


## 11-你在微积分课上学不到的知识

请大家先别把“导数是斜率”当成是导数的定义，而是把导数看作反映函数对于输入值微小变化的敏感程度，而斜率只是用图像来分析函数时这种敏感度的体现而已
![](asset/Pasted%20image%2020231117171203.png)

还有一种看待导数的方法 基本想法是把这个函数看作 把输入数轴上所有的点 映射到另一条对应的输出数轴上![](asset/Pasted%20image%2020231117171358.png)从这个角度看 导数衡量的就是![](asset/Pasted%20image%2020231117171449.png)

![](asset/Pasted%20image%2020231117171602.png)所以我们说 $x^2$ 在 x=1 处的导数就等于 2

![](asset/Pasted%20image%2020231117172053.png)
![](asset/Pasted%20image%2020231117172103.png)
我们又注意到原式里就包含它本身![](asset/Pasted%20image%2020231117172139.png)

![](asset/Pasted%20image%2020231117172239.png)
看到弹幕有人说递归思想，但想了一下可能只是类似，因为递归有一个最小出口，跳出递归条件，这里可能没有![](asset/Pasted%20image%2020231117172404.png)
![](asset/Pasted%20image%2020231117172415.png)
![](asset/Pasted%20image%2020231117172435.png)
这另一个点我喜欢叫是 φ 的小弟，因为 φ 有的性质 它基本都有

![](asset/Pasted%20image%2020231119142257.png)

初始代入负值的话
![](asset/Pasted%20image%2020231119142426.png)

![](asset/Pasted%20image%2020231119140803.png)

![](asset/Pasted%20image%2020231119144559.png)

![](asset/Pasted%20image%2020231119144658.png)

具体图像解释 见 [11-你在微积分课上学不到的知识\_哔哩哔哩\_bilibili](https://www.bilibili.com/video/BV1ob411y7L9?p=12&vd_source=1f9072e850dde202d6ddd4c60d9d334d) 09:00

![](asset/Pasted%20image%2020231119145408.png)

![](asset/Pasted%20image%2020231119145523.png)

![](asset/Pasted%20image%2020231119145555.png)

我们在 φ 附近放大可以发现![](asset/Pasted%20image%2020231119145715.png)

实际的导数为 -0.38![](asset/Pasted%20image%2020231119145740.png) ![](asset/Pasted%20image%2020231119145813.png)

而 1/φ 附近的点放大看![](asset/Pasted%20image%2020231119145859.png)所以不动点附近的点回来离它越来越远，计算一下你还能发现每次拉伸的倍数比 2 还要大，顺便一提，由于导数为负，这些点还会正负反转 不过导数的绝对值才是映射是否稳定的决定因素

![](asset/Pasted%20image%2020231119150137.png)
![](asset/Pasted%20image%2020231119150147.png)
所谓稳定就是即时你动那么一小下，它也会趋于回到原处 而非远离

![](asset/Pasted%20image%2020231119150315.png)
是由此时导数的绝对值是否大于 1 所决定的

![](asset/Pasted%20image%2020231119150430.png)
按照取极限的情况来说
![](asset/Pasted%20image%2020231119150617.png)

![](asset/Pasted%20image%2020231119150713.png)
![](asset/Pasted%20image%2020231119150718.png)

> 最后一期的视频为之后学习大学数学的新知识打开了思考的思路，很不错！






