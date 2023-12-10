### 二项式级数
$f(x)=(1+x)^m$ 的泰勒级数是
$$\begin{aligned}
1+mx+\frac{m(m-1)}{2!}x^2&+\frac{m(m-1)(m-2)}{3!}x^3+\cdots\\
&+\frac{m(m-1)(m-2)\cdots(m-k+1)}{k!}x^k+\cdots
\end{aligned}$$
这个级数称为二项式级数（`binomial series`）。当 $|x|<1$ 时绝对收敛。对这个级数求导可以得到以下函数及其导数
$$\begin{aligned}
f(x)&=(1+x)^m\\
f'(x)&=m(1+x)^{m-1}\\
f''(x)&=m(m-1)(1+x)^{m-2}\\
f'''(x)&=m(m-1)(m-2)(1+x)^{m-3}\\
&\vdots\\
f^{(k)}(x)&=m(m-1)(m-2)\cdots(m-k+1)x^{m-k}
\end{aligned}$$
将 $x=0$ 代入上面各个式子就能得到泰勒级数的公式了。

如果 $m$ 是大于等于零的正整数，那么这个系列有 $m+1$ 项，因为从 $k=m+1$ 开始系数是零。

如果 $m$ 不是正整数或零，这个级数无穷多项，且在 $|x|<1$ 时收敛。证明很简单，令 $u_k$ 涉及 $x_k$ 的项，根据比值测试
$$\bigg|\frac{u_{k+1}}{u_k}\bigg|=\bigg|\frac{m-k}{k+1}x\bigg|\to |x|$$
这仅仅证明了 $(1+x)^m$ 的泰勒级数在 $|x|<1$ 时成立。下面证明其收敛于 $(1+x)^m$。

令 $f(x)=1+\sum_{k=1}^\infty\begin{pmatrix}
m\\k
\end{pmatrix}x^k$，展开记作
$$\begin{aligned}
f(x)=1+mx+\frac{m(m-1)}{2!}x^2&+\frac{m(m-1)(m-2)}{3!}x^3\cdots\\
&+\frac{m(m-1)\cdots(m-k+2)}{(k-1)!}x^{k-1}\\
&+\frac{m(m-1)\cdots(m-k+2)(m-k+1)}{k!}x^k\\
&+\cdots
\end{aligned}$$
求导
$$\begin{aligned}
f'(x)=m+m(m-1)x&+\frac{m(m-1)(m-2)}{2!}x^2+\cdots\\
&+\frac{m(m-1)\cdots(m-k+2)}{(k-2)!}x^{k-2}\\
&+\frac{m(m-1)\cdots(m-k+2)(m-k+1)}{(k-1)!}x^{k-1}\\
\cdots
\end{aligned}$$
两边同时乘以 $x$
$$\begin{aligned}
xf'(x)=mx+m(m-1)x^2&+\frac{m(m-1)(m-2)}{2!}x^3+\cdots\\
&+\frac{m(m-1)\cdots(m-k+2)}{(k-2)!}x^{k-1}\\
&+\frac{m(m-1)\cdots(m-k+2)(m-k+1)}{(k-1)!}x^{k}\\
\cdots
\end{aligned}$$
两式相加，下面只处理 $x^{k-1}$ 项
$$\begin{aligned}
\frac{m(m-1)\cdots(m-k+2)(m-k+1)}{(k-1)!}x^{k-1}&+\frac{m(m-1)\cdots(m-k+2)}{(k-2)!}x^{k-1}\\
&=\frac{m(m-1)(m-k+2)}{(k-2)!}x^{k-1}(\frac{m-k+1}{k-1}+1)\\
&=\frac{m(m-1)(m-k+2)}{(k-2)!}x^{k-1}(\frac{m-k+1+k-1}{k-1})\\
&=m\frac{m(m-1)(m-k+2)}{(k-1)!}x^{k-1}
\end{aligned}$$
除去前面的系数 $m$，恰好是 $f(x)$ 关于 $x^{k-1}$这一项，那么
$$(1+x)f'(x)=mf(x)$$
即
$$f'(x)=\frac{mf(x)}{(1+x)}$$
令 $g(x)=(1+x)^{-m}f(x)$，求导
$$g'(x)=-m(1+x)^{-m-1}f(x)+(1+x)^{-m}\frac{mf(x)}{1+x}=f(x)(1+x)^{-m-1}(-m+m)=0$$
那么 $g(x)=C$，令 $x=0$，
$g(0)=C=1\cdot 1=1$，因此
$$g(x)=1$$
那么
$$f(x)=(1+x)^m$$

**二项式级数**
> $-1<x<1$ 时
> $$(1+x)^m=1+\sum_{k=1}^\infty\begin{pmatrix}
m\\k
\end{pmatrix}x^k$$

例1 如果 $m=-1$，那么
$$\begin{pmatrix}
-1\\1
\end{pmatrix}=1$$
$$\begin{pmatrix}
-1\\2
\end{pmatrix}=\frac{(-1)(-2)}{2!}=1$$
$$\begin{pmatrix}
-1\\k
\end{pmatrix}=\frac{(-1)(-2)(-3)\cdots(-1-k+1)}{k!}=(-1)^k$$
此时，二项式级数是等比级数
$$(1+x)^{-1}=1+\sum_{k=1}^\infty(-1)^kx^k=1-x+x^2-x^3+\cdots+(-1)^kx^k+\cdots$$

例2 从 3.11 小节例 1 可知 $\sqrt{1+x}\approx 1+(x/2)$。令 $m=1/2$，使用二项式级数，可以得到更高阶的近似项。
$$\begin{aligned}
(1+x)^{1/2}&=1+\frac{x}{2}+\frac{(1/2)(-1/2)}{2!}x^2\\
&+\frac{(1/2)(-1/2)(-3/2)}{3!}x^3\\
&+\frac{(1/2)(-1/2)(-3/2)(-5/2)}{4!}x^4\\
&+\cdots\\
&=1+\frac{x}{2}-\frac{x^2}{8}+\frac{x^3}{16}-\frac{5x^4}{128}+\cdots
\end{aligned}$$
将 $x$ 替换成其他式子可以得到其他近似公式。比如
$$\sqrt{1-x^2}\approx 1-\frac{x^2}{2}-\frac{x^4}{8},|x^2|\text{ small}$$
$$\sqrt{1-\frac{1}{2}}\approx 1-\frac{1}{2x}-\frac{1}{8x^2},|\frac{1}{x}|\text{ small}，|x| \text{ large}$$

### 求非初等积分
