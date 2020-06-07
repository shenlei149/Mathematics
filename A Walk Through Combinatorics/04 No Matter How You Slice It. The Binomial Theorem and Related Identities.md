## The Binomial Theorem
**Theorem 4.1** [二项式定理(`Binomial Theorem`)] 对于所有非负整数$n$有
$$(x+y)^n=\sum_{k=0}^n\begin{pmatrix}
n\\k
\end{pmatrix}x^ky^{n-k}$$
**Proof.** 略。

**Theorem 4.2.** 对于所有正整数$n$，二项式系数$\begin{pmatrix}n\\k\end{pmatrix}$的交替和为$0$。
$$\sum_{k=0}^n(-1)^k\cdot\begin{pmatrix}
n\\k
\end{pmatrix}=0$$
**Proof.** 令$x=-1,y=1$即可。

**Theorem 4.3.** 对于所有非负整数$n$和$k$，
$$\begin{pmatrix}
n\\k
\end{pmatrix}+\begin{pmatrix}
n\\k+1
\end{pmatrix}=\begin{pmatrix}
n+1\\k+1
\end{pmatrix}$$
**Proof.** 略。

**Theorem 4.4.** 对于所有非负整数$n$，
$$2^n=\sum_{k=0}^n\begin{pmatrix}
n\\k
\end{pmatrix}$$
**Proof.** 左右两边都是$n$个元素的集合的子集个数。左边是直接计算；右边是得到$k$个元素的子集个数，再相加。  
**Proof 2.** 利用二项式定理，令$x=y=1$即可。

第一个方法是证明组合恒等式的经典方法：利用不同的方法来对同一些对象计数。

帕斯卡三角(`Pascal triangle`):  
![](0401.png)

**Theorem 4.5.** 对于所有非负整数$n$和$k$，
$$\begin{pmatrix}
k\\k
\end{pmatrix}+\begin{pmatrix}
k+1\\k
\end{pmatrix}+\begin{pmatrix}
k+2\\k
\end{pmatrix}+\cdots\begin{pmatrix}
n\\k
\end{pmatrix}=\begin{pmatrix}
n+1\\k+1
\end{pmatrix}$$
**Proof.** 右边是$n+1$个元素的集合的$k+1$个元素的子集的个数。左边也是计算子集的个数，但是是分成了$n-k+1$个部分，左边第一项是最大的元素是$k+1$的子集个数，第二项是最大元素是$k+2$的子集个数，$\begin{pmatrix}k+i\\k\end{pmatrix}$是$n+1$个元素的集合的最大值是$k+i+1$的$k+1$个元素的子集个数，其中$i\leq n-k$。  
这个定理也意味着我们从帕斯卡三角的第$k$行的最右的元素开始，然后往左下前进，到某个元素终止。路径上的元素之和等于终止元素的下一行右边那个元素。

**Theorem 4.6.** 对于所有非负整数$n$，
$$\sum_{k=1}^nk\begin{pmatrix}
n\\k
\end{pmatrix}=n2^{n-1}$$
**Proof.** 公式两边都是在从$n$个人中选择一个委员会，并选举一个主席。左边的思路是先选择$k$个人组成委员会，再从$k$个人中选择一个当选主席；右边的思路是先从$n$个人中选出一个主席，再从$n-1$个人中选出一些人和主席组成委员会。  
**Proof 2.** 利用二项式定理，令$y=1$
$$(x+1)^n=\sum_{k=0}^n\begin{pmatrix}
n\\k
\end{pmatrix}x^k$$
对$x$求导
$$n(x+1)^{n-1}=\sum_{k=1}^nk\begin{pmatrix}
n\\k
\end{pmatrix}x^{k-1}$$
再令$x=1$即可。

