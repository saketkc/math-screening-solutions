title: MATH505a 2013 Spring
date: 2015-09-10

# Paper
[http://www-bcf.usc.edu/~mathgp/quals/20061/505aspring06.pdf](http://www-bcf.usc.edu/~mathgp/quals/20131/20131_505a.pdf)

# Problem 1

Given: $E[X|Y]=X\ and \ E[Y|X]=X$

To Show:

### Part (a): $P(X=Y)=1$

$$
E[Y]=E[E[Y|X]]=E[X]=\mu_x
$$

Thus, $\mu_y=\mu_x$

Also,
$$
\begin{align}
Cov(X,Y) &=E[XY]-E[X]E[Y]\\
&= E[E[XY|X]]-\mu_x^2\\
&= E[XE[Y|X]]-\mu_x^2\\
&= E[X^2]-\mu_x^2\\
&= \sigma_x^2
\end{align}
$$

Repeating the above with $E[XY]= E[E[XY|Y]]$ would give 
$Cov(X,Y)=\sigma_y^2$ and hence $Cov(X,Y)=\sigma_x^2=\sigma_y^2=Var(X)$
which implies $X=Y$ or $P(X=Y)=1$

Note, we implicitly used the requirement of the variance being finite[This is what is implied by the function being squared integrable: 
$\int |f(X)|^2dx < \infty$
