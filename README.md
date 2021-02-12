# Characterization-TCL-flow-for-8x-PLL-Clock-Multiplier-for-sky130-Process-Corners

The block diagaram of the PLL as a clock multiplier is as follows:
![](/images/pll_freq.png)
Here M = 8

Tested through spice simulations on skywater 130nm ss corner at room termperature

### PD Circuit ouput

![](/images/pd1.png)

![](/images/pd2.png)

Red: Clock 2
Blue: Clock 1
Orange: Up Signal
Green: Down Signal

### Frequency Divider Circuit output

![](/images/fd.png)

Red: Output Clock
Blue: Input Clock 

### Charge Pump(CP) output

![](/images/cp.png)

Red: Charge Pump Output Voltage

### VCO Output

![](/images/vco.png)

### PLL Output

The PLL output from the prelayout simulation is as follows:

![](/images/pll1.png)

![](/images/pll2.png)

Red: Reference Clock
Blue: Output Clock Divided by 8
Yellow: Down Signal
Brown: Up Signal
Pink (at top): ChargePump output 

### Future Work
1.We see that the frequency of the VCO output is less than what we expected, this is because we are using the slow corners and the delay is a lot. The goal in the next stage would be to fix this.
2. The overall output of PLL is not stable for long time and also the output frequency is less than desired valure, this is mainly due to VCO output frequency not matching up.

### Aknowledgement 
This PLL IP was taken from Lakshmi S 's github page:  https://github.com/lakshmi-sathi/avsdpll_1v8
