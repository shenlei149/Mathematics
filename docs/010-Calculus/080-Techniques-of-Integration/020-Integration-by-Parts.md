分部积分法可以简化形如下面的积分式子
$$\int u(x)v'(x)dx$$
当可以容易地对 $u(x)$ 反复微分，对 $v'(x)$ 反复积分时，这个方法很有用。积分
$$\int x\cos xdx,\int x^2e^xdx$$
就是这样类型的积分。因为 $u(x)=x,u(x)=x^2$ 很容易返回微分到零，并且可以很容易的对 $v'(x)=\cos x,v'(x)=e^x$ 反复积分。下面的积分式也可以用这个方法。
$$\int \ln xdx,\int e^x\cos xdx$$
因为第一个被积分式子可以写作 $(\ln x)(1)$，前者很容易微分，而且很容易对 $v'(x)=1$ 进行积分。第二个式子就更特殊了，乘积的两个子项都非常容易地进行微分和积分。

### 乘法法则的积分形式
如果 $u,v$ 是 $x$ 的可微函数，乘法法则如下
$$\frac{d}{dx}[u(x)v(x)]=u'(x)v(x)+u(x)v'(x)$$
两个积分得到
$$\int\frac{d}{dx}[u(x)v(x)]dx=\int u'(x)v(x)dx+\int u(x)v'(x)dx$$
调整项的位置得到
$$\int u(x)v'(x)dx=\int\frac{d}{dx}[u(x)v(x)]dx-\int u'(x)v(x)dx$$
所以分部积分公式是
$$\int u(x)v'(x)dx=u(x)v(x)-\int u'(x)v(x)dx$$
