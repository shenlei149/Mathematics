### $x\to\plusmn\infty$时的极限
无穷符号$\infty$不表示任何一个实数。比如函数$f(x)=1/x,x\neq 0$的定义如下图。当$x$增大时，$1/x$减小。当$x$是负数且数值增加时类似。也就是说当$x\to\infty$或$x\to 0\infty$时，$f(x)=1/x$的极限是0。或者说0是$f(x)=1/x$在无穷处和负无穷处的极限。  
![](050.010.png)

**定义**  
如果对于所有$\epsilon>0$，都有对应的$M$使得对于$f$定义域所有的$x$都有
$$|f(x)-L|<\epsilon, \text{ whenever } x>M$$
那么我们说$x$趋于无穷时，$f(x)$的极限是$L$，写作
$$\lim_{x\to\infty}f(x)=L$$
如果对于所有$\epsilon>0$，都有对应的$N$使得对于$f$定义域所有的$x$都有
$$|f(x)-L|<\epsilon, \text{ whenever } x<N$$
那么我们说$x$趋于负无穷时，$f(x)$的极限是$L$，写作
$$\lim_{x\to -\infty}f(x)=L$$

直观地，如果$\lim_{x\to\infty}f(x)=L$，那么当$x$移动的离原点越来越远，$f(x)$无限接近$L$。类似地，$\lim_{x\to-\infty}f(x)=L$，那么当$x$沿着负半轴移动的越来越远，$f(x)$无限接近$L$。  
计算$x\to\infty$或$x\to-\infty$的极限的策略和2.2节类似，那一节中我们先找到$y=x,y=k$的极限，然后应用定理1进行拓展。这里我们也要先找到$y=1/x,y=k$的极限。  
$$\lim_{x\to\plusmn\infty}k=k,\lim_{x\to\plusmn\infty}\frac{1}{x}=0\tag{1}$$

例1 证明  
（a）$\lim_{x\to\infty}\frac{1}{x}=0$  
（b）$\lim_{x\to-\infty}\frac{1}{x}=0$  
证明：  
（a）令$\epsilon>0$，我们必须找到一个$M$使得
$$|\frac{1}{x}-0|=|\frac{1}{x}|<\epsilon, \text{ whenever } x>M$$
那么$M=1/\epsilon$或者任意更大的正数。如下图所示：  
![](050.020.png)  
（b）令$\epsilon>0$，我们必须找到一个$N$使得
$$\bigg|\frac{1}{x}-0\bigg|=\bigg|\frac{1}{x}\bigg|<\epsilon, \text{ whenever } x<N$$
那么$N=-1/\epsilon$或者任意小于$1-\epsilon$的负数。

**定理8** 定理1的所有法则对$x\to\infty,x\to-\infty$时同样适用。

例2
$$\begin{aligned}

\end{aligned}$$
