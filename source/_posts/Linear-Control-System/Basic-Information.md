---
title: Basic Information
categories: 
- linear control system
- Basic
toc: true
---

## Basic Information

The systems to be studied in this categories are limited to linear systems. Using the concept of linearity, that every linear system can be described by
$$
\mathbf{y}(t)=\int_{t_{0}}^{t} \mathbf{G}(t, \tau) \mathbf{u}(\tau) d \tau
$$
<!--more-->
This equation describes the relationship between the input u and output y and is called the input–output or external description. If a linear system is lumped as well, then it can also be described by
$$
\dot{\mathbf{x}}(t) =\mathbf{A}(t) \mathbf{x}(t)+\mathbf{B}(t) \mathbf{u}(t)
$$

$$
\mathbf{y}(t) =\mathbf{C}(t) \mathbf{x}(t)+\mathbf{D}(t) \mathbf{u}(t) 
$$
$Equation (2)$ is a set of ﬁrst-order differential equations and $Equation (3)$ is a set of algebraic equations. 

They are called the internal description of linear systems. Because the vector $x$ is called the state, the set of two equations, $equation (2)$ and $equation (3)$, is called the state-space or, simply, the state equation.

If a linear system has, in addition, the property of time invariance, then $Equations (1)$ through $(3)$ reduce to
$$
\mathbf{y}(t)=\int_{0}^{t} \mathbf{G}(t-\tau) \mathbf{u}(\tau) d \tau
$$
and 
$$
\begin{array}{c}
{\dot{\mathbf{x}}(t)=\mathbf{A} \mathbf{x}(t)+\mathbf{B u}(t)} \\ {\mathbf{y}(t)=\mathbf{C x}(t)+\mathbf{D} \mathbf{u}(t)}\end{array}
$$
For this class of linear time-invariant systems, the Laplace transform is an important tool in analysis and design. Applying the Laplace transform to (1.4) yields
$$
\hat{\mathbf{y}}(s)=\hat{\mathbf{G}}(s) \hat{\mathbf{u}}(s)
$$
where a variable with a circumﬂex denotes the Laplace transform of the variable. The function $\hat{G}(s)$ is called the *transfer matrix*. Both $(4)$ and $(6)$ are input–output or external descriptions. The former is said to be in the time domain and the latter in the frequency domain. 


## Categories
*SISO*

A system with only one input terminal and only one output terminal is called a single-variable system or a single-input single-output (SISO) system.

*MIMO*

A system with two or more input terminals and/or two or more output terminals is called a multi-variable system. More speciﬁcally, we can call a system a multi-input multi-output (MIMO) system if it has two or more input terminals and output terminals.

*SIMO*

A single-input multi-output (SIMO) system if it has one input terminal and two or more output terminals.

*continuous-time*

A system is called a continuous-time system if it accepts continuous-time signals as its input and generates continuous-time signals as its output.

*discrete-time* 

A system is called a discrete-time system if it accepts discrete-time signals as its input and generates discrete-time signals as its output. 

*memoryless system* 

A system is called a memoryless system if its output y(t 0 ) depends only on the input applied at t 0 ; it is independent of the input applied before or after t 0 . This will be stated succinctly as follows: current output of a memoryless system depends only on current input; it is independent of past and future inputs.

*causal or non-anticipatory*

A system is called a causal or non-anticipatory system if its current output depends on past and current inputs but not on future input. If a system is not causal, then its current output will depend on future input. In other words, a non-causal system can predict or anticipate what will be applied in the future. No physical system has such capability. Therefore every physical system is causal and causality is a necessary condition for a system to be built or implemented in the real world. This text studies only causal systems.

![](https://cdn.mathpix.com/snip/images/SS39b_F6XhCg1YDMsDbnWJ5O4bin0N1O2TEFof_E9VY.original.fullsize.png)

Using the state at $t_0$ , we can express the input and output of a system as


$$
\left. \begin{array}{l}{\mathbf{x}\left(t_{0}\right)} \\ {\mathbf{u}(t), t \geq t_{0}}\end{array} \right\} \rightarrow \mathbf{y}(t), \quad t \geq t_{0}
$$

