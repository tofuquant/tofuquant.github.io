---
layout:     post
title:      "Coursera FE"
subtitle:   " \"Start here\" "
date:       2021-05-05 12:00:00
author:     "J"
catalog: false
header-style: text
tags:
    - Rando
---

# Introduction to Financial Engineering
## W1
Markets are central to everything. Gathering information, aggregating liquidity and promoting efficiency.

Products are created to satisfy customers. Hedging risks, speculation, raising funds and liabilities.

How can we model markets? Discrete time-models (single-,multi-period models) continuous time models.

Discrete time multi-period models will be the focus.

### Financial Engineering
* Security pricing - pricing securities and their derivatives
* Portfolio selection - maximising the utility of consumption and wealth
* Risk Management - stress-testing of portfolio. Tail risk measuring (VaR and conditional VaR)

## W2
### Discrete Random Variables
* cumulative distribution function $F(\cdot)$ of a random variable X
$$ F(x) := P(X<x)$$
* probability mass function $p(\cdot)$, if $p(x) \leq 0$
 and for all events A,
 $$P(X\in A)=\sum_{x\in A}p(x)$$
* expected value of a discrete random variable X,
$$E[X]:=\sum_i x_i p(x_i)$$
* variance of any random variable
$$\begin{split}Var(X):&= E[(X-E[X])^2]\\
&=E[X^2 - 2X E[X] +E[X]^2]\\
&= E[X^2] - 2E[X]E[X]+E[X]^2\\
&=E[X^2]-E[X]^2 \end{split}$$

### Binomial distribution
X has a binomial distribution ($X \sim \text{Bin}(n,p)$) if

$$ P(X=r) = \left(\begin{array}{c}{n\\
  r} \end{array}\right) p^r (1-p)^{n-r}, \text{where} \left(\begin{array}{c}{n\\r} \end{array}\right) = \dfrac{n!}{r!(n-r)!}$$

* $E[X]=np$
* $Var(X) = np(1-p)$

### Poisson Distribution

X has a $Poisson(\lambda)$ distribution if,

$$P(X=r)= \frac{ \lambda^r e^{-\lambda}}{r!}$$

* $E[X]=\lambda$
* $Var(X) = \lambda$


### Bayes' Theorem
Let $A$ and $B$ be two events for which $P(B)\neq0$. Then,
$$P(A|B) = \frac{P(A\cap B)}{P(B)}=\frac{P(B|A)P(A)}{P(B)}=\frac{P(B|A)P(A)}{\sum_j P(B|A_j)P(A_j)}$$
Where $A_j$ is a partition of the sample-space.

### Continuous Random Variables
A continuous random variable X, has probability density function $f(\cdot)$, if $f(x)\geq 0$ and for all events A,
$$P(X\in A) = \int_A f(y)dy$$
The relation of the CDF and PDF,
$$F(x) = P(-\infty \leq X \leq x)= \int_{-\infty}^x f(y) dy$$

### Normal Distribution
X has a Normal distribution ($X \sim  N(\mu,\sigma^2)$) if
$$f(x) = \frac{1}{\sqrt{2\pi\sigma^2}}\exp{\left(-\frac{(x-\mu)^2}{2\sigma^2}\right)}$$

* $E[X] = \mu$
* $Var(X)= \sigma^2$

### Log-Normal Distribution
X has a log-normal distribution ($X \sim LN(\mu,\sigma^2)$) if,
$$log(X) \sim N(\mu,\sigma^2)$$

* $E[X] = \exp(\mu+\sigma^2/2)$
* $Var(X)= \exp(2\mu+\sigma^2)(\exp(\sigma^2)-1)$

### Conditional Expectation and Variances

Conditional Expectation identity is
$$E[X]=E[E[X|Y]]$$

Conditional Variance identity is
$$Var(X)= Var(E[X|Y])+E[Var(X|Y)]$$

**Random** Sum of Random Variables
Let $W=X_1+X_2+...+...X_N$ where $X_i$ are IID with mean $\mu_x$ and variance $\sigma^2_x$). Where $N$ is also a random variable.
What is the expected value of this distribution?
$$E[W] = E[E[W|N]]$$
