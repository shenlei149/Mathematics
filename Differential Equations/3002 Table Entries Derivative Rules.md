### $t$-derivative rule
This is a course on differential equations. We should try to compute $\mathcal{L}(f')$.  
As usual, let $\mathcal{L}(f)(s) = F(s)$. Let $f'$ be the *generalized* derivative of $f$. (Recall, this means jumps in $f$ produce delta functions in $f'$.) The $t$-derivative rule is
$$\mathcal{L}(f')=sF(s)-f(0^-)\tag{1}$$
$$\mathcal{L}(f'')=s^2F(s)-sf(0^-)-f'(0^-)\tag{2}$$
$$\mathcal{L}(f^{(n)})=s^nF(s)-s^{(n-1)}f(0^-)-s^{(n-2)}f'(0^-)+\cdots-f^{(n-1)}(0^-)\tag{3}$$
**Proof:** Rule (1) is a simple consequence of the definition of Laplace transform and integration by parts.
$$\begin{aligned}
\mathcal{L}(f')&=\int_{0^-}^\infty f'(t)e^{-st}dt\\
&=f(t)e^{-st}\bigg|_{0^-}^\infty+s\int_{0^-}^\infty f(t)e^{-st}dt\\
&=sF(s)-f(0^-)
\end{aligned}$$
The last equality follows from:
1. We assume $f(t)$ has exponential order, so if Re$(s)$ is large enough $f(t)e^{-st}$ is 0 at $t = \infty$.
2. The integral in the second term is none other than the Laplace transform of $f(t)$.

Rule $(2)$ follows by applying rule $(1)$ twice.
$$\begin{aligned}
\mathcal{L}(f'')&=s\mathcal{L}(f')-f'(0^-)\\
&=s(sF(s)-f(0^-))-f'(0^-)\\
&=s^2F(s)-sf(0^-)-f'(0^-)
\end{aligned}$$
Rule $(3)$ Follows by applying rule $(1)$ $n$ times.  
**Notes:** 1. We will call the terms $f(0^-), f'(0^-)$ the 'annoying terms'. We will be happiest when our signal $f(t)$ has rest initial conditions, so all of the annoying terms are 0.  
2. A good way to think of the $t$-derivative rules is
$$\mathcal{L}(f)=F(s)$$
$$\mathcal{L}(f')=sF(s)+ \text{ annoying terms at } 0^-$$
$$\mathcal{L}(f'')=s^2F(s)+ \text{ annoying terms at } 0^-$$
Roughly speaking, Laplace transforms differentiation in $t$ to multiplication by $s$.  
3. The proof of rule $(1)$ uses integration by parts. This is clearly valid if $f'(t)$ is continuous at $t = 0$. It is also true (although we won't show this) if $f'(t)$ is a generalized function. - See example 2 below.  
**Example 1.**
