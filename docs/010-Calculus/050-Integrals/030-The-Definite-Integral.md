### 定积分的定义
对于某些函数而言，随着区间 $[a,b]$ 上的分区的模趋于零，黎曼和趋于极限值 $J$，这就是定积分的定义。引入符号 $\varepsilon$ 是一个小的整数，表示黎曼和要多么接近极限值 $J$，符号 $\delta$ 表示模多小的时候和收敛。

**定义** 令 $f(x)$ 是定义在闭区间 $[a,b]$ 上的函数。如果 $J$ 满足下面的条件，那么是黎曼和 $\sum_{k=1}^nf(c_k)\Delta x_k$ 的极限，即是 $f$ 在 $[a,b]$ 上的**定积分**：  
给定任意数 $\varepsilon>0$ 都有一个与之相应的 $\delta>0$ 使得对 $[a,b]$ 上任意分区 $P=\{x_0,x_1,\cdots,x_n\}$，其模满足 $\parallel P\parallel <\delta$，任意选择 $c_k\in[x_{k-1},x_k]$ 都有
$$\bigg|\sum_{k=1}^nf(c_k)\Delta x_k-J\bigg|<\varepsilon$$

模趋于零的分区有无数多，$c_k$ 的选择也任意多。不管如何选择，总能得到同样的极限值 $J$，那么定积分才存在。当极限存在时
$$J=\lim_{\parallel P\parallel\to 0}\sum_{k=1}^nf(c_k)\Delta x_k$$
莱布尼茨发明了记号 $\int$ 表示积分，是和（`Sum`）的首字母 $S$ 的变形。有限和变成了无限和，函数值 $f(x)$ 替代 $f(c_k)$ 乘以无穷小量 $dx$。记作
$$\int_a^b f(x)dx$$
当定积分存在时，$f$ 在 $[a,b]$ 上的黎曼和收敛于定积分 $J=\int_a^b f(x)dx$，并且 $f$ 在$[a,b]$ 上是可积的。  
如果所有区间相等 $\Delta x=(b-a)/n$，黎曼和形式是
$$S_n=\sum_{k=1}^nf(c_k)\Delta x_k=\sum_{k=1}^nf(c_k)\frac{b-a}{n}$$
其中 $c_k$ 是第 $k$ 个区间选择的值。如果定积分存在，那么
$$J=\int_a^bf(x)dx=\lim_{n\to\infty}\sum_{k=1}^nf(c_k)\frac{b-a}{n}$$
如果令每个子区间的右端点为 $c_k$，那么 $c_k=a+k\Delta x=a+k(b-a)/n$，那么公式变成
$$\int_a^bf(x)dx=\lim_{n\to\infty}\sum_{k=1}^nf(a+k\frac{b-a}{n})(\frac{b-a}{n})$$
上面的公式可以用于计算定积分。随着分区的模趋于令，那么 $n\to\infty$，不管如何选择分区和 $c_k$，黎曼和都会收敛到同一个值。  
一个函数的定积分的值之和函数自身相关，和用哪个字母表示无关。下面三种表示是等价的。
$$\int_a^bf(t)dt,\int_a^bf(u)du,\int_a^bf(x)dx$$

### 可积函数和非可积函数
即使函数是有界的，也不是所有函数在闭区间 $[a,b]$ 上都是可积的。对于一些函数，黎曼和不会趋于同一个值，甚至不收敛。函数是否可积需要更高等的数学分析知识，不过幸好应用中遇到的绝大多数函数都是可积的。函数在 $[a,b]$ 上连续或者只有有限个跳跃点（分段连续函数）是可积的。  
简单地说，$f$ 是连续的，我们可以选择每个区间的最大值对应的变量作为 $c_k$，那么得到一个上界。类似地，可以得到下界。当分区 $P$ 的模趋于零的时候，可以证明上界和下届收敛到同一个极限值。每一个黎曼和都介于这两者之间，所以这些黎曼和也都收敛到同样的极限值。  
一个函数非常地不连续，那么可能不可积。看下面的例子。

