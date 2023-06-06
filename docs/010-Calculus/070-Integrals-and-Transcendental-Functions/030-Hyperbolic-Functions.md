双曲函数由两个指数函数 $e^x,e^{-x}$ 组合得到，在数学和工程领域非常常见。

### 定义和恒等式
双曲正弦和双曲余弦定义如下
$$\sinh x=\frac{e^x-e^{-x}}{2}$$
$$\cosh x=\frac{e^x+e^{-x}}{2}$$
通过这对基本的例子，我们可以定义双曲正切、余切、正割、余割函数。
$$\tanh x=\frac{\sinh x}{\cosh x}=\frac{e^x-e^{-x}}{e^x+e^{-x}}$$
$$\coth x=\frac{\cosh x}{\sinh x}=\frac{e^x+e^{-x}}{e^x-e^{-x}}$$
$$\operatorname{sech} x=\frac{1}{\cosh x}=\frac{2}{e^x+e^{-x}}$$
$$\operatorname{csch} x=\frac{1}{\sinh x}=\frac{2}{e^x-e^{-x}}$$
图像如下图所示。  
![](030.010.png)  
满足如下恒等式。除了符号略有不同外，和三角函数的性质类似。
$$\cosh^2 x-\sinh^2 x=1$$
$$\sinh 2x=2\sinh x\cosh x$$
$$\cosh 2x=\cosh^2 x+\sinh^2 x$$
$$\cosh^2 x=\frac{\cosh 2x+1}{2}$$
$$\sinh^2 x=\frac{\cosh 2x-1}{2}$$
$$\tanh^2 x=1-\operatorname{sech}^2 x$$
$$\coth^2 x=1+\operatorname{csch}^2 x$$
这些恒等式都可以从定义出发得到证明。比如
$$\begin{aligned}
2\sinh x\cosh x&=2(\frac{e^x-e^{-x}}{2})(\frac{e^x+e^{-x}}{2})\\
&=\frac{e^{2x}-e^{-2x}}{2}\\
&=\sinh 2x
\end{aligned}$$
对于任意实数 $u$，点 $(\cos u,\sin u)$ 在单位圆 $x^2+y^2=1$ 上，所以三角函数也称为圆函数（`circular functions`）。恒等式的第一个
$$\cosh^2 u-\sinh^2 u=1$$
可知点 $(\cosh u,\sinh u)$ 在双曲线 $x^2-y^2=1$ 的右半边，这就是双曲函数（`hyperbolic function`）的由来。  
第八章将会看到双曲函数在求解积分时很有用。同时，他们在数学和工程领域也很有用。双曲余弦是一个绳索挂在等高的两个端点上绳索的形状。双曲正切描述了水深为常量时的波浪移动的速度。反双曲正切函数描述了在狭义相对论下的相对速度和。

### 双曲函数的微分和积分
六个双曲函数，是可导函数 $e^x,e^{-x}$ 的有理组合，所以在定义域上处处可导。如下所示。这些结论与三角函数类似。
$$\frac{d}{dx}\sinh u=\cosh u\frac{du}{dx}$$
$$\frac{d}{dx}\cosh u=\sinh y\frac{du}{dx}$$
$$\frac{d}{dx}\tanh u=\operatorname{sech}^2 u\frac{du}{dx}$$
$$\frac{d}{dx}\coth u=-\operatorname{csch}^2 u\frac{du}{dx}$$
$$\frac{d}{dx}\operatorname{sech} u=-\operatorname{sech} u\tanh u\frac{du}{dx}$$
$$\frac{d}{dx}\operatorname{csch} u=-\operatorname{csch} u\coth u\frac{du}{dx}$$
这些共识可以从 $e^u$ 推导出来。比如
$$\begin{aligned}
\frac{d}{dx}\sinh u&=\frac{d}{dx}(\frac{e^u-e^{-u}}{2})\\
&=\frac{e^udu/dx+e^{-udu/dx}}{2}\\
&=\cosh u\frac{du}{dx}
\end{aligned}$$
从定义出发，可以推导出双曲余割的导数。
$$\begin{aligned}
\frac{d}{dx}\operatorname{csch} u&=\frac{d}{dx}(\frac{1}{\sinh u})\\
&=-\frac{\cosh u}{\sinh^2 u}\frac{du}{dx}\\
&=-\frac{1}{\sinh u}\frac{\cosh u}{\sinh u}\frac{du}{dx}\\
&=-\operatorname{csch} u\coth u\frac{du}{dx}
\end{aligned}$$
其余公式可以用类似方法推导得出。  
从微分公式可以得到如下积分公式。
$$\int\sinh udu=\cosh u+C$$
$$\int\cosh udu=\sinh u+C$$
$$\int\operatorname{sech}^2 udu=\tanh u+C$$
$$\int\operatorname{csch}^2 udu=-\coth u+C$$
$$\int\operatorname{sech} u\tanh udu=-\operatorname{sech} u+C$$
$$\int\operatorname{csch} u\coth udu=-\operatorname{csch} u+C$$

例1  
（a）
$$\begin{aligned}
\frac{d}{dt}\tanh(\sqrt{1+t^2})&=\operatorname{sech}^2\sqrt{1+t^2}\frac{d}{dt}(\sqrt{1+t^2})\\
&=\frac{t}{\sqrt{1+t^2}}\operatorname{sech}^2\sqrt{1+t^2}
\end{aligned}$$
（b）
$$\begin{aligned}
\int\coth 5xdx&=\int\frac{\cosh 5x}{\sinh 5x}dx\\
&=\frac{1}{5}\int\frac{du}{u}\\
&=\frac{1}{5}\ln |u|+C\\
&=\frac{1}{5}\ln |\sinh 5x|+C
\end{aligned}$$
（c）
$$\begin{aligned}
\int_0^1\sinh^2xdx&=\int_0^1\frac{\cosh 2x-1}{2}dx\\
&=\frac{1}{2}\int_0^1(\cosh 2x-1)dx\\
&=\frac{1}{2}\bigg[\frac{\sinh 2x}{2}-x\bigg]_0^1\\
&=\frac{\sinh 2}{4}-\frac{1}{2}
\end{aligned}$$
（d）
$$\begin{aligned}
\int_0^{\ln 2}4e^x\sinh xdx&=\int_0^{\ln 2}4e^x\frac{e^x-e^{-x}}{2}dx\\
&=\int_0^{\ln 2}(2e^{2x}-2)dx\\
&=\bigg[e^{2x}-2x\bigg]_0^{\ln 2}\\
&=(e^{2\ln 2}-2\ln 2)-(e^0-0)\\
&=3-2\ln 2
\end{aligned}$$
