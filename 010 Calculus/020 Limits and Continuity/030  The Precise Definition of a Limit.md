现在我们学习极限的定义。对于严格的定义而言，避免使用任意接近这种描述性的语言。  

例1 思考$y=2x-1$在$x=4$附近的情况。直觉上有$\lim_{x\to 4}f(x)=7$。考虑$x=4$附近，$x$是多么靠近4使得$y=2x-1$和7的差距是小于两个单位长度？  
解：问题本质就是使得$|y-7|<2$？
$$|2x-1-7|=|2x-8|<2$$
那么
$$\begin{aligned}
|2x-8|&<2\\
-2&<2x-8&<2\\
3&<x&<5\\
-1&<x-4&<1
\end{aligned}$$
$x$在4附近一个单位长度的范围使得$y$在7附近两个单位长度以内。如下图所示  
![](030.010.png)

上面这个例子给了一个示例，$x$必须多么接近$c$才能保证$f(x)$在极限值$L$附近的指定区间。为了证明$x\to c$时$f(x)$的极限是$L$，我们必须能够证明$f(x)$和$L$之间的距离可以小于任意指定的误差，不管这个误差多小，总是可以通过$x$接近$c$来做到。为了描述任意指定的误差，引入两个常量，用$\delta$和$\epsilon$。这两个量通常用于表述很小的变化。

### 极限的定义
只要$x$位于距离$c$$\delta$长度附近，那么我们可以说$f(x)$位于$L$附近的区间$L-(1/10),L+(1/10))$。如下图所示：  
![](030.020.png)  
但是这不足够说明极限，因为随着$x$移向$c$，没有谁能保证始终$f(x)$位于$L$附近的区间$L-(1/10),L+(1/10))$并趋于$L$，有可能跳到其他值。我们可以把错误区间变小，比如$1/100,1/1000$，甚至是$1/100000$。每一次，我们都能在$c$附近找到一个新的区间使得$f(x)$满足这个误差。  
下图解释了整个过程。可以想象一个怀疑者和一个学者在辩论。怀疑者给出$\epsilon$区间以挑战极限是否存在，学者总是能在$c$附近找到一个区间$\delta$确保函数值都在$L$附近$\epsilon$的区间。  
![](030.041.png)  
![](030.042.png)  
![](030.043.png)  
如果停止这个过程呢？我们通过证明对于每一个错误容忍区间$\epsilon$，我们总有一个匹配的$\delta$区间使得$x$充分接近$c$时$f(x)$的值是在$L\plusmn \epsilon$这个区间内的。如下图所示：  
![](030.030.png)

**定义** $f(x)$在$c$附近的开区间有定义，除了$c$点外。如果对于每一个$\epsilon>0$都有一个相应的$\delta>0$使得
$$|f(x)-L|<\epsilon \text{ whenever } 0<|x-c|<\delta$$
那么我们称$x$趋于$c$时$f(x)$的极限是$L$，写作
$$\lim_{x\to c}f(x)=L$$

### 示例：定义的应用
函数极限的定义并没有告诉我们如何计算极限，而是能够让我们验证猜想是否正确。下面的例子将说明这一点。不过定义的真实目的不是这个，而是为了证明诸如上一节中出现的定理而简化极限的计算。

例2 证明
$$\lim_{x\to 1}(5x-3)=2$$
证明：令$c=1,f(x)=5x-3,L-2$。对于任意给定的$\epsilon>0$，我们需要找到一个合适的$\delta>0$，$x$在区间
$$0<|x-1|<\delta$$
那么$f(x)$在$L$附近区间满足
$$|f(x)-2|<\epsilon$$
我们代入$f(x)$到包含$\epsilon$的不等式来计算$\delta$
$$\begin{aligned}
|(5x-3)-2|=&|5x-5|&<\epsilon\\
&5|x-1|&<\epsilon\\
&|x-1|&<\epsilon
\end{aligned}$$
我们可以取$\delta=\epsilon/5$（如下图）。如果$0<|x-1|<\delta=\epsilon/5$那么
$$\begin{aligned}|(5x-3)-2|&=|5x-5|\\&=5|x-1|&\\&<5(\epsilon/5)=\epsilon\end{aligned}$$
这就证明了$\lim_{x\to 1}(5x-3)=2$。  
![](030.050.png)  
$\delta=\epsilon/5$不是唯一使得$0<|x-1|<\delta$蕴涵$|5x-5|<\epsilon$。任意更小的$\delta$都是可以的。定义只不要求求最佳的$\delta$而只要有一个即可。

