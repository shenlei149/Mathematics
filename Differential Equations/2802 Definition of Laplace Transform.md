### Definition of Laplace Transform
The Laplace transform of a function $f(t)$ of a real variable $t$ is another function depending on a new variable $s$, which is in general complex. We will denote the Laplace transform of $f$ by $\mathcal{L}f$. It is defined by the integral
$$(\mathcal{L}f)(s)=\int_{0^-}^\infty f(t)e^{-st}dt\tag{1}$$
for all values of $s$ for which the integral converges.

There are a few things to note.
* $\mathcal{L}f$ is only defined for those values of $s$ for which the improper integral on the right-hand side of $(1)$ converges.
* We will allow $s$ to be complex.
* As with convolution the use of $0^-$, in the definition $(1)$ is necessary to accomodate generalized functions containing $\delta(t)$. Many textbooks do not do this carefully, and hence their definition of the Laplace transform is not consistent with the properties they assert. In those cases where $0^-$ isn't needed we will use the less precise form
$$(\mathcal{L}f)(s)=\int_{0}^\infty f(t)e^{-st}dt\tag{1'}$$
* Also, as with convolution, the limits of integration mean that the Laplace transform is only concerned with functions on $(0^-, \infty)$.

### Notation, $F(s)$
We will adopt the following conventions:
* Writing $(\mathcal{L}f)(s)$ can be cumbersome so we will often use an uppercase letter to indicate the Laplace transform of the corresponding lowercase function:
$$(\mathcal{L}f)(s)=F(s),(\mathcal{L}g)(s)=G(s),\text{ etc.}$$
For example, in the formula
$$\mathcal{L}(f')=sF(s)-f(0^-)$$
it is understood that we mean $F(s) = \mathcal{L}(f)$.
* If our function doesn't have a name we will use the formula instead. For example, the Laplace transform of the function $t^2$ is written $\mathcal{L}(t^2)(s)$ or more simply $\mathcal{L}(t^2)$.
* If in some context we need to modify $f(t)$, e.g. by applying a translation by a number $a$, we can write $\mathcal{L}(f(t - a))$ for the Laplace transform of this translation of $f$.
* You've already seen several different ways to use parentheses. Sometimes we will even drop them altogether. So, if $f(t) = t^2$ then the following all mean the same thing
$$(\mathcal{L}f)(s) = F(s) = \mathcal{L}f(s) = \mathcal{L}(f(t))(s) = \mathcal{L}(t^2)(s); \mathcal{L}f = F = \mathcal{L}(t^2)$$

### Examples
