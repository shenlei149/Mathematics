微积分基本定理是说如果能找到一个函数的反导数，那么可以计算出一个连续函数的定积分。4.8 节我们给出了不定积分（`indefinite integral`）的定义，是函数 $f$ 所有的反导数，记作 $\int f(x)dx$。由于任意两个反导数之间差一个常数，那么不定积分是任意的反导数
$$\int f(x)dx=F(x)+C$$
微积分基本定理中表明的反导数和定积分的关系可以使用这个符号来解释：
$$\begin{aligned}
\int_a^bf(x)dx&=F(b)-F(a)\\
&=[F(b)+C]-[F(a)+C]\\
&=[F(x)+C]_a^b\\
&=\bigg[\int f(x)dx\bigg]_a^b
\end{aligned}$$
当我们找到 $f$ 的不定积分时，不要忘了最后加一个常量 $C$。  
我们必须严格区分定积分和不定积分。定积分 $\int_a^bf(x)dx$ 是一个数，而不定积分 $\int f(x)dx$ 是一个函数加上一个常数。  
目前，求反导数只能靠直接识别哪个函数的微分是该函数。下面介绍换元法，是一种更通用的方法。

### 换元法：反向链式法则
如果 $u$ 是关于 $x$ 的可导函数，$n$ 除了 -1 以外的整数，那么
$$\frac{d}{dx}(\frac{u^{n+1}}{n+1})=u^n\frac{du}{dx}$$
从另一个角度看，$\frac{u^{n+1}}{n+1}$ 是 $u^n(du/dx)$ 的反导数。因此
$$\int u^n\frac{du}{dx}dx=\frac{u^{n+1}}{n+1}+C$$
简写为
$$\int u^ndu=\frac{u^{n+1}}{n+1}+C$$
可以简单的看作是 $du$ 替换了 $(du/dx)dx$。莱布尼茨就洞察了这一点，引导出换元法来计算积分。与微分一样，计算积分时也有
$$du=\frac{du}{dx}dx$$

例1 求积分 $\int(x^3+x)^5(3x^2+1)dx$。  
解：令 $u=x^3+x$，那么
$$du=\frac{du}{dx}dx=(3x^2+1)dx$$
所以通过替换得到
$$\begin{aligned}
\int(x^3+x)^5(3x^2+1)dx&=\int u^5du\\
&=\frac{u^6}{6}+C\\
&=\frac{(x^3+x)^6}{6}+C
\end{aligned}$$

例2 求积分 $\int\sqrt{2x+1}dx$。  
解：这个积分不适用公式
$$\int u^ndu$$
因为令 $u=2x+1,n=1/2$，那么
$$du=\frac{du}{dx}dx=2dx$$
这不是 $dx$。原始积分中并没有 2。不过我们可以再积分号之外乘以 $1/2$ 以补偿这个因数。所以可以得到
$$\begin{aligned}
\int\sqrt{2x+1}dx&=\frac{1}{2}\int\sqrt{2x+1}\cdot 2dx\\
&=\frac{1}{2}\int u^{1/2} du\\
&=\frac{1}{2}\frac{u^{3/2}}{3/2}+C\\
&=\frac{1}{3}(2x+1)^{3/2}+C
\end{aligned}$$

**定理6 换元法**  
如果 $u=g(x)$ 在值域 $I$ 上可导，$f$ 在 $I$ 上连续，那么
$$\int f(g(x))g'(x)dx=\int f(u)du$$
证明：令 $F$ 是 $f$ 的反导数，由链式法则得到
$$\frac{d}{dx}F(g(x))=F'(g(x))g'(x)=f(g(x))g'(x)$$
所以 $F(g(x))$ 是 $f(g(x))g'(x)$ 的反导数。令 $u=g(x)$，那么
$$\begin{aligned}
\int f(g(x))g'(x)dx&=\int\frac{d}{dx}F(g(x))dx\\
&=F(g(x))+C\\
&=F(u)+C\\
&=\int F'(u)du\\
&=\int f(u)du
\end{aligned}$$
惯例使用 $u$ 作为换元法的变量，也可以使用其他变量名，比如 $v,t,\theta$ 等。如果满足定理6 的条件，那么形如 $\int f(g(x))g'(x)dx$ 的积分可以用换元法求解。这里主要挑战是确定哪个表达式被替换。

例3 求 $\int\sec^2(5x+1)\cdot 5dx$。  
解：令 $u=5x+1$，那么 $du=5dx$，所以
$$\begin{aligned}
\int\sec^2(5x+1)\cdot 5dx&=\int\sec^2udu\\
&=\tan u+C\\
&=\tan(5x+1)+C
\end{aligned}$$
