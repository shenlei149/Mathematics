一个级数中的项有正有负，它可能收敛也可能发散。比如下面的等比级数
$$5-\frac{5}{4}+\frac{5}{16}-\frac{5}{64}+\cdots=\sum_{n=0}^\infty 5(\frac{-1}{4})^n$$
收敛，原因是 $|r|=\frac{1}{4}<1$。不过下面的等比级数
$$1-\frac{5}{4}+\frac{25}{16}-\frac{125}{64}+\cdots=\sum_{n=0}^\infty(\frac{-5}{4})^n$$
就是发散的，因为公比 $|r|=\frac{5}{4}>1$。对于第一个级数，计算部分和的时候，一些项可以相互抵消，帮助其收敛。让级数的所有项都是正数，我们得到新的级数
$$5+\frac{5}{4}+\frac{5}{16}+\frac{5}{64}+\cdots=\sum_{n=0}^\infty |5(\frac{-1}{4})^n|=\sum_{n=0}^\infty5(\frac{1}{4})^n$$
仍旧收敛。

**定义**
> 如果一个级数 $\sum a_n$ 各项绝对值组成的级数 $\sum |a_n|$ 收敛，那么称级数 $\sum a_n$ 绝对收敛。

**定理 12 绝对收敛测试**
> 如果 $\sum_{n=1}^\infty |a_n|$ 收敛，那么 $\sum_{n=1}^\infty a_n$ 收敛。

证明：对于任意 $n$，都有
$$-|a_n|\leq a_n\leq |a_n|$$
那么
$$0\leq a_n+|a_n|\leq 2|a_n|$$
如果 $\sum_{n=1}^\infty |a_n|$ 收敛，根据直接比较测试，$\sum_{n=1}^\infty 2|a_n|$ 收敛，所以非负级数 $\sum_{n=1}^\infty (a_n+|a_n|)$ 也收敛。那么通过 $a_n=(a_n+|a_n|)-|a_n|$ 可以将级数 $\sum_{n=1}^\infty a_n$ 表达成两个收敛级数的差：
$$\sum_{n=1}^\infty a_n=\sum_{n=1}^\infty(a_n+|a_n|-|a_n|)=\sum_{n=1}^\infty(a_n+|a_n|)-\sum_{n=1}^\infty|a_n|$$
因此，$\sum_{n=1}^\infty a_n$ 收敛。

例1 下面是两个绝对收敛的例子。

（a）级数 $\sum_{n=1}^\infty(-1)^{n+1}\frac{1}{n^2}=1-\frac{1}{4}+\frac{1}{9}-\frac{1}{16}+\cdots$ 对应的绝对值级数
$$\sum_{n=1}^\infty\frac{1}{n^2}=1+\frac{1}{4}+\frac{1}{9}+\frac{1}{16}+\cdots$$
收敛，所以原级数绝对收敛。

（b）级数 $\sum_{n=1}^\infty\frac{\sin n}{n^2}=\frac{\sin 1}{1}+\frac{\sin 2}{4}+\frac{\sin 3}{9}+\cdots$ 包含正数项和负数项，对应的绝对值级数
$$\sum_{n=1}^\infty|\frac{\sin n}{n^2}|=\frac{|\sin 1|}{1}+\frac{|\sin 2|}{4}+\frac{|\sin 3|}{9}+\cdots$$
是收敛的，因为对于所有 $n$ 都有 $|\sin n|\leq 1$，和收敛级数 $\sum_{n=1}^\infty(1/n^2)$ 相比即可知其也收敛。所以原级数绝对收敛。

### 比值测试
通过检查 $a_{n+1}/a_n$ 的比值，可以判定级数增长或者衰减的速率。对于等比级数 $\sum ar^n$，比值 $(ar^{n+1})/(ar^n)=r$ 是常量，级数收敛等价于比值的绝对值是否小于 1。

**定理13 比值测试**
> 令 $\sum a_n$ 是任意级数且
> $$\lim_{n\to\infty}\bigg|\frac{a_{n+1}}{a_n}\bigg|=\rho$$
> （a）如果 $\rho<1$，那么级数绝对收敛
> （b）如果 $\rho>1$ 或者是无穷大，那么级数发散
> （c）如果 $\rho=1$，收敛性不确定

证明：

（a）$\rho<1$。令 $r$ 是 $\rho$ 和 1 之间的数，那么 $\varepsilon=r-\rho$ 是正数。

###
