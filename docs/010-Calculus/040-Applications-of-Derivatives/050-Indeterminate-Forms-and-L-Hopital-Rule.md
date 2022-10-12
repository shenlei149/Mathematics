### 0/0型不定式
如果我们知道
$$f(x)=\frac{3x-\sin x}{x}$$
在$x=0$附近的行为（$x=0$处无定义），那么可以求$x\to 0$时$f(x)$的极限值。由于极限分母为零，我们不能用导数的除法法则。然而在这个例子中，分子分母都是零，而$0/0$是不确定的，其极限可能存在也可能不存在，洛必达法则（`l'Hôpital's Rule`）会告诉我们答案。  
如果连续函数$f(x),g(x)$在$x=a$处都是零，那么不能通过替换法求
$$\lim_{x\to a}\frac{f(x)}{g(x)}$$
替换出来的表示是$0/0$是没有意义的。我们用$0/0$来表示这一类极限形式，称为不定式（`indeterminate form`）。其他类似的无意义表达式如$\infty/\infty,\infty\cdot 0,\infty-\infty,0^0,1^\infty$，都不能用统一的方式求解。

**定理6 洛必达法则**  
假设$f(a)=g(a)=0$，$f,g$在包含$a$的开区间$I$上可导，且$x\neq a$时$g(x)\neq 0$。那么
$$\lim_{x\to a}\frac{f(x)}{g(x)}=\lim_{x\to a}\frac{f'(x)}{g'(x)}$$
假设右边的极限存在。  
本节最后会给出证明。

例1 求下面$0/0$型的极限值。有的例子中需要反复使用洛必达法则。  
（a）
$$\lim_{x\to 0}\frac{3x-\sin x}{x}=\lim_{x\to 0}\frac{3-\cos x}{1}=2$$
（b）
$$\lim_{x\to 0}\frac{\sqrt{1+x}-1}{x}=\lim_{x\to 0}\frac{\frac{1}{2\sqrt{1+x}}}{1}=\frac{1}{2}$$
（c）
$$\begin{aligned}
\lim_{x\to 0}\frac{\sqrt{1+x}-1-x/2}{x^2}&=\lim_{x\to 0}\frac{(1/2)(1+x)^{-1/2}-1/2}{2x}\\
&=\lim_{x\to 0}\frac{-(1/4)(1+x)^{-3/2}}{2}\\
&=-\frac{1}{8}
\end{aligned}$$
（d）
$$\begin{aligned}
\lim_{x\to 0}\frac{x-\sin x}{x^3}&=\lim_{x\to 0}\frac{1-\cos x}{3x^2}\\
&=\lim_{x\to 0}\frac{\sin x}{6x}\\
&=\lim_{x\to 0}\frac{\cos x}{6}\\
&=\frac{1}{6}
\end{aligned}$$

**使用洛必达法则**  
反复使用洛必达法则，直至分子和分母有一个是有限非零极限。

例2 使用洛必达法则要小心
$$\lim_{x\to 0}\frac{1-\cos x}{x+x^2}=\lim_{x\to 0}\frac{\sin x}{1+2x}$$
右边不是$0/0$不定式。如果进一步使用洛必达法则会得到
$$\lim_{x\to 0}\frac{\cos x}{2}=\frac{1}{2}$$
答案是不正确的。洛必达法则只适用于不定式，而$\lim_{x\to 0}(\sin x)/(1+2x)$不是不定式，通过代入法得到极限是$0/1=0$。

洛必达法则对单边极限也适用。

例3 这个例子中单边极限是不同的。  
（a）
$$\lim_{x\to 0^+}\frac{\sin x}{x^2}=\lim_{x\to 0^+}\frac{\cos x}{2x}=\infty$$
（b）
$$\lim_{x\to 0^-}\frac{\sin x}{x^2}=\lim_{x\to 0^-}\frac{\cos x}{2x}=-\infty$$

### $\infty/\infty,\infty\cdot 0,\infty-\infty$型不定式
