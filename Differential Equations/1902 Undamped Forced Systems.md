We now look at the pure resonant case for a second-order LTI (Linear Time Invariance) DE. We will use the language of spring-mass systems in order to interpret the results in physical terms, but in fact the mathematics is the same for any second-order LTI DE for which the coefﬁcient of the ﬁrst derivative is equal to zero.

The problem is thus to ﬁnd a particular solution the DE
$$
x''+\omega_0^2x=F_0\cos \omega t
$$
Complex replacement:
$$
z''+\omega_0^2z=F_0e^{i\omega t}\\
x=Re(z)
$$
Characteristic polynonial:
$$
p(s)=s^2+\omega_0^2\\
p'(s)=2s\\
p(i\omega)=\omega_0^2-\omega^2\\
p'(i\omega)=2i\omega
$$
Exponential Response formula:
$$
z_p=\begin{cases}
\frac{F_0e^{i\omega t}}{p(i\omega)}=\frac{F_0e^{i\omega t}}{\omega_0^2-\omega^2}\text{ if }\omega\neq\omega_0\\
\frac{F_0te^{i\omega t}}{p'(i\omega)}=\frac{F_0te^{i\omega t}}{2i\omega}\text{ if } \omega=\omega_0
\end{cases}\\
x_p=\begin{cases}
\frac{F_0\cos \omega t}{\omega_0^2-\omega^2}\text{ if }\omega\neq\omega_0\\
\frac{F_0t\sin \omega t}{2\omega_0}\text{ if } \omega=\omega_0
\end{cases}
$$
**Resonance and amplitude response of the undamped harmonic oscillator**

In $x_p$ the amplitude $=A=A(\omega)=\vert\frac{1}{\omega_0^2-\omega^2}\vert$ is a function of $\omega$.  
The plot below shows $A$ as a function of $\omega$. Note, it is similar to the damped amplitude response except the peak is inﬁnitely high. As $\omega$ gets closer to $\omega_0$ the amplitude increases.
Tplot is output amplitude vs. input frequency.  
![](pic190201.png)

When $\omega=\omega_0$ we have $x_p=\frac{F_0t\sin \omega t}{2\omega_0}$. This is called *pure resonance* (like a swing). The frequency $\omega_0$ is called the *resonant* or *natural* frequency of the system.  
In the plot below notice that the response is oscillatory but not periodic. The amplitude keeps growing in time (caused by the factor of $t$ in $x_p$).   
The plot is output vs. time (for a ﬁxed input frequency).  
![](pic190202.png)
