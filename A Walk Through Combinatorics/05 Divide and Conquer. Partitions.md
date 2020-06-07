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

