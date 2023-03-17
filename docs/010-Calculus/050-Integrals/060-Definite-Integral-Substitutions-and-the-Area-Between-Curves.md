### 换元公式
下面的公式告诉我们当使用换元法的时候，如何更新上下界。

**定理7 定积分的换元法**  
如果 $g'$ 在区间 $[a,b]$ 上连续，$f$ 在 $g(x) =u$ 的值域上连续，那么
$$\int_a^b f(g(x))\cdot g'(x)dx=\int_{g(a)}^{g(b)} f(u)du$$

证明：令 $F$ 是 $f$ 任意一个反导数，那么
$$\begin{aligned}
\int_a^b f(g(x))\cdot g'(x)dx&=F(g(x))\bigg|_{x=a}^{x=b}\\
&=F(g(b))-F(g(a))\\
&=F(u)\bigg|_{u=g(a)}^{u=g(b)}\\
&=\int_{g(a)}^{g(b)} f(u)du
\end{aligned}$$

使用定理7 分两步，首先使用 $u=g(x), du=g'(x)dx$ 替换积分式，然后修改对应的上下界到 $g(a)=u(a), g(b)=u(b)$。

例1 求 $\int_{-1}^1 3x^2\sqrt{x^3+1}dx$。  
解：下面使用两种方法求解。  
方法一：应用定理7。令 $u=x^3+1,du=3x^2,u(-1)=0,u(1)=2$。
$$\begin{aligned}
\int_{-1}^1 3x^2\sqrt{x^3+1}dx&=\int_0^2\sqrt{u}du\\
&=\frac{2}{3}u^{3/2}\bigg|_0^2\\
&=\frac{2}{3}(2^{3/2}-0)\\
&=\frac{2}{3}2\sqrt{2}\\
&=\frac{4\sqrt{2}}{3}
\end{aligned}$$
方法二：先求不定积分，是 $x$ 的表达式，然后代入上下界计算定积分。
$$\begin{aligned}
\int 3x^2\sqrt{x^3+1}dx&=\int\sqrt{u}du\\
&=\frac{2}{3}u^{3/2}+C\\
&=\frac{2}{3}(x^3+1)^{3/2}+C
\end{aligned}$$
$$\begin{aligned}
\int_{-1}^1 3x^2\sqrt{x^3+1}dx&=\frac{2}{3}(x^3+1)^{3/2}\bigg|_{-1}^1\\
&=\frac{2}{3}((1^3+1)^{3/2}-((-1)^3+1)^{3/2})\\
&=\frac{2}{3}(2\sqrt{2}-0)\\
&=\frac{4\sqrt{2}}{3}
\end{aligned}$$
