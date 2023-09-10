### 积分表
[这里](/Formula/A-Brief-Table-of-Integrals.md)给了一个积分表。其中 $a,b,c,m,n$ 是常数，通常可以是任意实数而不必只是整数。极偶尔的对它们有所限制，比如公式 21 中 $n\neq -1$，公式 27 中 $n\neq -2$。

这些常数要使得公式有意义，分母不能为零，根号下的式子必须非负等。比如公式 24 隐含了 $a\neq 0$，公式 29a 和 29b 隐含了 $b>0$。

例1 求
$$\int x(2x+5)^{-1}dx$$
解：利用公式 24
$$\int x(ax+b)^{-1}dx=\frac{x}{a}-\frac{b}{a^2}\ln|ax+b|+C$$
代入 $a=2,b=5$ 得到
$$\int x(2x+5)^{-1}dx=\frac{x}{2}-\frac{5}{4}\ln|2x+5|+C$$

例2 求
$$\int\frac{dx}{x\sqrt{2x-4}}$$
解：利用公式 29b
$$\int\frac{dx}{x\sqrt{ax-b}}=\frac{2}{\sqrt{b}}\tan^{-1}\sqrt{\frac{ax-b}{b}}+C$$
代入 $a=2,b=4$ 得到
$$\int\frac{dx}{x\sqrt{2x-4}}=\frac{2}{\sqrt{4}}\tan^{-1}\sqrt{\frac{2x-4}{4}}+C=\tan^{-1}\sqrt{\frac{x-2}{2}}+C$$

例3 求
$$\int x\sin^{-1}xdx$$
解：

### 使用计算机代数系统求积分
书中推荐 Maple、Mathematica。个人经验 WolframAlpha 非常好用。

### 非初等积分
