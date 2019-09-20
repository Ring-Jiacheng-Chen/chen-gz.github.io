---
title: Type of Random Variable
category: Probability Density Function
toc: true
---

### Bernoulli Random Variable 

Used for experiments with two outcomes of interest: The success or failure of an experiment

$X \sim$ Bernoulli $(p),$ if its **PMF** has the following form:


$$
p_{X}(x)=\left\{\begin{array}{ll}{1-p} & {\text { if } x=0} \\ {p} & {\text { if } x=1} \\ {0} & {\text { otherwise }}\end{array}\right.
$$

<!--more-->

### Binomial Random Variable

$X \sim$ Binomial $(n, p),$ if its **PMF** has the following form:
$$
p_{X}(x)=\left\{\begin{array}{ll}{\left(\begin{array}{l}{n} \\ {x}\end{array}\right) p^{x}(1-p)^{n-x}} & {\text { if } x=\{0,1, \cdots, n\}} \\ {0} & {\text { otherwise. }}\end{array}\right.
$$

* Mean: $E[X] = np$

* Variance: $Var[X] = np(1-p)$

### Geometric Random Variable

$
X \sim$ Geometric $(p),$ if its PMF has the following form:
$$
p_{X}(x)=\left\{\begin{array}{ll}{p(1-p)^{x-1}} & {\text { if } x=1,2,3, \cdots} \\ {0} & {\text { otherwise }}\end{array}\right.
$$

* Mean: $\frac{1}{p}$
* Variance: $Var[X]$

### Exponential Random Variable



### Erlang Random Variable

Continuous version of the discrete Pascal Random Variable.



### Gamma Random Variable



### Beta Random Variable



### Gaussian Random Variable

Also called the **normal random variable** because of its prevalence.

$X \sim$ Gaussian $(\mu, \sigma) :$
$$
f_{X}(x)=\frac{1}{\sqrt{2 \pi \sigma^{2}}} e^{-(x-\mu)^{2} / 2 \sigma^{2}}
$$



