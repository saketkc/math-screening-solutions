title: 2006 Spring
date: 2015-08-07

## Problem 1

Define an indicator variable $I_i$ as:

$$
I_i = \begin{cases}
1 & \text{if $i^{th}$ and $(i+1)^{th} cards are different (H,T) or (T,H)$},\\
0 & \text{otherwise}
\end{cases}
$$

Now the number of runs in a sequence of $n$ coin tosses is given by:
$$
R_n = 1+ \sum_{i=2}^{n-1} I_i \forall n\geq 3
$$


Thus, 

$$
\begin{align}
ER_n &= 1 + \sum_{i=2}^{n-1} EI_i \\
     &= 1 + \sum_{i=2}^{n-1} P(I_i=1)
\end{align}
$$

$P(I_i=1)$  is given by : $P(I_i=1)=p\times q + q \times p$
(heads followed by tails or tails followed by heads)


And hence, 
$$
ER_n = 1+(n-2) \times (2pq)
$$

Check:
- $ER_1 = 1$ and that is $ER_1=1$
- $P(R_2=1)=p^2 + q^2$ and $P(R_2=2)=pq+qp=2pq$ thus
$E(R_2)=(p^2+q^2)+4pq = (p+q)^2+2pq = 1+2pq$ which is what $ER_n$ formula gives us
for n=2


### Variance Calculation:

To calculate: $\sigma^2=Var(R_n)$

$Var(R_n) = E(R_n^2)-(ER_n)^2$


So we focus on calculating $ER_n^2$:

$$
\begin{align}
ER_n^2 &= E((1+\sum_{i=2}^{n-1}I_i)^2)\\
 &= E(1+(\sum_{i=1}^{n-1}I_i)^2 + 2\sum_{i=2}^{n-1}I_i))\\
 &= E(1+(\sum{i=2}^{n-1}I_i^2 + 2\sum{2\leq i < j}^{n-1} I_iI_j) + 2\sum_{i=2}^{n-1}I_i)\\
 &= 1 + (n-2)\times(2pq) + 2\sum{2\leq i < j}^{n-1} I_iI_j + 2(n-2)(2pq) \\
 &= 1+3(n-2)\times(2pq) + 2\sum{2\leq i < j}^{n-1} I_iI_j\\

\end{align}
$$

In order to calculate $EI_iI_j$, we consider following 3 cases:

1. Case 1: $j-i=1$, then $P(I_i=1, I_j=1)$ = Probaility that $i^{th}, (i+1)^{th} \mathrm{and} (i+2)^{th}$ cards are different. For $i=2$ to $i={n-1}$
there are $(n-2-1)=n-3$ such terms and $P(I_i,I_j=1)= pqp+qpq=pq$

2. Case 2: $j-i>=2$, then $P(I_i=1,I_j=1) = P(I_i=1)P(I_j=1)$ , that is these events are independent unless they occur next to each other
as in Case 1. and hence $P(I_i=1,I_j=1)=P(I_i=1)P(I_j=1) = (pq)^2$ and there are $(n-4)$ such ways to choose

Thus,
$ER_n^2 = 1+6pq(n-2)+2\times((n-3)\times (pq)+(n-4)\times(pq)^2)$
Substitute in (skipping/TODO)
$Var(R_n) = ER_n^2-(ER_n)^2$

## Problem 2
$X = \{\}X_1,X_2 \dots, X_n)$ and $Y=\sum_{i=1}^{N}c_iX_i$

To determine :
- Distribution of Y

iWe use characteristic functions

Using the [characteristic function of a normal RV](https://en.wikipedia.org/wiki/Normal_distribution#Fourier_transform_and_characteristic_function):

$\phi_X(t) = E[e^{itX}] = e^{-it\mu- \frac{1}{2}\sigma^2t^2} = $

For multivariate case:

$\phi_X(\bf{t}) = E[e^{i\bf{t^T}X}] = e^{-i\bf{t^T}\mu- \frac{1}{2}\bf{t^T}\sum^2 \bf{t}} = $


Now, $Y=c^TX$ where $c=[c_1,c_2 \dots c_n]$ ($Y=\sum_{i=1}^{N}c_iX_i$)

Thus,

$\phi_Y(\bf{t}) = E[e^{i\bf{t^T}Y}] = E[e^{i\bf{t}c^TX}] = \phi_X(tc^T) =  e^{-ic^T\bf{t}\mu- \frac{1}{2}\bf{t}^Tc\sum^2 \bf{t}c^T$

and thus comparing with the characteristic function we started with:

$Y \sim N(c^T\mu, a\sum a^T)$

TODO: Check again the transposes

## Problem 3
TODO

