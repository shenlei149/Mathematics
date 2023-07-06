[公式大全](/formula.md)给出了很多函数的积分，下面也会再次列出几个基本函数的积分公式，结合第五章学习的替换法，能够解决很多更复杂的函数。
$$\int kdx=kx+C$$
$$\int x^ndx=\frac{x^{n+1}}{n+1}+C,n\neq -1$$
$$\int\frac{dx}{x}=\ln|x|+C$$
$$\int e^xdx=e^x+C$$
$$\int a^x=\frac{a^x}{\ln a}+C,a>0,a\neq 1$$

例1 求
$$\int_3^5\frac{2x-3}{\sqrt{x^2-3x+1}}dx$$
解：
$$\begin{aligned}
\int_3^5\frac{2x-3}{\sqrt{x^2-3x+1}}dx&=\int_1^{11}\frac{du}{\sqrt{u}}&&u=x^2+3x+1\\
&=2\sqrt{u}\bigg|_1^{11}\\
&=2(\sqrt{11}-1)
\end{aligned}$$

例2 配方法以求解
$$\int\frac{dx}{\sqrt{8x-x^2}}$$
解：对分母根号中的式子使用配方法
$$\begin{aligned}
8x-x^2&=-(x^2-8x)\\
&=-(x^2-8x+16-16)\\
&=16-(x-4)^2
\end{aligned}$$
代入式子
$$\begin{align*}
\int\frac{dx}{\sqrt{8x-x^2}}&=\int\frac{dx}{\sqrt{16-(x-4)^2}}\\
&=\int\frac{dx/4}{\sqrt{1-(\frac{x-4}{4})^2}}\\
&=\int\frac{du}{\sqrt{1-u^2}}&&u=\frac{x-4}{4}\\
&=\sin^{-1}u+C\\
&=\sin^{-1}\frac{x-4}{4}+C
\end{align*}$$

例3 
