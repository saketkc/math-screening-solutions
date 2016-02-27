title: MATH505a 2014 Spring
date: 2016-02-21

# Paper
[http://www-bcf.usc.edu/~mathgp/quals/20141/20141_505a.pdf](http://www-bcf.usc.edu/~mathgp/quals/20141/20141_505a.pdf)

# Problem 1

Define 

$$I_i = \begin{cases}
1 & \text{Game $i$ and Game $i+1$ are won},\\
0 & \text{otherwise}
\end{cases}$$

Thus,
$$
\begin{align*}
R &= \sum_{i=1}^{m-1}I_i\\
ER &= \sum_{i=1}^{m-1}EI_i\\
Var(R) &= \sum_{i=1}^{m-1}Var(I_i) + 2\sum_{i < j}Cov(I_i,U)
\end{align*}
$$

### Part 1.a

$$
\begin{align*}
 EI_i &= P(I_i=1) \\
 &= a_ia_{i+1}\\
ER &= \sum_i EI_i\\
&=\sum_{i=1}^{m-1}a_ia_{i+1}
\end{align*}
$$

$$
\begin{align*}
Var(I_i) &= E[I_i^2]-E[I_i]E[I_i]\\
&= E[I_i](1-E[I_i])\\
&= a_ia_{i+1}(1-a_ia_{i+1})
\end{align*}
$$


$$
\begin{align*}
Cov(I_i,I_j) &= \begin{cases}
0 & j-i\geq 2(i<j)\\
E[I_{i}I_{i+1}]-E[I_i]E[I_{i+1}] & \text{otherwise}\\
\end{cases}\\
&= \begin{cases}
0 & j-i\geq 2(i<j)\\
a_ia_{i+1}a_{i+2}(1-a_{i+1}) & \text{otherwise}\\
\end{cases}\\
\end{align*}
$$

Thus,
$$
Var(R) = \sum_{i=1}^{m-1}a_ia_{i+1} + 2\sum_{i=1}^{m-2} a_ia_{i+1}a_{i+2}(1-a_{i+1})
$$

### Part 1.b

When $a_n=p=0.1$ 

$$
\begin{align*}
ER &= \sum_{i=1}^{m-1}p^2\\
&= (m-1)p^2\\
Var(R) &= \sum_{i=1}^{m-1}a_ia_{i+1} + 2\sum_{i=1}^{m-2} a_ia_{i+1}a_{i+2}(1-a_{i+1})\\
&= (m-1)p^2+2(m-2)p^3(1-p)
\end{align*}
$$

## Problem 2

$$f(x) = x/2 \text{ for } 0 < x <2$$

### Part 2.a

$S=X_1+X_2$
Using [convolution theorem](http://statweb.stanford.edu/~susan/courses/s116/node114.html):

$$
\begin{align*}
f_S(s) &= \int \frac{x}{2} \frac{s-x}{2} dx\\
&0 < s-x < 2\\
& 0 <x<2\\
&\implies s-2 < x < s \text{ and } 0 < x < 2\\
&\text{Case 1: } 0 < s < 2\  f_S(s) = \int_0^s \frac{x}{2} \frac{s-x}{2} dx = \frac{s^3}{24}\\
&\text{ Case 2: }  2 < s < 4\  f_S(s) = \int_{s-2}^4 \frac{x}{2} \frac{s-x}{2} dx = \frac{1}{4}(\frac{s(4s-s^2)}{2}-\frac{(4^3-(s-2)^3)}{3})\\
\end{align*}
$$

### Part 2.b
$$L = min(X_1, X_2, X_3, \dots X_{100})$$


$F_L = 1 - P(min(X_i) \geq y) = 1 - \prod_i P(X_i \geq y) = 1-\prod(1-P(X_i\leq y)) = 1- \big(1-\frac{y^2}{4}\big)^n $

### Part 2.c

$$R=X_1/X_2$$

$$
\begin{align*}
P(X_1/X_2 \leq z) &= P(X_1 \leq zX_2)\\
&= \int_0^{min(zx_2,2)} \frac{z^2x_2^2}{4}x_2 dx_2
\end{align*}
$$
