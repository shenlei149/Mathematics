In the previous note we saw two main facts about the fundamental matrix:
$$\Phi(t)=\begin{pmatrix}
\boldsymbol{x}_1\\\boldsymbol{x}_2
\end{pmatrix}=\begin{pmatrix}
x_1&x_2\\y_1&y_2
\end{pmatrix}\tag{1}$$
and
$$\boldsymbol{x}=\Phi(t)\Phi(t_0)^{-1}\boldsymbol{x}_0\tag{2}$$
Is there a "best" choice for fundamental matrix?  
There are two common choices, each with its advantages. If the ODE system has constant coefficients, and its eigenvalues are real and distinct, then a natural choice for the fundamental matrix would be the one whose columns are the normal modes - the solutions of the form
$$\boldsymbol{x}_i=\overrightarrow{\alpha_i}e^{\lambda_i t}, i=1,2$$
There is another choice however which is suggested by $(2)$ and which is particularly useful in showing how the solution depends on the initial conditions. Suppose we pick $\Phi(t)$ so that
$$\Phi(t_0)=I=\begin{pmatrix}
1&0\\0&1
\end{pmatrix}\tag{3}$$
Referring to the definition $(1)$, this means the solutions $\boldsymbol{x}_1$ and $\boldsymbol{x}_2$ are picked so
$$\boldsymbol{x}_1(t_0)=\begin{pmatrix}
1\\0
\end{pmatrix},\boldsymbol{x}_2(t_0)=\begin{pmatrix}
0\\1
\end{pmatrix}\tag{3'}$$
Since the $\boldsymbol{x}_i(t)$ are uniquely determined by these initial conditions, the fundamental matrix $\Phi(t)$ satisfying $(3)$ is also unique; we give it a name.  
**Definition 2** The unique matrix $\widetilde{\Phi}_{t_0}(t)$ satisfying
$$\widetilde{\Phi}_{t_0}'=A\widetilde{\Phi}_{t_0}, \widetilde{\Phi}_{t_0}(t_0)=I$$
is called the **normalized fundamental matrix** at $t_0$ for $A$.  
For convenience in use, the definition uses Theorem 1 to guarantee $\widetilde{\Phi}_{t_0}$ will actually be a fundamental matrix. The condition $|\widetilde{\Phi}_{t_0}(t)| \neq 0$ in Theorem 1 is satisfied, since thedefinition implies $|\widetilde{\Phi}_{t_0}(t_0)| = 1$.
