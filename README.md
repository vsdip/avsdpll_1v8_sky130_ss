# Characterization-TCL-flow-for-8x-PLL-Clock-Multiplier-for-sky130-Process-Corners

The block diagaram of the PLL as a clock multiplier is as follows:
![](/images/pll_freq.png)
Here M = 8

Tested through spice simulations on skywater 130nm ss corner at room termperature

### PD Circuit ouput

![](/images/pd1.png)
![](/images/pd2.png)

### FD Circuit output
![](/images/fd.png)

### Charge Pump(CP) output
![](/images/cp.png)

### VCO Output
![](/images/vco.png)

### Future Work
We see that the frequency of the VCO output is less than what we expected, this is because we are using the slow corners and the delay is a lot. The goal in the next stage would be to fix this.

### Aknowledgement 
This PLL IP was taken from Lakshmi S 's github page:  https://github.com/lakshmi-sathi/avsdpll_1v8