It means that the output is partly excited by the initial state at $t_0$ and partly by the input applied at and after $t_0$ . In using $definition(2.1)$, there is no more need to know the input applied before $t_0$  all the way back to $\infin$. Thus  $definition(2.1)$ is easier to track and will be called a state-input–output pair. 

*lumped* 

A system is said to be lumped if its number of state variables is ﬁnite or its state is a ﬁnite vector. 

*distributed*

A system is called a distributed system if its state has inﬁnitely many state variables. The transmission line is the most well known distributed system.

*linear system*
additivity, homogeneity and superposition
A system is called a linear system if for every $t_0$ and any two state-input–output pairs
$$
\left.
\begin{array}{l}{\mathbf{x}\left(t_{0}\right)} \\ {\mathbf{u}(t), t \geq t_{0}}\end{array}\right\} \rightarrow \mathbf{y}(t), \quad t \geq t_{0}
$$
for $i =1,2$, we have
$$
\left.
\begin{array}{rl}{\mathbf{x}_{1}\left(t_{0}\right)+\mathbf{x}_{2}\left(t_{0}\right)} & {} \\ {\mathbf{u}_{1}(t)+\mathbf{u}_{2}(t),} & {t \geq t_{0}}\end{array}\right\}  \rightarrow \mathbf{y}_{1}(t)+\mathbf{y}_{2}(t), \quad t \geq t_{0} \text { (additivity) }
$$
and 
$$
\left.
\begin{array}{l}{\alpha \mathbf{x}_{1}\left(t_{0}\right)} \\ {\alpha \mathbf{u}_{1}(t), \quad t \geq t_{0}}\end{array} \right\} \rightarrow \alpha \mathbf{y}_{1}(t), \quad t \geq t_{0} \text { (homogeneity) }
$$
for any real constant $\alpha$. The ﬁrst property is called the additivity property, the second, the homogeneity property. These two properties can be combined as
$$
\left.
\begin{array}{l}{\alpha_{1} \mathbf{x}_{1}\left(t_{0}\right)+\alpha_{2} \mathbf{x}_{2}\left(t_{0}\right)} \\ {\alpha_{1} \mathbf{u}_{1}(t)+\alpha_{2} \mathbf{u}_{2}(t), \quad t \geq t_{0}}\end{array} \right \} \rightarrow \alpha_{1} \mathbf{y}_{1}(t)+\alpha_{2} \mathbf{y}_{2}(t), \quad t \geq t_{0}
$$
for any real constants $\alpha_1$ and $\alpha_2$, and is called the superposition property. 

A system is called a nonlinear system if the superposition property does not hold.

*zero input response*

If the input $\mathbf{u}(t)$ is identically zero for $t \geq t_{0}$ , then the output will be excited exclusively by the initial state $\mathbf{x}\left(t_{0}\right).$ This output is called the zero-input response and will be denoted by$\mathbf{y}_{z i}$ or

$$
\left.
\begin{array}{l}{\mathbf{x}\left(t_{0}\right)} \\ {\mathbf{u}(t) \equiv \mathbf{0}, t \geq t_{0}}\end{array}\right \}\rightarrow \mathbf{y}_{z i}(t), \quad t \geq t_{0}
$$
*zero state response*

If the initial state $\mathbf{x}\left(t_{0}\right)$ is zero, then the output will be excited exclusively by the input. This output is called the zero-state response and will be denoted by $\mathbf{y}_{z s}$ or
$$
\left.
\begin{array}{rl}{\mathbf{x}\left(t_{0}\right)=}  {\mathbf{0}} \\ {\mathbf{u}(t),} 4 {t \geq t_{0}}\end{array}\right\} \rightarrow \mathbf{y}_{z s}(t), \quad t \geq t_{0}
$$


