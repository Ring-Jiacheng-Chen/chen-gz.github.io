## SEPIC-Converter 

Single-ended primary-inductor converter



Principle 

when mos on, the circuit work at status 1

from the firgure we can see that we have 3 circle.
$$
v_{L1} = V_g \\
i_{C1} = -i_{L2} \approx -I_{L2} \\
v_{L2} = v_{C1} \approx V_{C1} \\
i_{C2} = -\frac{v_o}{R} \approx -\frac{V_o}{R}
$$

$$
\frac{di_{L_1}}{dt} = \frac{v_{L1}}{L_1} = \frac{V_g}{L_1} \\
\frac{du_{C_1}}{dt} = \frac{i_{C_1}}{C_1} = \frac{-i_{L_2}}{C_1} \approx \frac{-I_{L_2}}{C_1} \\
\frac{di_{L_2}}{dt} = \frac{v_{L_2}}{L_2} = \frac{v_{C_1}}{L_2} \approx \frac{V_{C_1}}{L_2} \\
\frac{du_{C_2}}{dt} = \frac{i_{C_2}}{C_2} = -\frac{v_o}{RC_2} \approx -\frac{V_o}{RC_2} \\
$$

when mos off, the circuit work at status 2 

from the figure we have equations:
$$
v_{L1} = V_g - v_{C_1} - v_o \approx V_g - V_{C_1} - V_o\\
i_{C1} = i_{L_1} \approx I_{L_1} \\
v_{L2} = -v_o \approx -V_o \\
i_{C2} = i_{L_1} + i_{L_2} - \frac{v_o}{R} \approx I_{L_1} + I_{L_2} - \frac{V_o}{R}
$$

$$
\frac{di_{L_1}}{dt} = \frac{V_g-v_{C_1}-v_o}{L_1} = \frac{V_g-V_{C_1}-V_o}{L_1} \\
\frac{du_{C_1}}{dt} = \frac{i_{C_1}}{C_1} = \frac{i_{L_1}}{C_1} \approx \frac{I_{L_1}}{C_1} \\
\frac{di_{L_2}}{dt} = \frac{v_{L_2}}{L_2} = \frac{-v_0}{L_2} \approx \frac{-V_{o}}{L_2} \\
\frac{du_{C_2}}{dt} = \frac{i_{C_2}}{C_2} = \frac{i_{L_1}-\frac{v_o}{R}}{C_2} \approx \frac{I_{L_1}-\frac{V_o}{R}}{C_2}
$$

to set $<v_{L_1}> = 0$ 
$$
\frac{V_g}{L_1}DT_s + \frac{V_g - V_{C_1} - V_o}{L_1}D'T_s = 0
$$
to set $<i_{C_1}> = 0$
$$
\frac{-I_{L_2}}{C_1}DT_s + \frac{I_{L_1}}{C_1} D'T_s = 0
$$
to set $<u_{L_2}> = 0 $
$$
\frac{V_{C_1}}{L_2}DT_s - \frac{V_o}{L_2}D'T_s = 0
$$
to set $<i_{C_2}> = 0$
$$
-\frac{V_o}{RC_2}DT_s +\frac{I_{L_1} + I_{L_2} -\frac{V_o}{R}}{C_2}D'T_s = 0
$$
 from $equation (7)$  
$$
V_{C_1}D =  V_o D'
$$
from $euqation(5)$ 
$$
V_g D + (V_g - V_{C_1} - V_o)D' = 0 \\ 
V_g + (-\frac{V_oD'}{D} - V_o)D' =0 \\
V_o = \frac{V_g D}{D'}
$$
from $equation(9)$
$$
V_o = \frac{V_{C_1}D}{D'}
$$
assiociate $equation(9),(11)$

we get that 
$$
V_g = V_{C_1}
$$
from $equation(6)$
$$
-I_{L_2}D + I_{L_1}D' = 0 \\
I_{L_2} = \frac{I_{L_1}D'}{D}
$$


from $euqaiton (8)$
$$
-\frac{V_o}{R} +(I_{L_1}+I_{L_2})D' = 0\\
I_{L_1}+I_{L_2} = \frac{V_o}{RD'} = \frac{V_gD}{RD'D'} \\
I_{L_1}+\frac{I_{L_1}D'}{D} = \frac{V_gD}{RD'D'} \\
\frac{I_{L_1}}{D} = \frac{V_gD}{RD'D'} \\
I_{L_1} = (\frac{D}{D'})^2 \frac{V_g}{R}
$$
from $equation(13)$ 
$$
I_{L_2} =\frac{D}{D'} \frac{V_g}{R}
$$
use $\frac{du_{C_1}}{dt} = \frac{i_{C_1}}{C_1} = \frac{-i_{L_2}}{C_1} \approx \frac{-I_{L_2}}{C_1} \\$

we can get that 
$$
2 \Delta v_{C_1} = \frac{-I_{L_2}}{C_1}DT_s \\
\Delta v_{C_1} = \frac{D^2}{D'}T_S\frac{V_g}{2RC_1}
$$
use $\frac{du_{C_2}}{dt} = \frac{i_{C_2}}{C_2} = -\frac{v_o}{RC_2} \approx -\frac{V_o}{RC_2} \\$
$$
2\Delta v_o = \frac{V_o}{RC_2}DT_s \\
\Delta v_o = \frac{D^2}{D'}T_s\frac{V_g}{2RC_2}
$$
use $\frac{di_{L_1}}{dt} = \frac{v_{L1}}{L_1} = \frac{V_g}{L_1} $
$$
2\Delta i_{L_1} = \frac{V_g}{L_1}DT_s \\
\Delta i_{L_1} = \frac{V_g}{2L_1}DT_s \\
$$
use $\frac{di_{L_2}}{dt} = \frac{v_{L_2}}{L_2} = \frac{-v_0}{L_2} \approx \frac{-V_{o}}{L_2} \\$
$$
2\Delta i_{L_2} = \frac{V_o}{L_2}D'T_s \\
\Delta i_{L_2} = \frac{V_gD}{2L_2}T_s \\
$$