**Theorem 4.7.** [范德蒙恒等式(`Vandermonde's identity`)] 对所有正整数$n,m,k$，
$$\begin{pmatrix}
n+m\\k
\end{pmatrix}=\sum_{k=0}^n\begin{pmatrix}
n\\i
\end{pmatrix}\begin{pmatrix}
m\\k-i
\end{pmatrix}$$
**Proof.** 公式的左边是$n+m$个元素集合的有$k$个元素子集的个数。右边是分两步进行，先从前$n$个元素中选择$i$个，有$\begin{pmatrix}n\\i\end{pmatrix}$种不同的方式，再从后$m$个元素中选择$k-i$个，有$\begin{pmatrix}m\\k-i\end{pmatrix}$种不同的方式，最后对不同的$i$求和。

观察帕斯卡三角的每一行，都是先增加再减少，下面两个定理说明了这一点。

**Theorem 4.8.** 对于所有非负整数$k$和$n$，其中$k\leq\frac{n-1}{2}$，有
$$\begin{pmatrix}
n\\k
\end{pmatrix}\leq\begin{pmatrix}
n\\k+1
\end{pmatrix}$$
当且仅当$n=2k+1$时等号成立。  
**Proof.** 将不等式展开
$$\frac{n!}{k!(n-k)!}\leq\frac{n!}{(k+1)!(n-k-1)!}$$
化简
$$\frac{1}{n-k}\leq\frac{1}{k+1}$$
$$n-k\geq k+1$$
$$2k+1\leq n$$
$$k\leq\frac{n-1}{2}$$

**Corollary 4.9.** 对于所有正整数$k$和$n$，其中$k\geq\frac{n-1}{2}$，有
$$\begin{pmatrix}
n\\k
\end{pmatrix}\geq\begin{pmatrix}
n\\k+1
\end{pmatrix}$$
当且仅当$n=2k+1$时等号成立。  
**Proof.** 略。

一个序列先递增再递减，被称之为单峰(`unimodal`)序列。对于实数序列$a_0,a_2\cdots a_n$，存在一$m$，使得$a_0\leq a_1\leq\cdots\leq a_m$且$a_m\geq\cdots\geq a_n$。

## The Multinomial Theorem
**Example 4.10.** 求证
$$(x+y+z)^3=x^3+y^3+z^3+3x^2y+3x^2z+3y^2x+3y^2z+3z^2x+3z^2y+6xyz$$
**Proof** 略。

**Definition 4.11.** $n=\sum_{i=1}^k a_i$，其中$a_1,a_2,\cdots a_k$是非负整数
$$\begin{pmatrix}
n\\a_1,a_2,\cdots a_k
\end{pmatrix}=\frac{n!}{a_1!\cdot a_2!\cdots a_k!}$$
$\begin{pmatrix}n\\a_1,a_2,\cdots a_k\end{pmatrix}$称之为多项式系数(`multinomial coefficients`)。

**Theorem 4.12** [多项式理论(`Multinomial theorem`)] 对所有非负整数$n$和$k$，有
$$(x_1+x_2+\cdots +x_k)^n=\sum_{a_1,a_2,\cdots a_k} \begin{pmatrix}
n\\a_1,a_2,\cdots a_k
\end{pmatrix} x_1^{a_1}x_2^{a_2}\cdots x_k^{a_k}$$
其中$k$元非负整数$a_1,a_2,\cdots a_k$满足$n=\sum_{i=1}^k a_i$。  
**Proof.** Hint: Theorem 3.5

**Theorem 4.13.** 对于所有非负整数$n$和$a_1,a_2,\cdots,a_k$，其中$n=\sum_{i=1}^k a_i$，有
$$\begin{pmatrix}
n\\a_1,a_2,\cdots,a_k
\end{pmatrix}=\begin{pmatrix}
n\\a_1
\end{pmatrix}\begin{pmatrix}
n-a_1\\a_2
\end{pmatrix}\cdots\begin{pmatrix}
n-a_1-a_2-\cdots -a_i\\a_{i+1}
\end{pmatrix}\cdots\begin{pmatrix}
n-a_1-a_2-\cdots - a_{k-1}\\a_k
\end{pmatrix}$$
**Proof** 略。

