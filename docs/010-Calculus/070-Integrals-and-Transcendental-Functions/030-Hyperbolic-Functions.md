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
