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
