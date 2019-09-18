---
title: Linear Time-Invariant(LTI) Systems
categories: 
- linear control system
- Basic
toc: true
---

*time invariant* 

A system is said to be time invariant if for every state-input–output pair
$$
\left.\begin{array}{l}{\mathbf{x}\left(t_{0}\right)} \\\ {\mathbf{u}(t), t \geq t_{0}}\end{array}\right\} \rightarrow \mathbf{y}(t), \quad t \geq t_{0}
$$
and any $T$, we have
$$
\left.
\begin{array}{l}{\mathbf{x}\left(t_{0}+T\right)} \\ {\mathbf{u}(t-T), t \geq t_{0}+T}\end{array}\right\} \rightarrow \mathbf{y}(t-T), t \geq t_{0}+T \quad \text { (time shifting) }
$$
<!--more-->

It means that if the initial state is shifted to time $t_0 + T$ and the same input waveform is applied from $t_0 + T$ instead of from $t_0$ , then the output waveform will be the same except that it starts to appear from time $t_0 + T$ . In other words, if the initial state and the input are the same, no matter at what time they are applied, the output waveform will always be the same. Therefore, for time-invariant systems, we can always assume, without loss of generality, that $t_0 = 0$. If a system is not time invariant, it is said to be *time varying*.

for a linear system causal condition is 
$$
\text { Causal } \Longleftrightarrow g(t, \tau)=0 \text { for } t<\tau
$$
so for LTI system that $g(t) = 0, t<t_0$. 

