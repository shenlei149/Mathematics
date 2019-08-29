### Introduction
Not every $F(s)$ we encounter is in the Laplace table. Partial fractions is a method for re-writing $F(s)$ in a form suitable for the use of the table.  
In this note we will run through the various cases encountered when we apply the method of partial fractions decomposition to a rational function. In the next note we will learn the Heaviside cover-up method, which simplifies some of the algebra.  
**Note:** We use the term undetermined coefficients in the same way it was use when solving an ODE with polynomial input. It involves setting a polynomial with unknown coefficients equal to a known polynomial and solving for the unknown coefficients by equating them with the known ones.

### Rational Functions
A **rational function** is one that is the ratio of two polynomials. For example
$$\frac{s+1}{s^2+7s+9} \text{ and } \frac{s^2+7s+9}{s+1}$$
are both rational functions.  
A rational function is called **proper** if the degree of the numerator is strictly smaller than the degree of the denominator; in the examples above, the first is proper while the second is not.  
**Long-division:** Using long-division we can always write an improper rational function as a polynomial plus a proper rational function. The partial fraction decomposition only applies to proper functions.  
**Example 1.** Use long-division to write $\frac{s^3+2s+1}{s^2+s-2}$ as a the sum of a polynomial and a proper rational function.  
**Solution.**
$$TODO$$
Therefore,
$$\frac{s^3+2s+1}{s^2+s-2}=s-1+\frac{5s-1}{s^2+s-2}$$

### Linear Factors
Here we assume the denominator factors in distinct linear factors. We start with a simple example. We will explain the general principle immediately afterwords.  
**Example 2.** Decompose $R(s)=\frac{s-3}{(s-2)(s-1)}$ using partial fractions. Use this to find $\mathcal{L}^{-1}(R(s))$.  
**Solution.**
$$\frac{s-3}{(s-2)(s-1)}=\frac{A}{s-2}+\frac{B}{s-1}$$
Multiplying both sides by the denominator on the left gives
$$s-3 = A(s-1) + B(s-2)\tag{1}$$
The sure algebraic way is to expand out the right hand side and equate the coefficients with those of the polynomial on the left.
$$s-3 = (A+B)s + (-A-2B) \rArr \begin{cases}
1&=&A+B\\
-3&=&-A-2B
\end{cases}$$
We solve this system of equations to find the undetermined coefficients $A$ and $B$: $A = -1, B = 2$.  
Answer: $R(s)=-1/(s-2)+2/(s-1)$  
Table lookup then gives $\mathcal{L}^{-1}(R(s))=-e^{2t}+2e^t$.  
**Note:** In this example it would have been easier to plug the roots of each factor into equation $(1)$. When you do this every term except one becomes 0.  
Plug in $s=1 \rArr -2=B(1-2) \rArr B=2$.  
Plug in $s=2 \rArr -1=A(2-1) \rArr A=-1$.  
In general, if $P(s)/Q(s)$ is a proper rational function and $Q(s)$ factors into distinct linear factors $Q(s) = (s-a_1)(s-a_2)\cdots(s-a_n)$ then
$$\frac{P(s)}{Q(s)}=\frac{A_1}{s-a_1}+\frac{A_2}{s-a_2}+\cdots+\frac{A_n}{s-a_n}$$
The proof of this is not hard, but we will not give it. Remember you must have a *proper* rational function and each of the factors must be distinct. Repeated factors are discussed below.  
**Example 3.** Use partial fractions to find $\mathcal{L}^{-1}(\frac{3}{s^3-3s^2-s+3})$  
**Solution.** The hardest part of this problem is to factor the denominator. For higher order polynomials this might be impossible. In this case you can check
$$s^3-3s^2-s+3=(s-1)(s+1)(s-3)$$
The partial fractions decomposition is
$$\frac{3}{(s-1)(s+1)(s-3)}=\frac{A}{s-1}+\frac{B}{s+1}+\frac{C}{s-3}$$
Multiplying through by the denominator gives
$$3=A(s+2)(s-3)+B(s-1)(s-3)+C(s-1)(s+2)$$
Plugging in $s = 1$ gives $A = -3/4$, likewise $s = -1$ gives $B = 3/8$ and $s = 3$ gives $C = 3/8$.  
Our answer is
$$\mathcal{L}^{-1}(\frac{3}{s^3-3s^2-s+3})=Ae^t+Be^{-t}+Ce^{3t}=-\frac{3}{4}e^t+\frac{3}{8}e^{-t}+\frac{3}{8}e^{3t}$$

### Quadratic Factors
TODO
