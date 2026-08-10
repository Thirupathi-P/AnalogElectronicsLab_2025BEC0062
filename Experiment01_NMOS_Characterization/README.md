# MOSET (NMOS) Characterization :

• Aim
• Design specifications
• Circuit description
• Simulation procedure
• Observations
• Conclusion
• Results

## Aim :<br>
        
   To obtain and plot the drain characteristics and transfer characteristics of an NMOS transistor using circuit simulation software (Cadence Virtuoso, ADE-L) and to use the gm/ID methodology to design the device for a target bias current.<br>
   
## Design specification :<br>
| S.No | Parameter | Value |
|------|-----------|-------|
| 1 | Technology | GPDK090 (90nm) |
| 2 | Device model | gpdk090_nmos1v |
| 3 | Width (W) | 1 µm |
| 4 | Length (L) | 100 nm |
| 5 | Multiplier (m) | 1 |
| 6 | Supply voltage (VDD) | 1.2 V |
| 7 | VGS range | 0 – 1.2 V |
|8 | VDS range | 0 – 1.2 V |

<br>

## Circuit description : <br>
Draw the NMOS schematic in Virtuoso with Vgs and Vds bias sources connected to the device terminal. <br>[Note : Body and Source are Connected]
<br>
<img width="1776" height="930" alt="image" src="https://github.com/user-attachments/assets/5be512dc-4cef-469d-b1df-f6cc976fc9df" />
<br>

##  Simulation procedure :

Before proceed to Simulation, we need  to check our schematic by check and save. Now, Run the DC Operating point Analysis in ADE-L and plot the graph. Note the region of operation.

Parameter Analysis :
Use Tools -> Parametric Analysis to sweep the variable in the circuit.

|S.No |Plot|	Swept variable|	Fixed / stepped variable|
|----|------|----------------|---------------------------|
|1|Id vs Vgs (constant Vds)|	Vgs: 0 → 1.2 V	|Vds = 1.2 V (constant)|
|2|Id vs Vgs (for different values of Vds)	|Vgs: 0 → 1.2 V |	Vds = 0, 0.3, 0.6, 0.9, 1.2 V|
|3|Id vs Vds (constant Vgs)	|Vds: 0 → 1.2 V	|Vgs = 1.2 V (constant)|
|4|Id vs Vds (for different values of Vgs)	|Vds: 0 → 1.2 V	|Vgs = 0, 0.3, 0.6, 0.9, 1.2 V|

Refer the Simulations part. I uploaded the plots.


## Observation :

<br> The drain current of an MOS transistor depends on the applied gate voltage.<br>
• When Vgs < Vth, the transistor remains OFF.  <br>
• As VGS exceeds the threshold voltage (Vth), a conductive channel is formed between drain and source.  <br>
• Beyond threshold, the drain current increases rapidly with increasing gate voltage, indicating strong inversion. <br>
• Current flow from Drain to Source.

## Conclusion :
<br> Refer the Simulations. <br>

Based on the Simulation.
1. CUT-OFF        : Vgs < Vth<br>
2. ON             : Vgs > Vth<br>
3. LINEAR REGION  : Vds < Vgs- Vth<br>
4. SATURATION     : Vds >= Vgs-Vth<br>


## Result:
The drain and transfer characteristics NMOS device were obtained, the region of operation was Verifed from DC operating Point.

