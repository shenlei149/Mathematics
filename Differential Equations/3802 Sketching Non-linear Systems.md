In session on Phase Portraits, we described how to sketch the trajectories of a linear system
$$\begin{aligned}
\begin{aligned}
x'=ax+by\\y'=cx+dy
\end{aligned}&&a,b,c,d \text{ constants}
\end{aligned}$$
We now return to the general (i.e., non-linear) $2 \times 2$ autonomous system discussed at the beginning of this chapter, in sections 1 and 2:
$$\begin{aligned}
x'=f(x,y)\\y'=g(x,y)
\end{aligned}\tag{1}$$
it is represented geometrically as a vector field, and its trajectories - the solution curves - are the curves which at each point have the direction prescribed by the vector field. Our goal is to see how one can get information about the trajectories of $(1)$, without determining them analytically or using a computer to plot them numerically.  
**Linearizing at the origin.** To illustrate the general idea, let’s suppose that $(0, 0)$ is a critical point of the system $(1)$, i.e.,
$$f(0,0)=0,g(0,0)\tag{2}$$
Then if $f$ and $g$ are sufficiently differentiable, we can approximate them near $(0, 0)$ (the approximation will have no constant term by $(2)$):
$$\begin{aligned}
f(x, y) = a_1x + b_1y + \text{ higher order terms in $x$ and $y$}\\
g(x, y) = a_2x + b_2y + \text{ higher order terms in $x$ and $y$}
\end{aligned}$$
If $(x, y)$ is close to $(0, 0)$, then $x$ and $y$ will be small and we can neglect the higher order terms. Then the non-linear system $(2)$ is approximated near $(0, 0)$ by a linear system, the linearization of $(2)$ at $(0,0)$:
$$\begin{aligned}
x' = a_1x + b_1y\\
y' = a_2x + b_2y
\end{aligned}\tag{3}$$
and near $(0,0)$, the solutions of $(1)$ - about which we know nothing - will be like the solutions to $(4)$, about which we know a great deal from our work in the previous sessions.  
**Example 1.** Linearize the system
