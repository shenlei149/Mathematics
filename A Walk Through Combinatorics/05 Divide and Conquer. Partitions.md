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

## Set Partitions
我们现在考虑球不一样但是盒子是一样的，也就是将集合$[n]$分配到$k$个非空的盒子中。

**Definition 5.5.** 集合$[n]$的分割(`partition`)是将每个元素唯一的分配到一个非空块(`block`)的集合。  
我们将集合$[n]$分配到$k$个非空的块中表示为$S(n,k)$，其称之为第二类斯特朗数(`Stirling numbers of the secondkind`)。  
如果$n<k$，那么$S(n,k)=0$。我们约定$S(0,0)=1$，下一章会解释为什么。

**Example 5.6.** $n\geq 1$时，$S(n,1) =S(n, n)=1$。$n\geq 2$时，$S(n,n-1)=\begin{pmatrix}n\\2\end{pmatrix}$，任选两个组成一块，其余每个元素自成一块。

**Example 5.7.** 集合$[4]$有七种分成两个非空块的分割：
$$\{1,2,3\}\{4\}\\\{1,2,4\}\{3\}\\\{1,3,4\}\{2\}\\\{2,3,4\}\{1\}\\\{1,2\}\{3,4\}\\\{1,3\}\{2,4\}\\\{1,4\}\{2,3\}$$
所以$S(4,2)=7$。

第一类斯特林数呢？第六章会讲解。  
有通项公式吗？第七章会给出一个包含求和记号的公式。

**Theorem 5.8.** 对于所有的正整数$k\leq n$，有
$$S(n,k)=S(n-1,k-1)+k\cdot S(n-1,k)$$
**Proof.** 如果第$n$个元素自成一块，那么剩下的问题就是将$[n-1]$分成$k-1$块，即右边的第一项；如果第$n$个元素混杂在$k$块中，那么先将$[n-1]$分成$k$块，即$S(n-1,k)$，任选一块，有$k$种选法。

如果将$n$个不同的球分到$k$个不同的盒子里面，共有$k!\cdot S(n,k)$种分法。

**Corollary 5.9.** 所有$[n]\to[k]$上的满射函数$f$的数量是$k!\cdot S(n,k)$  
**Proof.** 略。
