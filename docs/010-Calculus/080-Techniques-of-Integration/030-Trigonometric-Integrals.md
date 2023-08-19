三角函数的积分涉及六个基本三角函数的代数运算。一般地，我们通过恒等变形，将被积分的式子转化成更容易积分的式子。

### 正弦和余弦的幂的积
我们从形如
$$\int\sin^m x\cos^n xdx$$
的积分开始，其中 $m,n$ 是非负整数。根据 $m,n$ 的奇偶性可以分成三种情况。

第一种情况，$m$ 是奇数，可以将 $m$ 写作 $2k+1$，结合恒等式 $\sin^2 x=1-\cos^2 x$ 可以得到
$$\sin^m x=\sin^{2k+1} x=(\sin^2 x)^k\sin x=(1-\cos^2 x)^k\sin x$$
将 $\sin x$ 和 $dx$ 结合得到 $-d(\cos x)$。

第二种情况，$n$ 是奇数，和上面类似的推导可以得到
$$\cos^n x=\cos^{2k+1} x=(\cos^2 x)^k\cos x=(1-\sin^2 x)^k\cos x$$
将 $\cos x$ 和 $dx$ 结合得到 $d(\sin x)$。

第三种情况，$m,n$ 都是偶数，使用
$$\sin^2 x=\frac{1-\cos 2x}{2},\cos^2 x=\frac{1+\cos 2x}{2}$$
替换被积分的式子，得到用 $\cos 2x$ 更低次幂的式子。

例1 求
$$\int\sin^3 x\cos^2 xdx$$
解：这个式子是第一种情况。
$$\begin{aligned}
\int\sin^3 x\cos^2 xdx&=\int\sin^2 x\cos^2 x\sin xdx\\
&=\int(1-\cos^2 x)(\cos^2 x)(-d(\cos x))\\
&=\int(1-u^2)(u^2)(-du)\\
&=\int(u^4-u^2)du\\
&=\frac{u^5}{5}-\frac{u^3}{3}+C\\
&=\frac{\cos^5 x}{5}-\frac{\cos^3 x}{3}+C
\end{aligned}$$

例2 求
$$\int\cos^5 xdx$$
解：这个例子是第二种情况。
$$\begin{aligned}
\int\cos^5 xdx&=\int\cos^4 x\cos xdx\\
&=\int(1-\sin^2 x)^2d(\sin x)\\
&=\int(1-u^2)^2du\\
&=\int(1-2u^2+u^4)du\\
&=u-\frac{2u^3}{3}+\frac{u^5}{5}+C\\
&=\sin x-\frac{2\sin^3 x}{3}+\frac{\sin^5 x}{5}+C
\end{aligned}$$

例3 求
$$\int\sin^2 x\cos^4 xdx$$
解：这个第三种情况。
$$\begin{aligned}
\int\sin^2 x\cos^4 xdx&=\int(\frac{1-\cos 2x}{2})(\frac{1+\cos 2x}{2})^2dx\\
&=\frac{1}{8}\int(1-\cos 2x)(1+2\cos 2x+\cos^2 2x)dx\\
&=\frac{1}{8}\int(1+\cos 2x-\cos^2 2x-\cos^3 2x)\\
&=\frac{1}{8}[x+\frac{1}{2}\sin 2x-\int(cos^2 2x+\cos^3 2x)dx]
\end{aligned}$$
这里涉及 $\cos^2 2x$，
$$\int\cos^2 2xdx=\frac{1}{2}\int(1+\cos 4x)dx=\frac{1}{2}(x+\frac{1}{4}\sin 4x)$$
对于 $\cos^3 2x$，这是第二种情况，所以
$$\begin{aligned}
\int\cos^3 2xdx&=\int(1-\sin^2 2x)\cos 2xdx\\
&=\frac{1}{2}\int(1-u^2)du\\
&=\frac{1}{2}(\sin 2x-\frac{\sin^3 2x}{3})
\end{aligned}$$
代入原始的式子可以得到
$$\int\sin^2 x\cos^4 xdx=\frac{1}{16}(x-\frac{1}{4}\sin 4x+\frac{1}{3}\sin^3 2x)+C$$
