### 切线和面积
如果函数 $f,g$ 在 $t$ 可微，那么参数化曲线 $f(t),g(t)$ 在 $t$ 处是可微的。在可微曲线上，$y$ 是 $x$ 的可微函数，根据链式法则 $dy/dt,dx/dt,dy/dx$ 的关系如下
$$\frac{dy}{dt}=\frac{dy}{dx}\frac{dx}{dt}$$
如果 $dx/dt\neq 0$，两边除以 $dx/dt$ 可以 $dy/dx$。

> $dy/dx$ 的参数公式
> 如果三个导数都存在，且 $dx/dt\neq 0$，那么
> $$\frac{dy}{dx}=\frac{dy/dt}{dx/dt}$$

如果参数方程定义 $y$ 是 $x$ 二阶可微函数，令 $dy/dx=y'$，可以计算 $d^2y/dx^2$
$$\frac{d^2y}{dx^2}=\frac{d}{dx}(y')=\frac{dy'/dt}{dx/dt}$$

> $d^2y/dx^2$ 的参数公式
> 如果方程 $x=f(t),y=g(t)$ 定义 $y$ 是 $x$ 二阶可微函数，在任意点处有 $dx/dt\neq 0$，且 $y'=dy/dx$，那么
> $$\frac{d^2y}{dx^2}=\frac{dy'/dt}{dx/dt}$$

例1 求曲线
$$x=\sec t,y=\tan t,-\frac{\pi}{2}<t<\frac{\pi}{2}$$
在点 $(\sqrt{2},1)$ 处的切线，此时 $t=\pi/4$。如下图所示。

![](020.010.png)

解：
