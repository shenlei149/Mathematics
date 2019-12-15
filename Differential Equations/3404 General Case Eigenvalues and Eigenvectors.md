We are now ready to tackle the general case of a linear $2 \times 2$ system:
$$x'=ax+by\\y'=cx+dy$$
where the $a, b, c, d$ are constants. We will be following exactly the strategy that we laid out in the previous note. These are key concepts for the rest of the unit, and you should take the time to absorb them.  
We want to learn to write the system efficiently in matrix form. So, throughout the derivation, we will give the *expanded* matrix form of our manipulations on the left, and the *abridged* form on the right. For example, our system is:
$$\begin{pmatrix}
x'\\y'
\end{pmatrix}=\begin{pmatrix}
a&b\\c&d
\end{pmatrix}\begin{pmatrix}
x\\y
\end{pmatrix} \lrArr \boldsymbol{x'}=Ax\tag{1}$$
Following the method in the previous note, we look for solutions to our system having the form
$$\begin{pmatrix}
x\\y
\end{pmatrix}=e^{\lambda t}\begin{pmatrix}
a_1\\a_2
\end{pmatrix}=\begin{pmatrix}
a_1e^{\lambda t}\\a_2e^{\lambda t}
\end{pmatrix} \lrArr \boldsymbol{x}=e^{\lambda t}\boldsymbol{a}$$
where $a_1, a_2$, and $\lambda$ are unknown constants. We substitute this into the system $(1)$ to determine these unknown constants. Since $D(ae^{\lambda t}) = \lambda ae^{\lambda t}$, we arrive at
$$\lambda e^{\lambda t}\begin{pmatrix}
a_1\\a_2
\end{pmatrix}=e^{\lambda t}\begin{pmatrix}
a&b\\c&d
\end{pmatrix}\begin{pmatrix}
a_1\\a_2
\end{pmatrix} \lrArr \lambda e^{\lambda t}\boldsymbol{a}=e^{\lambda t}A\begin{pmatrix}
a_1\\a_2
\end{pmatrix}$$
We can cancel the factor $e^{\lambda t}$ from both sides, getting
$$\lambda\begin{pmatrix}
a_1\\a_2
\end{pmatrix}=\begin{pmatrix}
a&b\\c&d
\end{pmatrix}\begin{pmatrix}
a_1\\a_2
\end{pmatrix} \lrArr \lambda\boldsymbol{a}=A\begin{pmatrix}
a_1\\a_2
\end{pmatrix}$$
As it stands, we cannot combine the two sides by subtraction, since the scalar $\lambda$ cannot be subtracted from the square matrix on the right. As in the previously worked example, the trick is to replace the scalar $\lambda$ by the diagonal matrix $\lambda I$. This gives
$$\begin{pmatrix}
\lambda&0\\0&\lambda
\end{pmatrix}\begin{pmatrix}
a_1\\a_2
\end{pmatrix}=\begin{pmatrix}
a&b\\c&d
\end{pmatrix}\begin{pmatrix}
a_1\\a_2
\end{pmatrix} \lrArr \lambda I \boldsymbol{a}=A\begin{pmatrix}
a_1\\a_2
\end{pmatrix}$$
If we now proceed as we did in the example, subtracting the left side from the right one and using the distributive law for matrix addition and multiplication, we get a $2 \times 2$ homogeneous linear system of equations:
$$\begin{pmatrix}
a-\lambda&b\\c&d-\lambda
\end{pmatrix}\begin{pmatrix}
a_1\\a_2
\end{pmatrix}=\begin{pmatrix}
0\\0
\end{pmatrix} \lrArr (A-\lambda I)\boldsymbol{a}=\boldsymbol{0}$$
Written out without using matrices, the equations are
$$(a-\lambda)a_1+ba_2=0\\
ca_1+(d-\lambda)a_2=0\tag{2}$$
According to the theorem on square homogeneous systems this system has a non-zero solution for the $a$'s if and only if the determinant of the coefficients is zero, i.e.,
$$\begin{vmatrix}
a-\lambda&b\\c&d-\lambda
\end{vmatrix}=0 \lrArr \begin{vmatrix}
A-\lambda I
\end{vmatrix}=0$$
Evaluating the determinant we get a quadratic equation in $\lambda$:
$$\lambda^2-(a+d)\lambda+(ad-bc)=0$$
**Definition.** This is called the **characteristic equation** of the matrix
$$A=\begin{pmatrix}
a&b\\c&d
\end{pmatrix}$$
and if often denoted $p_A(\lambda)$. Its roots $\lambda_1$ and $$ are called the **eigenvalues** or **characteristic values** of the matrix $A$.  
**Remark.** In calculating the characteristic equation notice that
$$ad-bc=\det{A}\\a+d=\text{tr}A$$
Using this, the characteristic equation for a $2 \times 2$ matrix $A$ can be written as
$$\lambda^2-(\text{tr}A)\lambda+\det A=0$$
In this form, the characteristic equation of $A$ can be written down by inspection; you don't need the intermediate step of writing down $\begin{vmatrix}A-\lambda I\end{vmatrix}=0$.  
**Remark.** Abridged vs. expanded notation  
In the manipulations above, the matrix notation on the right is compact to write, which makes the derivation look simpler. On the other hand, its chief disadvantage for beginners is that it is very compressed. Practice writing the sequence of matrix equations so you get some skill in using the notation. Until you acquire some confidence, keep referring to the writtenout form on the left, so you are sure you understand what the abridged form is actually saying.

There are now various cases to consider, according to whether the eigenvalues of the matrix $A$ are:
1. two distinct real numbers,
2. a single repeated real number,
3. a pair of conjugate complex numbers.

We begin with the first case: for the rest of this note, the eigenvalues are two distinct real numbers $\lambda_1$ and $\lambda_2$.

### Real distinct eigenvalues
