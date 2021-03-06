---
layout: post
date:   2019-04-15 14:31:00
title:  "Functions And Limits"
categories: advanced mathematics
tags:  function limit 函数 极限
mathjax: true
---

* content
{:toc}
函数与极限 - Functions And Limits






---------
# 目录
- 第一章 [函数与极限](https://superzhangx.github.io/2019/04/15/AdvancedMathematics-FunctionsAndLimits/)
	- 第一节 映射与函数
	- 第二节 数列的极限
	- 第三节 函数的极限
	- 第四节 无穷大与无穷小
	- 第五节 极限运算法则
	- 第六节 极限存在的准则(俩个重要的极限)
	- 第七节 无穷小的比较
	- 第八节 函数的连续性与间断点
	- 第九节 连续函数的运算与初等函数的连续性
	- 第十节 闭区间上连续函数的性质
- 第二章 导数与微分
  - 第一节 导数的概念
  - 第二节 导数的求导法则
  - 第三节 高阶导数
  - 第四节 隐函数及由参数方程所确定的函数的导数-相关变化率
  - 第五节 函数的微分
- 第三章 微分中值定理与倒数的应用
- 第四章 不定积分
- 第五章 定积分
- 第六章 定积分的应用
- 第七章 微分方程

--------

# 1.1. 映射与函数

映射是现代数学中一个基本概念，而**函数是微积分的研究对象**，也是映射的一种。

## 1.1.1. 映射

### 1.1.1.1. 映射的概念

*设X、Y是俩个非空集合，如果存在一个**法则f** ，使得对X中的每个元素 x，按照法则 f，在Y中有唯一确定的元素y与之对应，那么**称f为从 X到 Y的映射**，记作：*

$$f:X \rightarrow Y$$

*其中 y 称为元素 x(在映射 f 下)的像，记作：*

$$ y = f(x) $$

*而元素 x 称为元素 y（在映射 f 下）的一个原像；集合X称为映射f的定义域，$记作 D_{f}$,$D_{f}=X$;X中的所有元素的像所组成的集合称为映射f的值域，$记作R_{f}或f(X)$,即*

$$R_{f} = f(X) = \{f(x) | x \in{X}\}$$

**注意**
* 构成一个映射必须具备以下三个要素：集合X，$即定义域D_{f}=X$;集合Y，即值域的范围：$R_{f} \subset Y$;对应法则f，$使对每个x \in X$,$有唯一确定的y=(x)与之对应$。
* $对每个x \in X$,元素x的像y是唯一的；$而对每个y \in R_{f}$,$元素y的原像不一定是唯一的$;$映射f的值域R_{f}是Y的一个子集$，$即R_{f} \subset Y$,$不一定R_{f}=Y$。

**映射的类型**
* **映射或满射** 设$f$是从集合X到集合Y上的映射，$若R_{f}=Y$,即Y中的任一元素y都是X中某元素的像，则**称f为X到Y上的映射或满射**；
**例：**

$$X=\{(x,y)|x^2 + y^2=1\},Y=\{(x,0)||x| \le 1\},f:X \rightarrow Y \qquad \mbox{每个$(x,y) \in X$,有唯一的$(x,0) \in Y与之对应$}$$

* **单射** 设$f$是从集合X到集合Y上的映射，若对X中任意俩个不同的元素$x_{1} \ne x_{2}$,他们的像$f(x_{1}) \ne f(x_{2})$,则**称f为X到Y的单射**；
**例：**

$$f:[-\frac{\pi}{2},\frac{\pi}{2}] \rightarrow [-1, 1] \qquad \mbox{对每个$x\in [-\frac{\pi}{2},\frac{\pi}{2}]$, $f(x)=sinx,f是一个映射$，‘同时是满射和单射’ }$$

* **一一映射(或双射)** 设$f$是从集合X到集合Y上的映射, 若**映射f**即是单射又是满射，则**f为一一映射或双射**；

**泛函**
从非空集合X到Y的映射又称X上的泛函。

**变换**
从非空集合X到其自身的映射又称X上的变换。

**函数**
从实数集(或其子集)X到实数集Y的映射通常称为定义在X上的函数。

### 1.1.1.2. 逆映射与复合映射

*设f是X到Y的单射，则由定义，对每个$y \in R_{f}有唯一的x \in X适合f(x)=y$,于是我们可以定义一个从$R_{f}到X的新映射g$，即*

$$g:R_{f} \rightarrow X$$

*对每个$y \in R_{f}$，$规定g(y)=x$,$这满足f(x)=y$,这个映射g称为f的逆映射，$记作f^{-1}$,$其定义域D_{f^{-1}}=R_{f}$,$值域R_{f^{-1}}=X$。*

**注**
只有单射存在逆映射。

## 1.1.2. 函数 *****

### 1.1.2.1. 函数的概念

设数集$D \subset R$,则称映射$f:D \rightarrow R为定义在D上的函数，通常简记为:$

$$y=f(x),x \in D$$

其中x为自变量，y称为因变量，D称为定义域(记作$D_{f},即D_{f}=D$);函数$f在x\in D对应的y=f(x),x\in D的函数值所组成的集合，称为函数的值域，常记作R_{f},$

$$R_{f}=\{y|y=f(x),x \in D\}$$

**常见的集中分段函数：**

* 绝对值函数

$$公式：\qquad \qquad y = |x| =
\begin{cases}
    x, \qquad & x \gt 0, \\
    0, \qquad & x = 0, \\
		-x, \qquad & x \lt 0
\end{cases}
$$

* 符号函数

$$公式：\qquad \qquad y = sgn \;x =
\begin{cases}
	-1, & x \lt 0, \\
	0, & x = 0, \\
	1, & x \gt 0
\end{cases}
$$

* 取整函数

$$
y = [x]
$$

**性质：**
*对于$x \in (-\infty, +\infty), 有[x] \le x \le [x] + 1,且[x+1]=[x] + 1$*

$$
狄利克雷函数: \qquad \qquad D(x) =
\begin{cases}
	1, \qquad \qquad \mbox{$x$为有理数时} \\
	0, \qquad \qquad \mbox{$x$为无理数时}
\end{cases}
$$

### 1.1.2.2. 函数的几种特性

#### 1.1.2.2.1. 有界性

**有界性的定义:**<br>
设函数$f(x)的定义域为D$,$数集X \subseteq D$.如果存在数$M_{1}$,使得
$$
f(x) \le M_{1},
$$
对任一$x \in X都成立$，则称函数$f(x)在X上有界$，而$M_{1}称为函数f(x)在X$上的一个上界，如果存在$M_{2}$,使得
$$
f(x) \ge M_{2},
$$
对任一$x \in X都成立$，则称函数$f(x)在X上有下界$，而$M_{2}称为函数f(x)在X上的一个下界$。如果存在正数$M$,使得
$$
|f(x)| \le M,
$$
对任一$x \in X都成立$，则称函数$f(x)在X上有界$。如果这样的$M$不存在，则称函数$f(x)在X上无界$；或者说，如果对于任何正数$M$,总存在$x_{0} \in X$,$使|f(x_{0})| \gt M$,则称函数$f(x)在X上无界$。

$如果函数f(x)在其定义域上有界就简称f(x)有界，或者说f(x)是有界函数$。

由以上定义知

$$sinx,cosx,arcsinx,arctanx,arccosx都是有界函数且|sinx| \le 1,|cosx|\le1,|arcsinx|\le\frac{\pi}{2},|arctanx|\lt\frac{\pi}{2},|arccosx|\le\pi
$$

**有界性的判定:**<br>

#### 1.1.2.2.2. 单调性

#### 1.1.2.2.3. 奇偶性

#### 1.1.2.2.4. 周期性

### 1.1.2.3. 反函数和复合函数

### 1.1.2.4. 函数的运算

### 1.1.2.5. 基本初等函数

* 常值函数

$$
f(x) = C, \qquad \mbox{C为常数}
$$

* 幂函数

$$
f(x)=x^a, \qquad （a为常数；其定义域由a确定，但不论a如何，在(0,+\infty)内总有定义
$$

* 指数函数

$$
f(x) = a^x, \qquad (a \gt 0, a \ne 1, x \in R)
$$

* 对数函数

$$
f(x) = log_{a}^{x}, \qquad (a>0, a \ne 1, x \in (0, +\infty))
$$

* 三角函数

$$
f(x) = sin \; x, \quad\qquad\qquad (x \in (-\infty, + \infty)) \\
f(x) = cos \; x, \quad\qquad\qquad (x \in (-\infty, + \infty)) \\
f(x) = tan \; x, \qquad (x \in (k\pi-\frac{\pi}{2}, k\pi + \frac{\pi}{2});k \in Z \\
f(x) = cot \; x, \qquad (x \in (k\pi, (k+1)\pi)); k \in Z
$$

* 反三角函数

$$
arcsin \; x, \qquad (x \in [-1, 1]) \\
arccos \; x, \qquad (x \in [-1, 1]) \\
arctan \; x, \qquad\qquad (x \in R) \\
arccot \; x, \qquad\qquad (x \in R)
$$
