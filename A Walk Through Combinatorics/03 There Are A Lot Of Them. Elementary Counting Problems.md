## Permutations
**Definition 3.1.** 将$n$个不同对象排成一列，且每个对象只能使用一次，这称之为排列(`permutation`)。$n$个对象的所有排列的个数是$n\cdot(n-1)\cdot(n-2)\cdots 2\cdot 1$，这称之为n的阶乘(`factorial`)，用$n!$表示。

**Theorem 3.2.** 一个$n$个元素的集合的所有排列的个数是$n!$。

这里有个约定：$0!=1$。为什么不等于零呢？考虑两个房子，一间$m$个人，一间$n$个人，将两间房的人分别拍成一列，共有$m!n!$种排列。如果$n=0$呢？为了使$m!n!$在这种极端情况下也成立，我们不得不令$0!=1$。  
$n!$是一个重要的数，但是它有多大呢？斯特林公式(`Stirling's formula`)给出了近似值
$$n!\approx\sqrt{2\pi n}(\frac{n}{e})^n$$
符号$n!\approx z(n)$意味着$\lim_{n\to \infty}\frac{n!}{z(n)}=1$。

**Example 3.3.** 三种不同的颜色图一个三个水平条纹的棋子，要求颜色各不相同，多少种图法？  
**Solution.** 略。

