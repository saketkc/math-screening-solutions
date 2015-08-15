title: MATH-541a 2014 Spring
date: 2015-08-14
tags: MATH-541a, 2014, Spring


## Source
  [http://www-bcf.usc.edu/~mathgp/quals/20141/20141_541a.pdf](http://www-bcf.usc.edu/~mathgp/quals/20141/20141_541a.pdf)

## Problem 1

Given:

$x_{i,1}, x_{i,2}$ :  Known values 
For $1  \leq i \leq n$:
$Z_i = \beta_1x_{i,1} +\epsilon_i $ and
$Y_i = \beta_1x_{i,1} +\beta_2x_{i,2} + \epsilon_i$
$\epsilon_i \sim N(0,1)$
### (a)
Given ${\bf{Z}} =(Z_1,Z_2,\dots,Z_n)$ find MLE estimate of $\beta_1$:

Since, $\epsilon_i \sim N(0,1)$ $\implies$ $Z_i \sim N(\beta_1x_{i,1}, 1)$ for given $\beta_1$
The likelihood function is given by:

$L(\beta_1|\textbf{Z}) = \frac{e^{-\sum_{i=1}^{n}\big(\frac{Z_i-\beta_1x_{i,1}}{2}\big)^2}}{(\sqrt{2\pi})^n}$

$LL = log(L(\beta_1|\textbf{Z})) = -\sum_{i=1}^{n}\big(\frac{Z_i-\beta_1x_{i,1}}{2}\big)^2 - \frac{n}{2}log(2\pi)$

$\frac{dLL}{d\beta_1} = \sum_{i=1}^n (Z_i-\beta_1x_{i,1})x_{i,1}$


and hence

$\hat\beta_1 = \frac{\sum Z_ix_{i,1}}{\sum x_{i,1}^2}$

$\frac{d^2LL}{d\beta_1} = -\sum x_{i,1}^2$ and hence $\hat \beta_1$ is in fact attains the maxima.


Now, $E\hat\beta_1 = \frac{E(\sum Z_ix_{i,1})}{\sum x_{i,1}^2} = \frac{\sum x_{i,1}E(Z_i)}{\sum x_{i,1}^2} = \beta_1$

and hence the MLE estimate pf $\hat \beta_1$ is an unibased estimator of $\beta_1$

###TODO Cramer-Rao Condition check?
