## Compositions
将20个一模一样的小球分给四个小朋友，有多少种分发呢？顺序很重要，比如$1 + 6 + 8 + 5$和$6 + 1 + 8 + 5$是两种，因为前者第一个小朋友有1个球而后者第一个小朋友有6个！

**Definition 5.1.** 一个序列$(a_1,a_2,\cdots,a_k)$，对于所有的$i$，$a_i\geq0$，满足$(a_1+a_2+\cdots+a_k)=n$，称之为$n$的弱composition(`weak composition`)。如果$a_i>0$，则称之为$n$的composition。  
> 不确定composition对应的中文翻译，故用英文代替。

**Theorem 5.2.** 对于正整数$n$和$k$，分为$k$部分的弱composition的数量是
$$\begin{pmatrix}
n+k-1\\k-1
\end{pmatrix}=\begin{pmatrix}
n+k-1\\n
\end{pmatrix}$$
**Proof.** 该问题其实就是将$n$个球放到$k$个盒子中，等价于用$k-1$个隔板将$n$个球分开。将$n$个球和$k-1$个隔板拍成一行，**Theorem 3.5**告诉我们共有
$$\frac{(n+k-1)!}{n!(k-1)!}$$
种不同的排列方式。

如果要求每个小孩至少一个呢？先每人分一个，然后问题就转化为了已知问题。  
**Corollary 5.3.** 对于正整数$n$和$k$，分为$k$部分的composition的数量是
$$\begin{pmatrix}
n-1\\k-1
\end{pmatrix}$$

将$n$分成任意多的部分，那么所有的composition数是多少呢？明显地，每个部分不能是0个，也就是说不是弱composition，因为如果可以为0，那么个数就是无穷多，因为可以向每个composition $C$构成一个新的composition。  
**Corollary 5.4** 对于正整数$n$，其所有composition的个数是$2^{n-1}$。  
**Proof.** 任意部分从1开始一直到$n$，所以
$$\sum_{i=1}^n\begin{pmatrix}
n-1\\i-1
\end{pmatrix}=\sum_{i=0}^{n-1}\begin{pmatrix}
n-1\\i
\end{pmatrix}=2^{n-1}$$
**Proof 2.** 使用递归法来证明。$n=1$时，只有一种组合方式。假设$n$时命题成立，我们考虑$n+1$时即可。对于$n$的每个composition$C$，我们将多出来的一个1分两类处理。1）加到$C$的第一个值上，那么有$2^{n-1}$个，2）放到$C$的第一个值的前面，和1）里面的肯定不同，因为1）里面第一个值至少为2，又有$2^{n-1}$个，共计$2^{n}$个不同的composition。