例1 函数
$$f(x)=\begin{cases}
1,&&x \text{ is rational}\\
0,&&x \text{ is irrational}
\end{cases}$$
在 $[0,1]$ 上定积分不存在。我们已经知道任意两个数之间都存在一个无理数和一个有理数。那么这个函数会在 $[0,1]$ 上无规则的上下跳跃。下面证明上和和下和收敛于不同的极限值。  
如果在 $[0,1]$ 上选择一个分区 $P$，分区的长度和是 1，即 $\sum_{k=1}^n\Delta x_k=1$。每个区间上都会有一个有理数，称为 $c_k$，那么 $f(c_k)=1$。同时，1 是各个区间的最大值，所以上和是
$$U=\sum_{k=1}^nf(c_k)\Delta x_k=\sum_{k=1}^n 1\Delta x_k=1$$
同样地，每个区间也都有一个无理数，那么每个区间的最小值是 0，所以下和是
$$L=\sum_{k=1}^nf(c_k)\Delta x_k=\sum_{k=1}^n 0\Delta x_k=0$$
所以上和和下和收敛于不同值，也就是选择不同的 $c_k$，黎曼和有不同的极限值。根据定义，定积分不存在。

### 定积分的属性
我们定义 $\int_a^b f(x)dx$ 作为 $\sum_{k=1}^n f(c_k)\Delta x_k$ 的极限，从左往右扫过区间 $[a,b]$。如果从右向左呢？从 $x_0=b$ 开始到 $x_n=a$？黎曼和中的每一个 $\Delta x_k$ 的符号都发生了改变，选择同样的 $c_k$，那么黎曼和的符号改变了，那么极限值、定积分也都一样。那么我们得到定义
$$\int_a^bf(x)dx=-\int_b^af(x)dx$$
尽管一般情况下区间 $[a,b]$ 有 $a<b$，不过很容易得到 $a=b$ 的情况。因为 $\Delta x=0$，不管 $f(a)$ 的值是多少，乘积都为零。那么
$$\int_a^af(x)dx=0$$
下面给出一些定积分的运算法则。前两个就是上述的定义。后面几个需要严格证明。我们后面会给出法则 6 的证明，其余是类似的。
$$\begin{aligned}
\int_a^bf(x)dx&=-\int_b^af(x)dx\\
\int_a^af(x)dx&=0\\
\int_a^bkf(x)dx&=k\int_a^bf(x)dx\\
\int_a^b(f(x)\pm g(x))dx&=\int_a^bf(x)dx\pm \int_a^bg(x)dx\\
\int_a^bf(x)dx+\int_b^cf(x)dx&=\int_a^cf(x)dx\\
(\text{min } f)(b-a)&\leq \int_a^bf(x)dx\leq (\text{max }f)(b-a)\\
\int_a^bf(x)dx&\geq\int_a^bg(x)dx \text{ , if } f(x)\geq g(x)\\
\int_a^bf(x)dx&\geq 0 \text{ , if }f(x)\geq 0
\end{aligned}$$
下面的图像是法则二到七的几何解释。图像中的函数都是正值，不过法则具有普适性，函数值可正可负。  
![](030.010.png)

证明法则六：规则六是说，$f$ 在 $[a,b]$ 上的积分不会小于最小值乘以区间长度，不会大于最大值乘以区间长度。在 $[a,b]$ 上的任意分区任意选取 $c_k$ 都有
$$\begin{aligned}
(\text{min } f)(b-a)&\leq (\text{min } f)\sum_{k=1}^n\Delta x_k\\
&=\sum_{k=1}^n (\text{min } f) \Delta x_k\\
&\leq\sum_{k=1}^n f(c_k)\Delta x_k\\
&\leq\sum_{k=1}^n (\text{max } f) \Delta x_k\\
&=(\text{max } f)\sum_{k=1}^n\Delta x_k\\
&=(\text{max } f)(b-a)
\end{aligned}$$
也就是说，所有的黎曼和都满足不等式
$$(\text{min } f)(b-a)\leq \sum_{k=1}^n f(c_k)\Delta x_k\leq (\text{max } f)(b-a)$$
因此，黎曼和的极限，即定积分，也满足这个不等式。

例2 假设
$$\int_{-1}^1f(x)dx=5,\int_1^4f(x)dx=-2,\int_{-1}^1h(x)dx=7$$
运用上述法则可以得到下列结果
$$\int_4^1f(x)dx=-\int_1^4f(x)dx=-(-2)=2$$
$$\begin{aligned}
\int_{-1}^1[2f(x)+3h(x)]dx&=2\int_{-1}^1f(x)dx+3\int_{-1}^1h(x)dx\\
&=2(5)+3(7)\\
&=31
\end{aligned}$$
$$\begin{aligned}
\int_{-1}^4f(x)dx&=\int_{-1}^1f(x)dx+\int_1^4f(x)dx\\
&=5+(-2)\\
&=3
\end{aligned}$$
