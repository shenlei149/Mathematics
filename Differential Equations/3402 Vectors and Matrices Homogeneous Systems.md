### More on matrices
Associated with every square matrix $A$ is a number, written $|A|$ or $|\det(A)|$ called the determinant of $A$. For these notes, it will be enough if you can calculate the determinant of $2 \times 2$ matrices, which is as follows:
$$\det\begin{pmatrix}
a&b\\c&d
\end{pmatrix}=ad-bc$$
The trace of a square matrix $A$ is the sum of the elements on the main diagonal; it is denoted $tr(A)$:
$$tr\begin{pmatrix}
a&b\\c&d
\end{pmatrix}=a+d$$
**Remark.** Theoretically, the determinant should not be confused with the matrix itself. The determinant is a number, the matrix is the square array. But, everyone puts vertical lines on either side of the matrix to indicate its determinant, and then uses phrases like "the first row of the determinant," meaning the first row of the corresponding matrix.  
An important formula which everyone uses and no one can prove is
$$\det{(AB)}=\det{A}\cdot \det{B}\tag{1}$$

### Homogeneous $2 \times 2$ systems
Matrices and determinants were originally invented to handle, in an efficient way, the solution of a system of simultaneous linear equations. This is still one of their most important uses. We give a brief account of what you need to know for now. We will restrict ourselves to square $2 \times 2$ homogeneous systems; they have two equations and two variables (or "unknowns", as they are frequently called). Our notation will be:
$$A = (a_{ij}), \text{a square $2 \times 2$ matrix of constants}$$
$$\boldsymbol{x} = (x_1, x_2)^T, \text{a column vector of unknowns}$$
then the square system
$$a_{11}x_1+a_{12}x_2=0$$
$$a_{21}x_1+a_{22}x_2=0$$
can be abbreviated by the matrix equation
$$A\boldsymbol{x}=0\tag{2}$$
This always has the solution $\boldsymbol{x} = 0$, which we call the **trivial solution**. The question is: when does it have a nontrivial solution?  
Theorem. Let $A$ be a square matrix. The equation 
$$A\boldsymbol{x} = 0 \text{ has a nontrivial solution} \rArr \det{A} = 0 \text{(i.e., A is singular)}\tag{3}$$

### Linear independence of vectors
