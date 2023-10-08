### Linear Congruences
形式如下的式子，
$$ax\equiv b(\operatorname{mod}m)$$
其中 $a,b$ 是整数，$m$ 是正整数，$x$ 是变量，被称为线性同余。

如何找到满足这个同余式子的 $x$ 的值呢？一个办法是使用称为 $a$ 模 $m$ 的逆（`inverse`）$\bar{a}$，其满足 $a\bar{a}\equiv 1(\operatorname{mod}m)$。

**定理 1**
如果 $a,m$ 是互斥的整数且 $m>1$，那么 $a$ 模 $m$ 的逆存在，且逆模 $m$ 是唯一的。也就是说，小于 $m$ 的正整数 $\bar{a}$ 是唯一的，其他的逆与该值模 $m$ 同余。

证明：根据 4.3 节定理 6，因为 $\gcd(a,m)=1$，那么存在 $s,t$ 使得
$$sa+tm=1$$
这蕴涵着
$$sa+tm\equiv 1(\operatorname{mod}m)$$
因为
$$tm\equiv 0(\operatorname{mod}m)$$
所以
$$sa\equiv 1(\operatorname{mod}m)$$
这里的 $s$ 即 $a$ 模 $m$ 的逆。

下面证明唯一性。假定还有一个 $b<m$ 的正整数也满足 $ab\equiv 1(\operatorname{mod}m)$，且 $b\neq s$，那么
$$sa\equiv ba(\operatorname{mod}m)$$
根据 4.3 节定理 7，有
$$s\equiv b(\operatorname{mod}m)$$
与假设矛盾。

如果 $m$ 很小，测试小于 $m$ 的正整数是否满足逆的属性即可。比如找 3 模 7 的逆，尝试 $j\cdot 3, j=1,2,3,4,5,6$ 即可。一个便捷方法是当发现 $2\cdot 3\equiv -1(\operatorname{mod}7)$ 时，可知 $-2\cdot 3\equiv 1(\operatorname{mod}7)$，那么 $-2$ 是逆，因此 5 也是 3 模 7 的逆。

通用方法是根据 $sa+tm=1$，利用 4.3 节的两种不同方法求 $s$ 即可。

有了 $\bar{a}$ 之后，求解 $ax\equiv b(\operatorname{mod}m)$ 就很简单了：两边同乘 $\bar{a}$ 即可。