例3 证明2.2节的两个公式  
（a）$\lim_{x\to c} x = c$  
（b）$\lim_{x\to c} k = k$  
解：  
（a）令$\epsilon>0$，我们需要找到$\delta>0$有
$$|x-c|<\epsilon \text{ whenever } 0<|x-c|<\delta$$
那么取$\delta=\epsilon$或者更小的值即可。如下图所示  
![](030.060.png)  
（b）令$\epsilon>0$，我们需要找到$\delta>0$有
$$|k-k|<\epsilon \text{ whenever } 0<|x-c|<\delta$$
由于$k-k=0$，任意的整数$\delta$都满足。如下图所示：  
![](030.070.png)

### 给定$\epsilon$代码法计算$\delta$
上面两个例子中，$\epsilon$总是以$L$为中心对称，$\delta$总是以$c$为中心对称。如果不对称的话，我们取$\delta$为距离$c$更近的端点。

例4 对于极限$\lim_{x\to 5}\sqrt{x-1}=2$，计算$\delta>0$使得$\epsilon=1$，即找到一个$\delta>0$，使得
$$|\sqrt{x-1}-2|<1 \text{ whenever } 0<|x-5|<\delta$$
解：解不等式$|\sqrt{x-1}-2|<1$，来寻找包含$x=5$的区间，使得除了$x\neq 5$之外的$x$都满足不等式。
$$|\sqrt{x-1}-2|<1$$
$$-1<\sqrt{x-1}-2<1$$
$$1<\sqrt{x-1}<3$$
$$1<x-1<9$$
$$2<x<10$$
找一个$\delta$满足$5-\delta<x<5+\delta$，5距离2比较近，所以取距离2的长度（如下图），即$\delta=3$或者更小的值  
![](030.080.png)
那么
$$|\sqrt{x-1}-2|<1 \text{ whenever } 0<|x-5|<3$$
![](030.090.png)

给定$f,L,c,\epsilon>0$，如何计算$\delta$  
计算$\delta>0$使得
$$|f(x)-L|<\epsilon \text{ whenever } 0<|x-c|<\delta$$
的过程分为以下两步：
1. 解不等式$|f(x)-L|<\epsilon$找到一个开区间$(a,b)$，这个区间包含$c$，且所有$x\neq c$都能使不等式成立。不管$x=c$是否能使得不等式成立不影响。
2. 找一个$\delta>0$的开区间$(c-\delta,c+\delta)$，以$c$为中心，且在开区间$(a, b)$之内。那么在这个$\delta$区间内所有$x\neq c$都满足$|f(x)-L|<\epsilon$。

例5 证明当
$$f(x)=\begin{cases}
x^2,&&x\neq 2\\
1,&&x=2
\end{cases}$$
时，$\lim_{x\to 2}f(x)=4$。  
解：我们的任务是对于任意给定的$\epsilon>0$都存在$\delta$使得
$$|f(x)-4|<\epsilon \text{ whenever } 0<|x-2|<\delta$$
首先解不等式$|f(x)-4|<\epsilon,x\neq 2$，已知$f(x)=x^2,x\neq c=2$，那么就是要求解$|x^2-4|<\epsilon$：
$$|x^2-4|<\epsilon$$
$$-\epsilon<x^2-4<\epsilon$$
$$4-\epsilon+<x^2<4+\epsilon$$
$$\sqrt{4-\epsilon}+<|x|<\sqrt{4+\epsilon}$$
$$\sqrt{4-\epsilon}+<x<\sqrt{4+\epsilon}$$
上面求解过程假设$\epsilon<4$。
对于所有在区间$(\sqrt{4-\epsilon},\sqrt{4+\epsilon})$的$x\neq 2$，都满足不等式$|f(x)-4|<\epsilon$，如下图所示：  
![](030.100.png)  
找一个$\delta>0$使得以2为中心的开区间$(2-\delta,2+\delta)$在$(\sqrt{4-\epsilon},\sqrt{4+\epsilon})$区间内。  
寻找一个距离较短的端点，即$\delta=\min\{2-\sqrt{4-\epsilon}, \sqrt{4+\epsilon}+2\}$。  
如果$\epsilon\geq 4$呢？那么区间是$(0, \sqrt{4+\epsilon})$，那么$\delta=\min\{2,\sqrt{4+\epsilon}-2\}=2$。

### 使用定义证明定理
