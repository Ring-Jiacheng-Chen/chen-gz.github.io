---
title: Probability Properties
category: Probability Density Function
toc: true
---

### Conditional Probability

Quite often we are interested in determining whether two events, $A$ and $B$ , are related in the sense that knowledge about the occurrence of one, say $B$ , alters the likelihood of occurrence of the other, $A$ . This requires that we find the conditional probability, $P[A | B],$of event $A$ given that event $B$ has occurred. The conditional probability is defined by

<!--more-->
$$
P[A | B]=\frac{P[A \cap B]}{P[B]} \quad \text { for } P[B]>0
$$
If we multiply both sides of the definition of $P[A | B]$ by $P[B]$ we obtain
$$
P[A \cap B]=P[A | B] P[B]
$$
Similarly we also have that
$$
P[A \cap B]=P[B | A] P[A] .
$$

### Total Probability
Let $B_{1}, B_{2}, \ldots, B_{n}$ be mutually exclusive events whose union equals the sample space $S$. We refer to these sets as a partition of $S$ . Any event $A$ can be represented as the union of mutually exclusive events in the following way:

$$
\begin{aligned} A=& A \cap S=A \cap\left(B_{1} \cup B_{2} \cup \cdots \cup B_{n}\right) \\ &=\left(A \cap B_{1}\right) \cup\left(A \cap B_{2}\right) \cup \cdots \cup\left(A \cap B_{n}\right) \end{aligned}
$$
By applying $Eq(2.28 a)$ to each of the terms on the right-hand side, we obtain the 

$$
\begin{aligned}
P[A]=P\left[A | B_{1}\right] P\left[B_{1}\right]+P\left[A | B_{2}\right] P\left[B_{2}\right]+\cdots+P\left[A | B_{n}\right] P\left[B_{n}\right]
\end{aligned}
$$



### Bayes' Rule

Let $B_{1}, B_{2}, \ldots, B_{n}$ be a partition of a sample space $S$ . Suppose that event $A$ occurs; what is the probability of event $B_{j} ?$ By the definition of conditional probability we have
$$
P\left[B_{j} | A\right]=\frac{P\left[A \cap B_{j}\right]}{P[A]}=\frac{P\left[A | B_{j}\right] P\left[B_{j}\right]}{\sum_{k=1}^{n} P\left[A | B_{k}\right] P\left[B_{k}\right]}
$$
where we used the theorem on total probability to replace $P[A] .$ Equation $(2)$ is called Bayes' rule.

### Independence of Events

We will define two events $A$ and $B$ to be independent if
$$
P[A \cap B]=P[A] P[B]
$$
Equation (2.31) then implies both
$$
P[A | B]=P[A]
$$
and
$$
P[B | A]=P[B]
$$

### Bernoulli trial

A Bernoulli trial involves performing an experiment once and noting whether a particular event $A$ occurs. The outcome of The Bernoulli trial is said to be a *success* if A occurs and a "failure" otherwise. In this section we are interested in finding the probability of $k$ successes in $n$ dependent repetitions of a Bernoulli trail.