## When the Exponent Is Not a Positive Integer
当$m$不是正整数时，$(1 +x)^m$是多少呢？首先给出$m$是任意实数时二项式系数$\begin{pmatrix}m\\k\end{pmatrix}$的定义。  
**Definition 4.14.** 对于任意实数$m$和非负整数$k$，$\begin{pmatrix} m\\0 \end{pmatrix}=1$，$k>0$时有
$$\begin{pmatrix}
m\\k
\end{pmatrix}=\frac{m(m-1)\cdots(m-k+1)}{k!}$$
这个定义扩大了$m$的域。

利用$(1+x)^m$在$x=0$附近的泰勒级数(`Taylor series`)，其$n$阶导为$\frac{m!}{(m-n)!}(1+x)^{m-n}$，可以得到下面定理：  
**Theorem 4.15** $m$为任意实数，有
$$(1+x)^m=\sum_{n\geq 0}\begin{pmatrix}
m\\n
\end{pmatrix}x^n$$
如果$m$不是整数，那么$(1+x)^m$是无穷级数。

**Example 4.16.** 求$\sqrt{1-4x}$的幂级数。  
**Solution.** 根据定理4.15，
$$\sqrt{1-4x}=(1-4x)^{1/2}=\sum_{n\geq 0}\begin{pmatrix}
1/2\\n
\end{pmatrix}(-4x)^n$$
为了简化这个表达式，我们需要简化$\begin{pmatrix}1/2\\n\end{pmatrix}$。$\begin{pmatrix}1/2\\0\end{pmatrix}=1$，$\begin{pmatrix}1/2\\1\end{pmatrix}=1/2$，当$n\geq 2$时，
$$\begin{pmatrix}
1/2\\n
\end{pmatrix}=\frac{\frac{1}{2}\cdot\frac{-1}{2}\cdot\frac{-3}{2}\cdots\frac{-2n+3}{2}}{n!}=(-1)^{n-1}\frac{(2n-3)!!}{2^n\cdot n!}$$
$(2n-3)!!$表示从$1$到$2n-3$所有奇数之积，称之为$2n-3$的半阶乘或双阶乘(`semifactorial` or `double factorial`)。  
代入上式得到
$$\sqrt{1-4x}=1-2x-\sum_{n\geq 2}\frac{2^n\cdot(2n-3)!!}{n!}x^n$$
对$\frac{2^n\cdot(2n-3)!!}{n!}$的分子分母同乘$(n-1)!$，那么$2^{n-1}(n-1)!$就等于从$2$到$2n-2$所有偶数的乘积。所以
$$\frac{2^n\cdot(2n-3)!!}{n!}=2\frac{(2n-2)!}{n!(n-1)!}$$
$$\sqrt{1-4x}=1-2x-\frac{2}{n}\sum_{n\geq 2}\begin{pmatrix}
2n-2\\n-1
\end{pmatrix}x^n$$

## Exercises
TODO 2

TODO 5

(7) 有$n$个石头，将其分成两堆，令$p_1$是两堆石头数量的乘积，对每堆石头做重复的操作，令$p_2$是第二次分成两堆石头数量的乘积，以此类推，直至每堆石头都只有一个为止，显然这需要$n-1$步。求$p_1+p_2+\cdots+p_{n-1}$的最大值和最小值。  
**Solution.** 考虑极端情况，每次都取出一个石头单独一堆，那么$p_1=n-1, p_2=n-2,\cdots,p_{n-1}=1$，所以
$$p_1+p_2+\cdots+p_{n-1}=\frac{n(n-1)}{2}=\begin{pmatrix}
n\\2
\end{pmatrix}$$
下面我们证明当$n\geq 2$时，其和都是$\begin{pmatrix}n\\2\end{pmatrix}$。$n=2$时明显成立，假设小于$n$时该命题都成立，现在考察$n$，我们将其分成任意$k$和$n-k$两堆，其乘积是$k(n-k)$，那么总和为
$$k(n-k)+\begin{pmatrix}
k\\2
\end{pmatrix}+\begin{pmatrix}
n-k\\2
\end{pmatrix}=\frac{n(n-1)}{2}=\begin{pmatrix}
n\\2
\end{pmatrix}$$
