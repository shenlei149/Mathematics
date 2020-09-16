## Ordinary Generating Functions
### Recurrence Relations and Generating Functions
一个池塘，每年年底从里面打捞100个青蛙，青蛙自身每年繁殖四倍，若初始时青蛙有50只，第$n$年有多少青蛙呢。  
$a_0=50,a_1=4a_0-100=100,\cdots$，很容易写出递归式$a_{n+1}=4a_n-100$，但是如果只想知道第87年的青蛙数量，就必须从1开始逐个计算，浪费了很多中间结果。  
为了避免这种情况，需要知道$a_n$的显式公式(`explicit formula`)，只依赖于$n$而不包含$a_{n-1}$或其他项，是可以直接计算得到值的。  
我们从这个递归式开始
$$a_{n+1}=4a_n-100\tag{8.1}$$
对$n\ge 0$都成立且初始值$a_0=50$。事实上上面的公式包含无穷个式子，从无穷个式子归纳出一个显式公式，就需要用到生成函数(`generating functions`)的概念。

**Definition 8.1.** $\{f_n\}_{n\geq 0}$是实数序列。形式幂级数$F(x)=\sum_{n\geq 0}f_nx^n$称之为序列$\{f_n\}_{n\geq 0}$的普通生成函数(`ordinary generating function`)。

下面计算序列$\{a_n\}$的生成函数。对$(8.1)$两边同乘$x^{n+1}$然后对$n\geq 0$的$a_n$求和。得到
$$\sum_{n\geq 0}a_{n+1}x^{n+1}=\sum_{n\geq 0}4a_nx^{n+1}-\sum_{n\geq 0}100x^{n+1}\tag{8.2}$$
由于$\sum_{n\geq 0}x^n=1/(1-x)$，所以生成函数$G(x)$为
$$G(x)-a_0=4xG(x)-\frac{100x}{1-x}\tag{8.3}$$
$$G(x)=\frac{a_0}{1-4x}-\frac{100x}{(1-x)(1-4x)}\tag{8.4}$$
生成函数$G(x)$是幂级数，将右侧也写作幂级数的形式，那么$x_n$对应的系数既为$a_n$。
$$\frac{a_0}{1-x}=50\sum_{n\geq 0}(4x)^n=50\sum_{n\geq 0}4^nx^n$$
$x_n$对应的系数是$50\cdot 4^n$。  
第二项稍微复杂一些，要用到微分方程课学到的部分函数(`partial function`)方法。
$$\frac{A}{1-x}+\frac{B}{1-4x}=\frac{100x}{(1-x)(1-4x)}$$
$$A(1-4x)+B(1-x)=100x$$
$$(-4A-B)x+(A+B)=100x$$
对应系数相等，所以$A+B=0,-4A-B=100$，那么$A=-100/3,B=100/3$，因此第二项可以写作
$$\begin{aligned}
\frac{100x}{(1-x)(1-4x)}&=\frac{100}{3}\cdot \frac{1}{1-4x}-\frac{100}{3}\cdot \frac{1}{1-x}\\
&=\frac{100}{3}(\sum_{n\geq 0}4^nx^n-\sum_{n\geq 0}x^n)\\
&=\sum_{n\geq 0}(4^n-1)x^n\frac{100}{3}
\end{aligned}$$
结合两项得到
$$a_n=50\cdot 4^n-100\cdot \frac{4^n-1}{3}\tag{8.5}$$
现在验证下$(8.5)$是正确的。$n=0$时，很容易计算得到$a_0=50$。
$$\begin{aligned}
4a_n-100&=4(50\cdot 4^n-100\cdot \frac{4^n-1}{3})-100\\
&=50\cdot x^{n+1}-100\cdot \frac{4^{n+1}-4}{3}-100\\
&=50\cdot x^{n+1}-100\cdot \frac{4^{n+1}-1}{3}
\end{aligned}$$
现在总结一下已知递归式求显式的步骤：
1. 定义$\{a_n\}$序列的生成函数$G(x)$
2. 将递归式写作包含$G(x)$的方程。一般是递归式两边同乘$x^n$或$x^{n+1}$，有时需要同乘$x^{n+k}$，然后对所有非负数$n$求和
3. 求解$G(x)$
4. 找到$G(x)$的$x^n$的系数

**Example 8.2.** 一个账户由1000块钱，年利率百分之五。然后每年存500。求第$n$年账户有多少钱。  
**Solution** 很容易写出递归式$a_0=1000,a_{n+1}=1.05\cdot a_n+500$，下面利用上面总结的步骤来求解。
1. 定义$\{a_n\}$序列的生成函数$G(x)=\sum_{n\geq 0}a_nx^n$
2. 递归式两边同乘$x^{n+1}$然后求和得到
$$\sum_{n\geq 0}a_{n+1}x^{n+1}=\sum_{n\geq 0}1.05a_nx^{n+1}+\sum_{n\geq 0}500x^{n+1}\tag{8.6}$$
$$G(x)-a_0=1.05xG(x)+\frac{500x}{1-x}$$
3. 因此
$$G(x)=\frac{1000}{1-1.05x}+\frac{500x}{(1-x)(1-1.05x)}\tag{8.7}$$
4. 现在找$x^n$的系数
$$\frac{1000}{1-1.05x}=1000\cdot\sum_{n\geq 0}1.05^nx^n$$
$$\begin{aligned}
\frac{500x}{(1-x)(1-1.05x)}&=\frac{10000}{1-1.05x}-\frac{10000}{1-x}\\
&=10000\sum_{n\geq 0}1.05^nx^n-10000\sum_{n\geq 0}x^n\\
&=10000\sum_{n\geq 0}(1.05^n-1)x^n
\end{aligned}\tag{8.8}$$
结合以上两式，得到
$$a_n=1000\cdot 1.05^n+10000\cdot (1.05^n-1)=1.05^n\cdot 11000-10000$$

下面这个例子来展示如何用这个方法将包含多项的递推式写作显式公式。  
**Example 8.3.** $n\geq 0$时，令$a_{n+2}=3a_{n+1}-2a_n, a_0=0, a_1=1$，求$a_n$。  
**Solution** 令$G(x)=\sum_{n\geq 0}a_nx^n$。递归式的两边同乘$x^{n+2}$，
$$\sum_{n\geq 0}a_{n+2}x^{n+2}=3\sum_{n\geq 0}a_{n+1}x^{n+1}-2\sum_{n\geq 0}a_nx^n$$
$$G(x)-a_1x-a_0=G(x)-x=3x(G(x)-a_0)-2x^2G(x)=3xG(x)-2x^xG(x)$$
$$G(x)=\frac{x}{1-3x-2x^2}=\frac{A}{x-1}+\frac{B}{2x-1}$$
$$x=A(2x-1)+B(x-1)=(2A+B)x-(A+B)$$
$$2A+B=1,A+B=0\rArr A=1,B=-1$$
$$\begin{aligned}
G(x)&=\frac{-1}{1-x}+\frac{1}{1-2x}\\
&=-\sum_{n\geq 0}x^n+\sum_{n\geq 0}2^nx^n\\
&=\sum_{n\geq 0}(2^n-1)x^n
\end{aligned}$$
所以
$$a_n=2^n-1$$

### Products of Generating Functions
