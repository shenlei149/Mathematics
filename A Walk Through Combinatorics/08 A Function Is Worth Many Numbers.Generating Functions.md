## Ordinary Generating Functions
### Recurrence Relations and Generating Functions
一个池塘，每年年底从里面打捞100个青蛙，青蛙自身每年繁殖四倍，若初始时青蛙有50只，第$n$年有多少青蛙呢。  
$a_0=50,a_1=4a_0-100=100,\cdots$，很容易写出递归式$a_{n+1}=4a_n-100$，但是如果只想知道第87年的青蛙数量，就必须从1开始逐个计算，浪费了很多中间结果。  
为了避免这种情况，需要知道$a_n$的显式公式(`explicit formula`)，只依赖于$n$而不包含$a_{n-1}$或其他项，是可以直接计算得到值的。  
我们从这个递归式开始
$$a_{n+1}=4a_n-100\tag{8.1}$$
对$n\ge 0$都成立且初始值$a_0=50$。事实上上面的公式包含无穷个式子，从无穷个式子归纳出一个显式公式，就需要用到生成函数(`generating functions`)的概念。

**Definition 8.1.**
