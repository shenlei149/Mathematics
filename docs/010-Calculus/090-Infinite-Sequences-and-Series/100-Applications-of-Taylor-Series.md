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
有时，我们可以用熟悉的泰勒级数来找到给定幂级数的和，结果使用已知很熟表示。比如
$$x^2-\frac{x^6}{3!}+\frac{x^{10}}{5!}-\frac{x^{14}}{7!}+\cdots=(x^2)-\frac{(x^2)^3}{3!}+\frac{(x^2)^5}{5!}-\frac{(x^2)^7}{7!}+\cdots=\sin x^2$$

泰勒级数还可以应用于使用级数的形式表示非初等积分的结果。比如光的衍射中会涉及的积分 $\int\sin x^2 dx$。

例3 使用幂级数表示
$$\int\sin x^2 dx$$
解：用 $x^2$ 代替 $x$ 代入 $\sin x$ 的级数可以得到
$$\sin x^2=x^2-\frac{x^6}{3!}+\frac{x^{10}}{5!}-\frac{x^{14}}{7!}+\cdots$$
所以
$$\int\sin x^2dx=C+\frac{x^3}{3}-\frac{x^7}{7\cdot 3!}+\frac{x^{11}}{11\cdot 5!}-\frac{x^{15}}{15\cdot 7!}+\cdots$$

例4 估算 $\int_0^1\sin x^2 dx$，误差小于 0.001。

解：从例 3 的不定积分中，可以容易得到
$$\int_0^1\sin x^2dx=\frac{1}{3}-\frac{1}{7\cdot 3!}+\frac{1}{11\cdot 5!}-\frac{1}{15\cdot 7!}+\cdots$$
右边是交错级数，且
$$\frac{1}{11\cdot 5!}\approx 0.00076$$
是第一项绝对值小于 0.001 项。因此前两项的和即满足要求。
$$\int_0^1\sin x^2dx\approx\frac{1}{3}-\frac{1}{42}\approx 0.310$$
多加两项
$$\int_0^1\sin x^2dx\approx\frac{1}{3}-\frac{1}{42}+\frac{1}{1320}-\frac{1}{75600}\approx 0.310268$$
误差小于 $10^{-6}$。再多加一项有
$$\int_0^1\sin x^2dx\approx\frac{1}{3}-\frac{1}{42}+\frac{1}{1320}-\frac{1}{75600}+\frac{1}{6894720}\approx 0.310268303$$
误差大约是 $1.08\times 10^{-9}$。

### 反正切
9.7 节的例 5 给出了如下结论
$$\frac{d}{dx}\tan^{-1}x=\frac{1}{1+x^2}=1-x^2+x^4-x^6+\cdots$$
积分得到
$$\tan^{-1}x=x-\frac{x^3}{3}+\frac{x^5}{5}-\frac{x^7}{7}+\cdots$$
下面我们给出证明。从积分前的式子开始推导。
$$\frac{1}{1+t^2}=1-t^2+t^4-t^6+\cdots+(-1)^nt^{2n}+\frac{(-1)^{n+1}t^{2t+2}}{1+t^2}$$
其中最后一项是首项是 $a=(-1)^{n+1}t^{2n+2}$ 公比是 $r=-t^2$ 的等比数列的和。两边对 $t=0$ 到 $t=x$ 积分
$$\tan^{-1}x=x-\frac{x^3}{3}+\frac{x^5}{5}-\frac{x^7}{7}+\cdots+(-1)^n\frac{x^{2n+1}}{2n+1}+R_n(x)$$
其中
$$R_n(x)=\int_0^x\frac{(-1)^{n+1}t^{2n+2}}{1+t^2}dt$$
被积分式子的分母大于等于 1，因此
$$|R_n(x)|\leq\int_0^{|x|}t^{2n+2}dt=\frac{|x|^{2n+3}}{2n+3}$$
如果 $|x|<1$，当 $n\to\infty$ 时，不等式右边趋于零。因此 $|x|\leq 1$ 时 $\lim_{n\to\infty}R_n(x)=0$，且有
$$\tan^{-1}x=\sum_{n=0}^\infty\frac{(-1)^nx^{2n+1}}{2n+1},|x|\leq 1$$
$$\tan^{-1}x=x-\frac{x^3}{3}+\frac{x^5}{5}-\frac{x^7}{7}+\cdots,|x|\leq 1$$
当 $x=1$ 时，我们得到了莱布尼茨公式
$$\frac{\pi }{4}=1-\frac{1}{3}+\frac{1}{5}-\frac{1}{7}+\frac{1}{9}-\cdots+\frac{(-1)^n}{2n+1}+\cdots$$
这个级数收敛的很慢，所以我们不会使用这个式子来估算 $\pi$ 的值。当 $x$ 趋于零的时候，$\tan^{-1}x$ 的级数收敛的最快。因此，可以利用一些三角恒等变形来估算 $\pi$。

比如如果
$$\alpha=\tan^{-1}\frac{1}{2},\beta=\tan^{-1}\frac{1}{3}$$
那么
$$\tan(\alpha+\beta)=\frac{\tan\alpha+\tan\beta}{1-\tan\alpha\tan\beta}=1=\tan\frac{\pi}{4}$$
因此
$$\frac{\pi}{4}=\alpha+\beta=\tan^{-1}\frac{1}{2}+\tan^{-1}\frac{1}{3}$$
将 $x=\frac{1}{2},x=\frac{1}{3}$ 代入公式估算 $\tan^{-1}(1/2),\tan^{-1}(1/3)$ 的值，进而得到 $\pi$ 的值。

### 
