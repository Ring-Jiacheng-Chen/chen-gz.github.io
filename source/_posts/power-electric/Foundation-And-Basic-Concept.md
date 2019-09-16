---
title: Foundation and Basic Concept
category: power electric
toc: true
---

*note: most things are copied from book, not write by myself and this book can get from Google. I only copy important things to here and add some comments.*

## symbols

Duty cycle: *D*

single pole double throw:  *SPDT*.

output voltage $v_{s}(t)$.

converter input voltage $V_{g}$. 

The complement of the duty ratio, $D^{\prime},$ is defined as $(1-D)$.
<!--more-->

## DC component of $v_s(t)$:

From Fourier analysis, we know that the DC component of $v_{s}(t)$ is given by its average value $\left\langle v_{s}\right\rangle,$ or
$$
\left\langle v_{s}\right\rangle=\frac{1}{T_{s}} \int_{0}^{T_{s}} v_{s}(t) d t
$$
## position of inductor 

The buck converter is just one of many possible switching converters. Two other commonly used converters, which perform different voltage conversion functions, are illustrated in Fig. $2.5 .$ In the boost converter, the positions of the inductor and switch are reversed.

## balance rule for inductor voltage and capacitor current

The principles of inductor volt-second balance and capacitor charge balance are derived; these can be used to solve for the inductor currents and capacitor voltages of switching converters. 

## small-ripple and linear-ripple approximation

![](https://cdn.mathpix.com/snip/images/UtGYcs5WNOTFcynd9FcgumtN21f0WcJOTF5930TkFKg.original.fullsize.png)



So it is nearly always a good approximation to assume that the magnitude of the switching ripple is much smaller than the DC component:
$$
\left|v_{\text {ripple}}\right|<V
$$
Therefore, the output voltage $v(t)$ is well approximated by its DC component $V,$ with the small ripple term $v_{ripple}(t)$ neglected:
$$
v(t) \approx V
$$
## inductor voltage and conductor current

### inductor voltage 

The inductor voltage can be found by use of the definition
$$
v_{L}(t)=L \frac{d i_{L}(t)}{d t}
$$

###  Capacitor current

$$
i_c(t) = C \frac{du_c(t)}{dt}
$$

## The balance of inductor and capacitor

### Inductor voltage balance 

the principle of inductor volt-second balance. Given the defining relation of an inductor:
$$
v_{L}(t)=L \frac{d i_{L}(t)}{d t}
$$
Integration over one complete switching period, say from $t=0$ to $T_{s}$ , yields
$$
i_{L}\left(T_{s}\right)-i_{L}(0)=\frac{1}{L} \int_{0}^{T_{s}} v_{L}(t) d t
$$
Therefore, in steady state the integral of the applied inductor voltage must be zero:
$$
0=\int_{0}^{T_{s}} v_{L}(t) d t
$$
### Capacitor current balance

Similar arguments can be applied to capacitors. The defining equation of a capacitor is
$$
i_{C}(t)=C \frac{d v_{C}(t)}{d t}
$$
Integration of this equation over one switching period yields
$$
v_{C}\left(T_{s}\right)-v_{C}(0)=\frac{1}{C} \int_{0}^{T_{s}} i_{C}(t) d t
$$

In steady state, the net change over one switching period of the capacitor voltage must be zero, so that the left-hand side of $Eq. (2.26)$ is equal to zero. Therefore, in equilibrium the integral of the capacitor current over one switching period (having the dimensions of amp-seconds, or charge) should be zero. There is no net change in capacitor charge in steady state. An equivalent statement is
This should be an intuitive result. If a DC current is applied to a capacitor, then the
$$
0=\frac{1}{T_{s}} \int_{0}^{T_{s}} i_{c}(t) d t=\left\langle i_{c}\right\rangle
$$
The average value, or DC component, of the capacitor current must be zero in equilibrium.

## continue conduction mode 

current must over zero, if not satisfied continue conduction mode, then when switch to  status 2, two component will off!

from continue conduction mode we can define $L_{min}$ to satisfy continue conduction mode.



## M(D) of various converter

![](https://cdn.mathpix.com/snip/images/eTfq0ninHSJSxUEnWNIkg5oEzPDzXGm8Kqjpk1MTh78.original.fullsize.png)