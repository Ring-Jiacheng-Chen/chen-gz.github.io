---
title: Buck Converter
category: power electric
toc: true
---

# Buck Converter

## equations

$$
v_L = v_g - V \approx V_g -V
$$

$$
i_c = i_L - \frac{V}{R} = i_L - I_o \approx I - \frac{V}{R}
$$

$$
\frac{dv_c}{dt} = \frac{i_c}{C} \approx \frac{I-\frac{V}{R}}{C}
$$

$$
\frac{di_l}{dt} = \frac{v_L}{L} \approx \frac{V_g-V}{L}
$$

<!--more-->

## circuit

![buck converter](https://cdn.mathpix.com/snip/images/_M6gGUAHbPliyaCoPxV6vYsQCDwB-7SaTn7ctheyrTE.original.fullsize.png)



![](https://cdn.mathpix.com/snip/images/6ncIPCZr4oVCyAsn524icBYMQFKuZ3js368UPkgJEx4.original.fullsize.png)

## relationship of input and output voltage 

The relationship between input voltage $V_g$ and output voltage $ V_s$:
$$
V_{s}=\frac{1}{T_{s}} \int_{0}^{T_{s}} v_{s}(t) d t=D V_{g}
$$
![](https://cdn.mathpix.com/snip/images/6wZ77ncJ5ZgeRNXhQdlLnaOiIjSViMAlBRUxGmh9P1E.original.fullsize.png)



## DC component of $v_s(t)$

As illustrated in Fig. $2.2 .$ the integral is given by the area under the curve, or $D T_{s} V_{g}$ . The average value is
therefore
$$
\left\langle v_{s}\right\rangle=\frac{1}{T_{s}}\left(D T_{s} V_{g}\right)=D V_{g}
$$
So the average value, or DC component, of $v_{s}(t)$ is equal to the duty cycle times the DC input voltage $V_{g}$.

## the ripple of inductor current

The inductor voltage $v_{L}(t)$ is then given by
$$
v_{L}=V_{x}-v(t)
$$
The inductor voltage can be found by use of the definition
$$
v_{L}(t)=L \frac{d i_{L}(t)}{d t}
$$
![](https://cdn.mathpix.com/snip/images/bT4Tzk761_LDrkRgsfosMKTpqlKTMGXyLUZT0Sjrh54.original.fullsize.png)
![](https://cdn.mathpix.com/snip/images/LSS4uMGqIjjKZyB3UnhCjcWhyCErx4x-f8hgGjqnNE8.original.fullsize.png)
Thus, during the first interval, when $v_{L}(t)$ is approximately $\left(V_{x}-V\right),$ the slope of the inductor current waveform is
$$
\frac{d i_{L}(t)}{d t}=\frac{v_{L}(t)}{L} \approx \frac{v_{g}-v}{L}
$$

$$
\frac{d i_{L}(t)}{d t} \approx-\frac{V}{L}
$$

![](https://cdn.mathpix.com/snip/images/n_IxNkgfwePVTMnEdEOXx4y5g6MBJFjpzQCju7CXo_M.original.fullsize.png)

## the inductor current ripple $\Delta i_{L}$

since we know the slope of the inductor curring the first subinterval, and we also know the length of the first subinterval, we can calculate the ripple magnitude. The $i_{t}(t)$ waveform is symmetrical about $I,$ and hence during the first so the change in current increases by 2$\Delta i_{L}$ (since $\Delta i_{1}$ is the peak ripple, the peak-to-peak ripple is $2\Delta i_{l}$). So the change in current, $2 \Delta i_{L},$ is equal to the slope (the applied inductor voltage divided by $L$ ) times the length of the first subinterval $\left(D T_{s}\right)$ :
$$
\left(2 \Delta i_{L}\right)=\left(\frac{V_{g}-V}{L}\right)\left(D T_{\mathrm{s}}\right)
$$

$$
\Delta i_{L}=\frac{V_{g}-V}{2 L} D T_{\mathrm{s}}
$$

## the Capacitor voltage ripple $\Delta v_{C}$


### why can not use $\frac{dv_c}{dt}$ to calcutlate



### why need use $\Delta i_L$ to calculate

### the value of $\Delta v_C$

By the capacitor relation $Q=C V$
$$
q=C(2 \Delta v)
$$

$$
q=\frac{1}{2} \Delta i_{L} \frac{T_{s}}{2}
$$

$$
\Delta v=\frac{\Delta i_{L} T_{s}}{8 C}
$$





## reduce peak to peak ripple

The inductor value can be chosen such that a desired current ripple $\Delta i_{L}$ is attained. Solution of $Eq. (2.15)$ for the inductance $L$ yields
$$
L=\frac{V_{k}-V}{2 \Delta i_{L}} D T_{\mathrm{s}}
$$
![](https://cdn.mathpix.com/snip/images/1g0OPaNI3J_GFCqS2icfdgWoVawPDMRUhk7fNLv_Abk.original.fullsize.png)

## fit continue conduction mode get $L_{min}$

$$
L=\frac{V_{g}-V}{2 \Delta i_{l}} D T_{\mathrm{s}}
$$