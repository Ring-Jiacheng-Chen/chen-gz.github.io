---
title: Buck Boost Converter
category: power electric
toc: true
---

# Buck Boost Converter

### buck-boost converter revert output voltage

Another converter, the buck-boost converter, can either increase or decrease the magnitude of the voltage, but the polarity is inverted. So with a positive input voltage, the ideal buck-boost converter can produce a negative output voltage of any magnitude. 

<!--more-->

### circuit

![](Buck-Boost-Converter.png)

## why this is a buck-boost converter

when mos on, the circuit at status 1: 
$$
v_L = V_g \\
i_C = \frac{v}{R} \approx \frac{V}{R} \\
\frac{di_L}{dt} = \frac{v_L}{L} \approx \frac{V_g}{L} \\
\frac{dv_C}{dt} = \frac{i_C}{C} = \frac{v}{RC} \approx \frac{V}{RC}
$$
when mos off, the circuit at status 2:
$$
v_L = v \approx V \\
i_C = i_L + i_o \approx I_L + I_o \\
\frac{di_L}{dt} = \frac{v_L}{L} = \frac{v}{L} \approx \frac{V}{L} \\
\frac{dv_C}{dt} = \frac{i_C}{C} = \frac{i_L + i_0}{C} \approx \frac{I_L+I_o}{C}
$$
to find out the relationship between input voltage and output voltage equate $<v_L> = 0$.

$$
\frac{V_g}{L}DT_s + \frac{V}{L}D'T_s = 0
$$
then
$$
V = -\frac{V_g D }{D'}
$$

from the formula, when $D<D'$ is a buck converter. Otherwise this is a boost converter.

we can figure out that 
$$
D = \frac{V}{V-V_g}
$$




 set $<i_C> = 0$

$$
\frac{V}{RC}DT_s + \frac{I_L+I_o}{C}D'T_s = 0
$$

$$
I_o = -I_L D' \\ 
I_L = -\frac{I_o}{D'} = -\frac{V}{RD'}
$$

### ripple

to find $\Delta i_L$ notice that $\frac{di_L}{dt}$ so we can get that 
$$
2\Delta i_L = \frac{V_g}{L}DT_s
$$
to find $\Delta v$ notice that $\frac{dv_C}{dt}$ and $v_C = v $ so we can get that 
$$
2\Delta v_C = \frac{V}{RC}DT_s \\
\Delta v_C = \frac{-V_g D^2 T_s} {2RC(1-D)}
$$

  