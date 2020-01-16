**Ex 1**  
In this problem, $A=\begin{pmatrix}1&1\\-4&1\end{pmatrix}$ and we are interested in the equation $\boldsymbol{u'}=A\boldsymbol{u}$.  
(a) Find a fundamental matrix $\Phi(t)$ for $A$.  
(b) Find the exponential matrix $e^{At}$.  
(c) Find the solution to $\boldsymbol{u'}=A\boldsymbol{u}$ with $\boldsymbol{u}(0)=\begin{bmatrix}1\\2\end{bmatrix}$.  
(d) Find a solution to $\boldsymbol{u'}=A\boldsymbol{u}+\begin{bmatrix}5\\10\end{bmatrix}$. What is the general solution? What is the solution with $\boldsymbol{u}(0)=\boldsymbol{0}$.  
**Solution**  
(a) The eigenvalues of $A$ are solutions to $(1-\lambda)^2+4=\lambda^2-2\lambda+5=0$, which are in this case the complex conjugates $1\plusmn 2i$.  
Choose one of them, say $\lambda_1=1+2i$, and find an eigenvector $v_1$ for it.  
The eigenvectors corresponding to $\lambda_1$ are the vectors in the killed by $A-\lambda_1I=\begin{bmatrix}-2i&1\\-4&-2i\end{bmatrix}$, so we can take, say, $v_1=\begin{bmatrix}1\\2i\end{bmatrix}$.  
This means this equation has a complex-valued solution
$$\begin{aligned}
\boldsymbol{u}(t)&=e^{\lambda_1t}v_1=e^{(1+2i)t}\begin{bmatrix}
1\\2i
\end{bmatrix}\\
&=e^t\begin{bmatrix}
\cos 2t+i\sin 2t\\
2i\cos 2t-2\sin 2t
\end{bmatrix}\\
&=\begin{bmatrix}
e^t\cos 2t\\-2e^t\sin 2t
\end{bmatrix}+i\begin{bmatrix}
e^t\sin 2t\\2e^t\cos 2t
\end{bmatrix}
\end{aligned}$$
By taking real and imaginary parts, we get two independent real solutions, and so can read off a fundamental matrix
$$\Phi(t)=\begin{bmatrix}
e^t\cos 2t&e^t\sin 2t
\\-2e^t\sin 2t&2e^t\cos 2t
\end{bmatrix}$$
(b) we can compute the exponential matrix for this system from any fundamental matrix $\Phi(t)$ found in the first part by using the formula
$$e^{At}=\Phi(t)\Phi(0)^{-1}$$
$$\Phi(0)=\begin{bmatrix}
1&0\\0&2
\end{bmatrix}$$
so
$$\Phi(0)^{-1}=\begin{bmatrix}
1&0\\0&1/2
\end{bmatrix}$$
$$\begin{aligned}
e^{At}&=\begin{bmatrix}
e^t\cos 2t&e^t\sin 2t
\\-2e^t\sin 2t&2e^t\cos 2t
\end{bmatrix}\begin{bmatrix}
1&0\\0&1/2
\end{bmatrix}\\
&=\begin{bmatrix}
e^t\cos 2t&\frac{1}{2}\sin 2t\\
-2e^t\sin 2t&e^t\cos 2t
\end{bmatrix}
\end{aligned}$$
(c) The general strategy is to find the solution with a given initial condition directly from the exponential matrix:
$$\begin{aligned}
\boldsymbol{u}(t)&=e^{At}\boldsymbol{u}(0)\\
&=\begin{bmatrix}
e^t\cos 2t&\frac{1}{2}\sin 2t\\
-2e^t\sin 2t&e^t\cos 2t
\end{bmatrix}\begin{bmatrix}
1\\2
\end{bmatrix}\\
&=\begin{bmatrix}
e^t(\cos 2t+\sin 2t)\\2e^t(-\sin 2t+\cos 2t)
\end{bmatrix}
\end{aligned}$$
(d) We guess a constant solution
$$\boldsymbol{u}=\begin{bmatrix}
k_1\\k_2
\end{bmatrix}$$
Substituting this into the DE gives
$$\begin{bmatrix}
0\\0
\end{bmatrix}=A\begin{bmatrix}
k_1\\k_2
\end{bmatrix}+\begin{bmatrix}
5\\10
\end{bmatrix}$$
This implies
$$\boldsymbol{u}=-A^{-1}\begin{bmatrix}
5\\10
\end{bmatrix}=-\frac{1}{5}\begin{bmatrix}
1&-1\\4&1
\end{bmatrix}\begin{bmatrix}
5\\10
\end{bmatrix}=\begin{bmatrix}
1\\-6
\end{bmatrix}$$
Since all homogeneous solutions are of the form $e^{At}\begin{bmatrix}a\\b\end{bmatrix}$, the general solution is then given by
$$e^{At}\begin{bmatrix}a\\b\end{bmatrix}+\begin{bmatrix}
1\\-6
\end{bmatrix}=\begin{bmatrix}
e^t(a\cos 2t+\frac{1}{2}b\sin 2t)+1\\
e^t(-2a\sin 2t+b\cos 2t)-6
\end{bmatrix}$$
for some constants $a, b$.  
To find the particular solution with $\boldsymbol{u}(0)=0$, we plug $t = 0$ into this expression, and get that
$$\begin{bmatrix}
a+1\\b-6
\end{bmatrix}=\begin{bmatrix}
0\\0
\end{bmatrix}$$
so the desired solution is given by the constants $a = -1$ and $b = 6$:
$$\begin{bmatrix}
e^t(-\cos 2t+3\sin 2t)+1\\
e^t(2\sin 2t+6\cos 2t)-6
\end{bmatrix}$$
