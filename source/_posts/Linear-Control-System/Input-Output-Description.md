---
title: input-output description
categories: 
- linear control system
- Basic
toc: true
---


Consequently, the input u(t) can be expressed symbolically as
$$
u(t) \approx \sum_{i} u\left(t_{i}\right) \delta_{\Delta}\left(t-t_{i}\right) \Delta
$$
<!--more-->

Let $g_{\Delta}\left(t, t_{i}\right)$ be the output at time $t$ excited by the pulse $u(t)=\delta_{\Delta}\left(t-t_{i}\right)$ applied at time $t_{i}$. Then we have
$$
\begin{aligned} \delta_{\Delta}\left(t-t_{i}\right) & \rightarrow g_{\Delta}\left(t, t_{i}\right) \\
\delta_{\Delta}\left(t-t_{i}\right) u\left(t_{i}\right) \Delta & \rightarrow g_{\Delta}\left(t, t_{i}\right) u\left(t_{i}\right) \Delta \quad \text { (homogeneity) } \\
\sum_{i} \delta_{\Delta}\left(t-t_{i}\right) u\left(t_{i}\right) \Delta & \rightarrow \sum_{i} g_{\Delta}\left(t, t_{i}\right) u\left(t_{i}\right) \Delta \quad \text { (additivity) } \end{aligned}
$$
Thus the output $y(t)$ excited by the input $u(t)$ can be approximated by
$$
y(t) \approx \sum_{i} g_{\Delta}\left(t, t_{i}\right) u\left(t_{i}\right) \Delta
$$
Now if $\Delta$ approaches zero, the pulse $\delta_{\Delta}\left(t-t_{i}\right)$ becomes an impulse at $t_{i},$ denoted by $\delta\left(t-t_{i}\right),$ and the corresponding output will be denoted by $g\left(t, t_{i}\right) .$ As $\Delta$ approaches zero, the approximation in $equation (2)$  becomes an equality, the summation becomes an integration, the discrete $t_{i}$ becomes a continuum and can be replaced by $\tau,$ and $\Delta$ can be written as $d \tau .$ Thus $(2)$ becomes
$$
y(t)=\int_{-\infty}^{\infty} g(t, \tau) u(\tau) d \tau
$$
Note that $g(t, \tau)$ is a function of two variables.  The second variable denotes the time at which the impulse input is applied; the ﬁrst variable denotes the time at which the output is observed. Because $g(t,\tau)$ is the response excited by an impulse, it is called the impulse response. If a system is causal, the output will not appear before an input is applied. Thus we have
$$
\text { Causal } \Longleftrightarrow g(t, \tau)=0 \text { for } t<\tau
$$
*relax* 

A system is said to be relaxed at $t_0$ if its initial state at $t_0$ is 0. In this case, the output $y(t)$, for $t ≥ t_0$ , is excited exclusively by the input $u(t)$ for $t \geq 0$.

In conclusion, every linear system that is causal and relaxed at $t_0$ can be described by
$$
\mathbf{G}(t, \tau)=\left[\begin{array}{cccc}{g_{11}(t, \tau)} & {g_{12}(t, \tau)} & {\cdots} & {g_{1 p}(t, \tau)} \\\ {g_{21}(t, \tau)} & {g_{22}(t, \tau)} & {\cdots} & {g_{2 p}(t, \tau)} \\\ {\vdots} & {\vdots} & {} & {\vdots} \\\ {g_{q 1}(t, \tau)} & {g_{q 2}(t, \tau)} & {\cdots} & {g_{q p}(t, \tau)}\end{array}\right]
$$
where 
$$
\mathbf{y}(t)=\int_{t_{0}}^{t} \mathbf{G}(t, \tau) \mathbf{u}(\tau) d \tau
$$
and $g_{ij}(t,\tau)$ is the response at time $t$ at the $i$th output terminal due to an impulse applied at time $\tau$ at the $j$ th input terminal, the inputs at other terminals being identically zero. 

That is, $g_{ij}(t, \tau )$ is the impulse response between the $j$ th input terminal and the $i$th output terminal. Thus $G$ is called the *impulse response matrix* of the system. 

