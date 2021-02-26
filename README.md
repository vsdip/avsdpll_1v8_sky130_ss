# Characterization-TCL-flow-for-8x-PLL-Clock-Multiplier-for-sky130-Process-Corners

### Running the Simulation
1. Clone this repo. <br/>
2. Download and add `sky130_fd_pr` and `Sky130_Primitives` to the folder <br/>
3. cd <repo_name>/Prelayout <br/>
4. open the PLL_PreLay.cir and change .include /home/subham/Characterization-TCL-flow-for-8x-PLL-Clock-Multiplier-for-sky130-Process-Corners/sky130nm.lib accordingly . <br/>
5. Run the PLL circuit by typing `ngspice PLL_PreLay.cir` <br/>

The block diagaram of the PLL as a clock multiplier is as follows:
![](/images/pll_freq.png)
Here M = 8

Tested through spice simulations on skywater 130nm ss corner at room termperature

### PD Circuit ouput

![](/images/pd1.png)

![](/images/pd2.png)

Red: Clock 2 <br />
Blue: Clock 1 <br />
Orange: Up Signal <br />
Green: Down Signal
 
### Frequency Divider Circuit output

![](/images/fd.png)

Red: Output Clock <br />
Blue: Input Clock  <br />

### Charge Pump(CP) output

![](/images/cp.png)

Red: Charge Pump Output Voltage

### VCO Output

![](/images/vco.png)

### PLL Output

The PLL output from the prelayout simulation is as follows:


![](/images/pll3.png)

Red: Reference Clock <br />
Blue: Output Clock Divided by 8 <br />
Yellow: Down Signal <br />
Brown: Up Signal <br />
Pink (at top): ChargePump output  <br />

### Work done in week 3
1. Increased the xm44 pfet width from 480n to 640n in charge pum to fix the error it was causing.

![](/images/w3_!.png)

2. Changed transistor widths for FD.cir to fix the frequency

![](/images/w3_2.png)

3. Changed widths of lots of pfets in VCO. Was ablr to fix the voltage swings and levels but still having problem with the frequency.

![](/images/w3_3.png)

### Future Work
The main broblem remaining is to fix the frequency of the VCO. This is causing the error in the PLL.

### Aknowledgement 
This PLL IP was taken from Lakshmi S 's github page:  https://github.com/lakshmi-sathi/avsdpll_1v8
