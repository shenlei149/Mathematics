### 正弦函数的导数
$x$弧度表示，下面计算$f(x)=\sin x$的导数。正弦函数的和公式是
$$\sin(x+h)=\sin x\cos h+\cos x\sin h$$
那么
$$\begin{aligned}
f'(x)&=\lim_{h\to 0}\frac{f(x+h)-f(x)}{h}\\
&=\lim_{h\to 0}\frac{\sin(x+h)-\sin x}{h}\\
&=\lim_{h\to 0}\frac{\sin x\cos h+\cos x\sin h-\sin x}{h}\\
&=\lim_{h\to 0}\frac{\sin x(\cos h-1)+\cos x\sin h}{h}\\
&=\lim_{h\to 0}(\sin x\frac{\cos h-1}{h})+\lim_{h\to 0}(\cos x\frac{\sin h}{h})\\
&=\sin x\cdot \lim_{h\to 0}\frac{\cos h-1}{h}+\cos x\cdot\lim_{h\to 0}\frac{\sin h}{h}\\
&=\sin x\cdot 0+\cos x\cdot 1\\
&=\cos x
\end{aligned}$$
其中倒数第三步到倒数第二步利用了2.4节例5 和定理7 的结论。

**正弦函数的导数是余弦函数**
$$\frac{d}{dx}\sin x=\cos x$$

例1 求下面函数的导数  
（a）$y=x^2-\sin x$  
（b）$y=e^x\sin x$  
（c）$y=\frac{\sin x}{x}$  
解：  
（a）$y'=2x-\cos x$  
（b）$y=e^x\sin x+e^x\cos x=e^x(\sin x+\cos x)$  
（c）$y=\frac{\sin x}{x}=\frac{\cos x\cdot x-\sin x}{x^2}=\frac{x\cos x-\sin x}{x^2}$  

### 余弦函数的导数
余弦函数的和公式是
$$\cos(x+h)=\cos x\cos h-\sin x\sin h$$
那么
$$\begin{aligned}
\frac{d}{dx}\cos x&=\lim_{h\to 0}\frac{\cos(x+h)-\cos x}{h}\\
&=\lim_{h\to 0}\frac{\cos x\cos h-\sin x\sin h-\cos x}{h}\\
&=\lim_{h\to 0}\frac{\cos x(\cos h-1)-\sin x\sin h}{h}\\
&=\lim_{h\to 0}(\cos x\frac{\cos h-1}{h})-\lim_{h\to 0}(\sin x\frac{\sin h}{h})\\
&=\cos x\lim_{h\to 0}\frac{\cos h-1}{h}-\sin x\lim_{h\to 0}\frac{\sin h}{h}\\
&=\cos x\cdot 0-\sin x\cdot 1\\
&=-\sin x
\end{aligned}$$

**余弦函数的导数是负的正弦函数**
$$\frac{d}{dx}\cos x=-\sin x$$

下图显示了$y=\cos x$曲线上各点切线的斜率。  
![](050.010.png)

例2 求下面函数的导数  
（a）$y=5e^x+\cos x$  
（b）$y=\sin x\cos x$  
（c）$y=\frac{\cos x}{1-\sin x}$  
解：  
（a）$y=5e^x+-\sin x$  
（b）$y=\cos x\cos x-\sin x\sin x=\cos^2 x-\sin^2 x$  
（c）$y=\frac{-\sin x(1-\sin x)-\cos x(-\cos x)}{(1-\sin x)^2}=\frac{-\sin x+\sin^2+\cos^x}{(1-\sin x)^2}=\frac{1-\sin x}{(1-\sin x)^2}=\frac{1}{1-\sin x}$  

### 简谐运动
简谐运动（`simple harmonic motion`）是在没有其他外力的情况下重物挂在弹簧的一端上下运动的模型。运动是周期性重复的，用三角函数表示。

例3 如下图所示，一个重物挂在弹簧一端，当$t=0$时弹簧延长了五个单位长度，然后上下运动，任意时刻的位置是
$$s=5\cos t$$
那么任意时刻的速度和加速度分别是多少？  
![](050.020.png)  
解：位移
$$s=5\cos t$$
速度
$$v=\frac{ds}{dt}=-5\sin t$$
加速度
$$a=\frac{dv}{dt}=-5\cos t$$
从这个问题中，我们可以知道
1. 随着时间的流逝，重物在$s=-5$和$s=5$之间上下运动。运动的振幅是5。周期是余弦函数的周期$2\pi$。
2. 当$\cos t=0$时，速度$v=-5\sin t$达到最大值5。如下图所示。
   ![](050.030.png)
3. 重物受到弹簧和重力的作用。
