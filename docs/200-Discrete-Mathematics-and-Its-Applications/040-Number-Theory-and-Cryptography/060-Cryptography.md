### Classical Cryptography
最早加密信息的例子之一是 Julius Caesar 将字母后移三位进行字母替换。加密（`encryption`）是使信息保密的过程。

Caesar 的加密方法是将字母映射到数字 0 到 25，然后加 3 模 26。加密函数可以写作
$$f(p)=(p+3)\operatorname{mod}26$$
从加密信息中获取原始信息的过程是解密（`decryption`）。Caesar 解密方法是使用 $f$ 的逆
$$f^{-1}(p)=(p-3)\operatorname{mod}26$$

下面一般化这个方法。引入密钥（`key`）$k$
$$f(p)=(p+k)\operatorname{mod}26$$
$$f^{-1}(p)=(p-k)\operatorname{mod}26$$
这就是移位密码（`shift cipher`），也称为凯撒密码。

可以通过如下公式增加安全性
$$f(p)=(ap+b)\operatorname{mod}26$$
其中 $a,b$ 是整数且他们的选择保证这个函数是双射（等价于 $\gcd(a,26)=1$）。

这称为仿射密码（`affine cipher`），这种变化方式称为仿射变换（`affine transformation`）。

下面解释如何对这种加密方法进行解密。给定一个数字 $p,0\leq p\leq 25$，那么 $c=(ap+b)\operatorname{mod}26,\gcd(a,26)=1$，解密就是要用 $c$ 来表示 $p$。同同余式 $c\equiv (ap+b)\operatorname{mod}26$ 开始，两边同时减去 $b$ 得到 $c-b\equiv ap\operatorname{mod}26$。由于 $\gcd(a,26)=1$，所以 $a$ 模 26 存在逆 $\bar{a}$。那么两边同时乘以 $\bar{a}$ 得到 $\bar{a}(c-b)\equiv \bar{a}ap\equiv p\operatorname{mod}26$，所以 $p\equiv\bar{a}(c-b)(\operatorname{mod}26)$。$p$ 是确定值，因为 $p\in Z_{26}$。

**密码破译（`CRYPTANALYSIS`）** 在不知道加密方法和密钥的情况下恢复原文的过程称为密码破译，这个过程非常困难。这里只介绍移位密码的破解。
