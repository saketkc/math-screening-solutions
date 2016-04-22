title: Royal Statistical Society Graduate Diploma Module 1- 2014
date: 2016-04-21

# Paper
[Paper Link](http://www.rss.org.uk/Images/PDF/pro-dev/Exam past papers/2014/rss-grad-diploma-module1-2014.pdf)

# Problem 1

## Problem (i)
\begin{align*}
F(x) &= P(X \leq x\\
&= \sum_{A} P(X \leq x, A)\\
&= P(X \leq x, A) + P(X \leq x, A^c)\\
&= P(X \leq x|A)P(A) + P(X \leq x|A^c)P(A^c)\\
&= F_1(x)\theta + F_2(x)(1-\theta)
 \end{align*}

To deduce the next euqation, we simply differentiate the above:

\begin{align*}
\frac{d}{dx} F(x) &= \frac{d}{dx} F_1(x)\theta+F_2(x)(1-\theta)\\
f(x) &= f_1(x)\theta+f_2(x)(1-\theta)\\
\int x f(x)dx &= \int x\theta f_1(x)dx + \int x(1-\theta)f_2(x)dx\\
E[X] &= \theta \mu_1 + (1-\theta)\mu__1
\end{align*}

## Problem (ii)

\begin{align*}
W_i &\sim \mathcal{N}(4.5,0.25)\\
S_6=\sum_{i=1}^6 W_I &\sim \mathcal{N}(27,1.5)\\
P(S_6\leq 25) &= P(\frac{S_6-27}{\sqrt{1.5}} \leq -\frac{2}{\sqrt{1.5}})\\
&= P(Z \leq -1.63)\\
&=0.056
\end{align*}

## Problem (iii)

\begin{align*}
EW &= P(S_6 \leq 25)E[S_7] + P[S_6 \geq 25]E[S_6]\\
&= 0.056*31.5+(1-0.056)*27\\
&= 27.322
\end{align*}

## Problem (iv)

\begin{align*}
P(S_6 \leq 25) &= 0.01\\
P(Z \leq -\frac{2}{\sigma}) &= 0.01
\implies -\frac{2}{\sigma}&= -2.33\\
&= 1.165
\end{align*}

# Problem 2


## Problem (i)
Median = $\int_{-\infty}^m = \frac{1}{2}$
Thus,
\begin{align*}
\int_{-\infty}^m xf(x) dx &= \frac{1}{2}\\
\int_{-p}^{\infty}
 x f(-x) = \frac{1}{2}\\
&= \int_p^{\infty} xf(x)\\
&=  \int_{-p}^{\infty} xf(-x)dx\\
\implies p &= \\
\implies p &=0
\end{align*}

Thus median $m=0$



## Problem (ii)

\begin{align*}
EX &= \int_{-\infty}^{\infty}xf(x)dx \\
&= \int_{\infty}^{-\infty}-xf(-x)d(-x) \ x \longrightarrow -x\\
&= -\int_{-\infty}^{\infty}xf(-x)dx\\
&= -\int_{-\infty}^{\infty}xf(x)dx \text{ since } f(x)=f(-x) \\
\implies E[X} &=0
\end{align*}

## Problem (iii)

$Y=X^2$

\begin{align*}
E[XY] &= E[X^3]\\
&= \int_{-\infty}^\infty x^3f(x)dx\\
&=0
\end{align*}

$Cov(X<y)=E[XY]-E[X]E[Y] = 0$ and hence $X,Y$ are uncorrelated

## Problem (iv)

\begin{align*}
g(y) &= f_X(\sqrt{y}) \frac{dx}{dy}\\
&= \frac{1}{2\sqrt{y}}f_X(\sqrt{y})\\
\text{Note the typo in the original question where $\frac{1}{2}$ is issing}
\end{align*}

# Problem 3


# Problem 4


# Problem 5


# Problem 6

# Problem 7


# Problem 8
