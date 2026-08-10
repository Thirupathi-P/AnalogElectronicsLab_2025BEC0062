# MOSET (NMOS) Characterization :


• Aim
• Design specifications
• Circuit description
• Simulation procedure
• Results
• Observations
• Conclusion


## Aim :
        
   To obtain and plot the drain characteristics and transfer characteristics of an NMOS transistor using circuit simulation software <br>
   (Cadence Virtuoso, ADE-L) and to use the gm/ID methodology to design the device for a target bias current.

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
| 8 | VDS range | 0 – 1.2 V |


## Circuit description : <br>
A single NMOS transistor (NM0) is connected between two DC sources — Vds at the drain and Vgs at the gate. Source and bulk are tied to ground. This setup allows sweeping one voltage while fixing or stepping the other, to obtain both transfer (Id-Vgs) and drain (Id-Vds) characteristics.<br>
<img width="1776" height="930" alt="image" src="https://github.com/user-attachments/assets/5be512dc-4cef-469d-b1df-f6cc976fc9df" />
<br>




##  Simulation procedure :
|S.No |Plot|	Swept variable|	Fixed / stepped variable|
|----|------|----------------|---------------------------|
|1|Id vs Vgs (constant Vds)|	Vgs: 0 → 1.2 V	|Vds = 1.2 V (constant)|
|2|Id vs Vgs (for different values of Vds)	|Vgs: 0 → 1.2 V |	Vds = 0, 0.3, 0.6, 0.9, 1.2 V|
|3|Id vs Vds (constant Vgs)	|Vds: 0 → 1.2 V	|Vgs = 1.2 V (constant)|
|4|Id vs Vds (for different values of Vgs)	|Vds: 0 → 1.2 V	|Vgs = 0, 0.3, 0.6, 0.9, 1.2 V|


## Result :


 
## Observation :<br>
1.Two regions seen: triode (low VDS) and saturation (high VDS).<br>
2.ID increases with both VGS and VDS, flattening in saturation.<br>
3.Threshold voltage estimated from onset of ID rise in Id-Vgs plot.<br>
4.Curves follow expected MOSFET square-law behavior.<br>

## Conclusion :
Drain and transfer characteristics were successfully simulated and match standard MOSFET theory, confirming correct model and setup. Results can be used to extract VTH and gm, and apply the gm/ID method for biasing.
