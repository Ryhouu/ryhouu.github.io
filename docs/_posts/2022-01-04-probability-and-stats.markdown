---
layout: post
title:  "Probability and Statistics Notes"
date:   2022-01-04 15:06:15 -0800
categories: jekyll update
mathjax: true
---

## Probability

### 1. PMF & PDF

> + (discrete) Probability Mass Function:
>
>   
>   $$
>   P(x_i) = P(X=x_i)
>   $$
>
> + (continuous) Probability Density Function $f$:
>
>   
>   $$
>   P(a \leq X \leq b) = \int_a^b f(x) dx \quad \forall a \leq b
>   $$

---

### 2. Basic Concepts

| Measurements          | Discrete                          | Continuous                                         |
| --------------------- | --------------------------------- | -------------------------------------------------- |
| $P(a \leq X \leq b)$  | $\sum_{a\leq x_i \leq b} P(x_i)$  | $\int_a^b f(x)dx$                                  |
| $\mu = E[X]$          | $\sum x_i \cdot P(x_i)$           | $\int_{-\infty}^{\infty} x \cdot f(x)dx$           |
| $E[g(X)]$             | $\sum g(x_i) \cdot P(x_i)$        | $\int_{-\infty}^{\infty} g(x) \cdot f(x)dx$        |
| $Var(X)=E[(X-\mu)^2]$ | $\sum (x_i - \mu)^2 \cdot P(x_i)$ | $\int_{-\infty}^{\infty} (x - \mu)^2 \cdot f(x)dx$ |
| $SD(X)$               | $\sqrt{Var{(X)}}$                 | $\sqrt{Var{(X)}}$                                  |



#### Properties:

+ $Var(X) = E[X^2] - E[X]^2$

+ $E[aX+b] = a\cdot E[X] + b$

+ $Var(aX+b) = a^2 \cdot Var(X)$

+ $SD(aX+b) = \vert a\vert \cdot SD(X)$

---

### 3. Distributions

#### 1. Discrete

+ Binomial

$$
\begin{aligned}
X \sim Bin(n,p): \quad 
& \text{$X$ is the number of successes in $n$ trials.} \\
& P(X = k) = {n \choose k}p^k (1-p)^{n-k}, \quad \forall k \in \mathbb N \\
& E[X] = np, \quad Var(X) = np(1-p) \\

\end{aligned}
$$

+ Geometric

$$
\begin{aligned}
X \sim Geom(p): \quad 
& \text{$X$ is the number of trials until the first success.} \\
& P(X = k) = (1-p)^{k-1} \cdot p, \quad \forall k \in \mathbb N^+ \\
& E[X] = \frac{1}{p}, \quad Var(X) = \frac{1-p}{p^2} \\

\end{aligned}
$$

