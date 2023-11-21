# 回顾

## 三角函数与反三角函数

![450](asset/Pasted%20image%2020231120202046.png)

> 解释一下 sec csc cot
> sec（secant）正割函数 --> 斜边比邻边
> csc（cosecant）余割函数 --> 斜边比对边
> cot（cotangent）余切函数 --> 邻边比对边

![550](asset/Pasted%20image%2020231120202236.png)

![](asset/Pasted%20image%2020231120204832.png)





# 1-极限与连续 ①

## 定义

极限是无限接近的结果，这个结果可能永远达不到，是理想状态。例如：
![](asset/Pasted%20image%2020231120215007.png)

![|400](asset/Pasted%20image%2020231120215245.png)
![|550](asset/Pasted%20image%2020231120215513.png)
![|500](asset/Pasted%20image%2020231120215620.png)
所以说，函数在一个点的极限值跟函数在该点的函数值之间无关（可能函数表达式不同、可能不存在）

![](asset/Pasted%20image%2020231120220059.png)

- 函数研究某点的极限函数跟在该点有没有定义没有关系，因为 x 取不到该点

[几何平均数 - 维基百科](https://www.wikiwand.com/zh-hans/%E5%87%A0%E4%BD%95%E5%B9%B3%E5%9D%87%E6%95%B0)

[算术-几何平均值不等式 - 维基百科](https://www.wikiwand.com/zh-hans/%E7%AE%97%E6%9C%AF-%E5%87%A0%E4%BD%95%E5%B9%B3%E5%9D%87%E5%80%BC%E4%B8%8D%E7%AD%89%E5%BC%8F)

[均值不等式\_百度百科](https://baike.baidu.com/item/%E5%9D%87%E5%80%BC%E4%B8%8D%E7%AD%89%E5%BC%8F/8046796)

![](asset/Pasted%20image%2020231121085318.png)

ξ 取值不同，δ 取值也会改变，它们是对应关系

[常用数学符号 markdown 语法](学习日报/Day/2023-11-21.md#常用数学符号%20markdown%20语法)

![](asset/Pasted%20image%2020231121091036.png)

![](asset/Pasted%20image%2020231121091231.png)

[指数函数 - 维基百科](https://www.wikiwand.com/zh-hans/%E6%8C%87%E6%95%B0%E5%87%BD%E6%95%B0)

> 指数函数的底数大于 1 和大于 0 小于 1 的底数，图像相反

![](asset/Pasted%20image%2020231121092311.png)
举个例子
![](asset/Pasted%20image%2020231121092606.png)

![](asset/Pasted%20image%2020231121092945.png)

![|450](asset/Pasted%20image%2020231121093204.png)

![|500](asset/Pasted%20image%2020231121093611.png) 因为没有影响

![](asset/Pasted%20image%2020231121093848.png)

[为什么要有邻域？](学习日报/Day/2023-11-21.md#为什么要有邻域？)

![](asset/Pasted%20image%2020231121095622.png)
无穷小是指当一个变量趋近于某个特定值时，与该值的差趋近于 0 的量

[0是无穷小吗？那负无穷是什么？](学习日报/Day/2023-11-21.md#0是无穷小吗？那负无穷是什么？)

Notes
1. 0 为与自变量趋向无关的无穷小
2. 函数型的无穷小，要根据 x 的趋向来判断![](asset/Pasted%20image%2020231121100539.png)
3. 无穷小不谈正负（这种情况下，谈论两个无穷小相减的情况就失去意义了）![](asset/Pasted%20image%2020231121101713.png)

## 性质

### (一) 基本性质

![](asset/Pasted%20image%2020231121102220.png)
![](asset/Pasted%20image%2020231121102628.png)
![](asset/Pasted%20image%2020231121103722.png)


![](asset/Pasted%20image%2020231121104234.png)
这里 ε 是任意取值的

![](asset/Pasted%20image%2020231121105146.png)

[极限与连续中怎么理解有介性](学习日报/Day/2023-11-21.md#极限与连续中怎么理解有介性)

### (二) 存在性质

准则 I（夹逼定理）

> 下面情况讲的是数列，不是函数

[$为什么2^n=(1+1)^n=C^0_n+C^1_n+C^2_n+...+C^n_n$](学习日报/Day/2023-11-21.md#为什么2%20n%201%201%20n%20C%200_n%20C%201_n%20C%202_n%20C%20n_n)

![](asset/Pasted%20image%2020231121112041.png)
![](asset/Pasted%20image%2020231121112243.png)
![](asset/Pasted%20image%2020231121112504.png)

![](asset/Pasted%20image%2020231121142612.png)
> 疑问：为什么 0＜x ≤1 时，选取 $x^n$ 做分析，而 x ＞1 时，选取 $x^{2n}$ 做分析，为什么不一起分析或选取相反着来分析 