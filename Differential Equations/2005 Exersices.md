Find a solution of $x''+3x'+2x=te^{−t}$.  
Solution: We use the method of variation of parameters.  
Suppose there is a solution of the form $x(t) =u(t)e^{−t}$ for some function $u(t)$.
$$x'=(u'-u)e^{-t}$$
$$x''=(u''-2u'+u)e^{-t}$$
and the equation becomes
$$
\begin{aligned}
x''+3x'+x&=[(u''-2u'+u)+3(u'-u)+2u]e^{-t}\\
&=(u''+u')e^{-t}\\
&=te^{-t}
\end{aligned}
$$
The exponential is never zero, so can cancel $e^{−t}$ from both sides and obtain
$$u''+u'=t$$
Lowest order derivative is 1, so we should bump up all degrees by 1. So try $u=At^2+Bt+C$.  
$$u'=2At+B$$
$$u''=2A$$
$$u''+u'=2At+(2A+B)=t$$
$$A=1/2\text{ and }B=-1$$
so
$$u=\frac{1}{2}t^2-t$$
$$x=(\frac{t^2}{2}-t)e^{-t}$$
