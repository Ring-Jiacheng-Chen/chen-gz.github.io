---

---

<!--
author: 小柯基
title: power ele
category: power-electric
status: publish
summary: 
-->

*note: most things are copied from book, not write by myself and this book can get from Google. I only copy import things to here and add some comments.*

[TOC]

# no title now

### symbols and some concepts

Duty cycle: *D*

single pole double throw:  *SPDT*.

output voltage $v_{s}(t)$.

converter input voltage $V_{g}$. 

The complement of the duty ratio, $D^{\prime},$ is defined as $(1-D)$.

### relationship of input and output voltage 

The relationship between input voltage $V_g$ and output voltage $ V_s$:
$$
V_{s}=\frac{1}{T_{s}} \int_{0}^{T_{s}} v_{s}(t) d t=D V_{g}
$$
![](https://cdn.mathpix.com/snip/images/6wZ77ncJ5ZgeRNXhQdlLnaOiIjSViMAlBRUxGmh9P1E.original.fullsize.png)

### DC component of $v_s(t)$:

From Fourier analysis, we know that the DC component of $v_{s}(t)$ is given by its average value $\left\langle v_{s}\right\rangle,$ or
$$
\left\langle v_{s}\right\rangle=\frac{1}{T_{s}} \int_{0}^{T_{s}} v_{s}(t) d t
$$
 As illustrated in Fig. $2.2 .$ the integral is given by the area under the curve, or $D T_{s} V_{g}$ . The average value is
therefore
$$
\left\langle v_{s}\right\rangle=\frac{1}{T_{s}}\left(D T_{s} V_{g}\right)=D V_{g}
$$
So the average value, or DC component, of $v_{s}(t)$ is equal to the duty cycle times the DC input voltage $V_{g}$.

### buck converter

The switch reduces the DC voltage by a factor of $D .$

buck converter
![buck converter](https://cdn.mathpix.com/snip/images/_M6gGUAHbPliyaCoPxV6vYsQCDwB-7SaTn7ctheyrTE.original.fullsize.png)

### use feedback system to control voltage

Feedback systems are often constructed that adjust the duty cycle $D$ to regulate the converter output voltage. Inverters or power amplifiers can also be built, in which the duty cycle varies slowly with time and the output voltage follows.

### position of inductor 

The buck converter is just one of many possible switching converters. Two other commonly used converters, which perform different voltage conversion functions, are illustrated in Fig. $2.5 .$ In the boost converter, the positions of the inductor and switch are reversed.

### buck-boost converter revert output voltage

Another converter, the buck-boost converter, can either increase or decrease the magnitude of the voltage, but the polarity is inverted. So with a positive input voltage, the ideal buck-boost converter can produce a negative output voltage of any magnitude. 

### balance rule for inductor voltage and capacitor current

The principles of inductor volt-second balance and capacitor charge balance are derived; these can be used to solve for the inductor currents and capacitor voltages of switching converters. 

### small-ripple and linear-ripple approximation

A useful approximation, the small-ripple or linear-ripple approximation, greatly facilitates the analysis. Some simple methods for selecting the filter element values are also discussed.

![](https://cdn.mathpix.com/snip/images/eTfq0ninHSJSxUEnWNIkg5oEzPDzXGm8Kqjpk1MTh78.original.fullsize.png)

![](https://cdn.mathpix.com/snip/images/6ncIPCZr4oVCyAsn524icBYMQFKuZ3js368UPkgJEx4.original.fullsize.png)

![](https://cdn.mathpix.com/snip/images/UtGYcs5WNOTFcynd9FcgumtN21f0WcJOTF5930TkFKg.original.fullsize.png)



So it is nearly always a good approximation to assume that the magnitude of the switching ripple is much smaller than the DC component:
$$
\left|v_{\text {ripple}}\right|<V
$$
Therefore, the output voltage $v(t)$ is well approximated by its DC component $V,$ with the small ripple term
$v_{ripple}(t)$ neglected:
$$
v(t) \approx V
$$
### the ripple of inductor voltage

The inductor voltage $v_{L}(t)$ is then given by
$$
v_{L}=V_{x}-v(t)
$$

By knowledge of the inductor voltage waveform, the inductor current can be found by use of the definition
$$
v_{L}(t)=L \frac{d i_{d}(t)}{d t}
$$
![](https://cdn.mathpix.com/snip/images/bT4Tzk761_LDrkRgsfosMKTpqlKTMGXyLUZT0Sjrh54.original.fullsize.png)
![](https://cdn.mathpix.com/snip/images/LSS4uMGqIjjKZyB3UnhCjcWhyCErx4x-f8hgGjqnNE8.original.fullsize.png)
Thus, during the first interval, when $v_{L}(t)$ is approximately $\left(V_{x}-V\right),$ the slope of the inductor current waveform is
$$
\frac{d i_{d}(t)}{d t}=\frac{v_{-}(t)}{L} \approx \frac{v_{x}-v}{L}
$$

$$
\frac{d i_{L}(t)}{d t} \approx-\frac{V}{L}
$$

![](https://cdn.mathpix.com/snip/images/n_IxNkgfwePVTMnEdEOXx4y5g6MBJFjpzQCju7CXo_M.original.fullsize.png)

the inductor current ripple $\Delta i_{L}$

### peak to peak ripple

since we know the slope of the inductor curring the first subinterval, and we also know the length of the first subinterval, we can calculate the ripple magnitude. The $i_{t}(t)$ waveform is symmetrical about $I,$ and hence during the first so the change in current increases by 2$\Delta i_{L}$ (since $\Delta i_{1}$ is the peak ripple, the peak-to-peak ripple is $ 2 \Delta i_{l}$). So the change in current, $2 \Delta i_{L},$ is equal to the slope (the applied inductor voltage divided by $L$ ) times the length of the first subinterval $\left(D T_{s}\right)$ :
$$
\left(2 \Delta i_{L}\right)=\left(\frac{V_{x}-V}{L}\right)\left(D T_{\mathrm{s}}\right)
$$

$$
\Delta i_{L}=\frac{V_{R}-V}{2 L} D T_{\mathrm{s}}
$$

#### reduce peak to peak ripple

The inductor value can be chosen such that a desired current ripple $\Delta i_{L}$ is attained. Solution of $Eq. (2.15)$ for the inductance $L$ yields
$$
L=\frac{V_{k}-V}{2 \Delta i_{L}} D T_{\mathrm{s}}
$$
![](https://cdn.mathpix.com/snip/images/1g0OPaNI3J_GFCqS2icfdgWoVawPDMRUhk7fNLv_Abk.original.fullsize.png)

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

#### 



current must over zero 

switch to  status 2! ! 

two component will off !!!! 



ccm 

continut conduct  mode 

have $L_{min}$



Q coil 

