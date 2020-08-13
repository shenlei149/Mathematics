## Enumerating The Elements of Intersecting Sets
**Example 7.1.** 有14个同学踢足球17个同学打篮球，其中4个同学参与了两者。问至少玩其中一种运动的同学有多少个？  
**Solution.** 略。

**Example 7.2.** 有14个同学踢足球17个同学打篮球18个同学玩曲棍球，其中4个同学同时玩足球和篮球，3个同学同时玩足球和曲棍球，5个同学同时玩篮球和曲棍球，1个同学三者都参与了。问至少玩其中一种运动的同学有多少个？  
**Solution.** 略。

**Theorem 7.3** [(`Sieve Formula`)或容斥原理(`Principle of Inclusion-Exclusion`)]. $A_1,A_2,\cdots,A_n$是有限集合，有
$$|A_1\cup A_2\cup\cdots\cup A_n|=\sum_{j=1}^n(-1)^{j-1}\sum_{i_1,i_2,\cdots,i_j}|A_{i_1}\cap A_{i_2}\cap\cdots\cap A_{i_j}|$$
其中$\{{i_1,i_2,\cdots,i_j}\}$是所有$[n]$的$j$个元素子集。  
**Proof.** 考虑任意元素$x\in A_1\cup A_2\cup\cdots\cup A_n$，显然，左边只计算了一次$x$。令$S\subseteq [n]$是索引的集合，使得$x\in A_i$当且仅当$i\in S$，$s=|S|$。由于仅当$i\in S$时有$x\in A_i$，那么$A_{i_1}\cap A_{i_2}\cap\cdots\cap A_{i_t}$不包含$x$，除非$(i_1,i_2,\cdots,i_t)\subseteq S$。所以计算$x$在右边出现的次数时，只需要考虑$A_i$被$S$索引的时候；也就是说，这些交集都包含$x$。比如$j=2$时，从$S$任取两个值$p,q$，对应的$A_p,A_q$都是包含$x$的。那么右边计算$x$的次数是
$$s-\begin{pmatrix}
s\\2
\end{pmatrix}+\begin{pmatrix}
s\\3
\end{pmatrix}-\cdots +(-1)^{s-1}\begin{pmatrix}
s\\s
\end{pmatrix}$$
根据二项式定理
$$(1-1)^s=0=1-s+\begin{pmatrix}
s\\2
\end{pmatrix}-\begin{pmatrix}
s\\3
\end{pmatrix}+\cdots (-1)^{s-1}\begin{pmatrix}
s\\s
\end{pmatrix}$$
所以右边也只计算了$x$一次。

## Applications of the Sieve Formula
**Example 7.4.** 一个派对有$n$个客人，他们的帽子放在衣帽间。然后停电了，客人随机拿了一个帽子，他们发现所有人都拿到别人的帽子。求有多少种这种情况发生呢？  
这就是错位排列(`derangement`)。$[n]$的错位排列就是其没有不动点(`fixed point`)，没有元素$i$在第$i$个位置上。  
**Solution.** 全排列减去至少有一个不动点就是要求的数。  
用$A_i$表示元素$i$在位置$i$上。Theorem 7.3告诉了计数的方法。  
$A_1$是多少呢？元素1在位置1上，其余$n-1$个元素可以自由排列，所以$|A_1|=(n-1)!$，类似的，$|A_2|=(n-1)!$，$|A_i|=(n-1)!$，那么公式右边的第一项是$(n-1)!\cdot n=n!$。  
接下来考察$|A_i\cap A_j|$。两个元素是不动点，那么有$(n-2)!$中排列方式，从$n$个元素里面选择两个，所以第二项是
$$-\begin{pmatrix}
n\\2
\end{pmatrix}(n-2)!=-\frac{n!}{2}$$
依此类推，第$i$项是
$$(-1)^{i-1}\begin{pmatrix}
n\\i
\end{pmatrix}(n-i)!=(-1)^{i-1}\frac{n!}{i!}$$
根据Theorem 7.3
$$\begin{aligned}
|A_1\cup A_2\cup\cdots\cup A_n|&=\sum_{j=1}^n(-1)^{j-1}\sum_{i_1,i_2,\cdots,i_j}|A_{i_1}\cap A_{i_2}\cap\cdots\cap A_{i_j}|\\
&=n!-\frac{n!}{2}+\frac{n!}{3!}-\cdots+(-1)^{n-1}\frac{n!}{n!}\\
&=\sum_{i=1}^n(-1)^{i-1}\frac{n!}{i!}
\end{aligned}$$
使用全排列$n!$减去上式就得到没有不动点的个数$D(n)$
$$D(n)=\sum_{i=0}^n(-1)^i\frac{n!}{i!}$$
和$n!$有什么关系呢？
$$\frac{D(n)}{n!}=\sum_{i=0}^n\frac{(-1)^i}{i!}$$
当$n$趋于无穷大的时候，由泰勒级数
$$e^x=\sum_{n=0}^\infty \frac{x^n}{n!}$$
得到右边收敛于$1/e$。
