# MOSET (NMOS) Characterization :


• Aim
• Design specifications
• Circuit description
• Simulation procedure
• Results
• Observations
• Conclusion


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
| 8 | VDS range | 0 – 1.2 V |

<br>

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

Refer the Simulations part. I uploaded the all plots 


## Observation :<br>


<table>
<tr style="background-color:#f8d7da;">
<th>Region</th><th>Condition</th><th>Formula</th>
</tr>
<tr style="background-color:#fff3cd;">
<td>Cutoff</td>
<td>Vgs &lt; Vth</td>
<td>ID = 0</td>
</tr>
<tr style="background-color:#d1ecf1;">
<td>Linear (Triode)</td>
<td>Vgs &gt; Vth and Vds &lt; (Vgs − Vth)</td>
<td>ID = μnCox(W/L) [(Vgs − Vth)Vds − Vds²/2]</td>
</tr>
<tr style="background-color:#d4edda;">
<td>Saturation</td>
<td>Vgs &gt; Vth and Vds ≥ (Vgs − Vth)</td>
<td>ID = ½ μnCox(W/L) (Vgs − Vth)²</td>
</tr>
</table>



1. Two regions seen: triode (low VDS) and saturation (high VDS).<br>
2. ID increases with both VGS and VDS, flattening in saturation.<br>
3. Threshold voltage estimated from onset of ID rise in Id-Vgs plot.<br>
4. Curves follow expected MOSFET square-law behavior.<br>

## Result :<br>

Refer the Simulations.

| S.No | Plot | Key Result |
|------|------|------------|
| 1 | Id vs Vgs (Vds = 1.2 V) | ID ≈ 0 below threshold, rises to ~0.93 mA at Vgs = 1.2 V |
| 2 | Id vs Vgs (Vds stepped) | Higher Vds → higher ID for same Vgs (channel length modulation) |
| 3 | Id vs Vds (Vgs = 1.2 V) | Triode rise, then saturates near ~0.93 mA |
| 4 | Id vs Vds (Vgs stepped) | Clear triode + saturation regions; higher Vgs → higher ID(sat) |
<br>


## Conclusion :
Drain and transfer characteristics were successfully simulated and match standard MOSFET theory, confirming correct model and setup. Results can be used to extract VTH and gm, and apply the gm/ID method for biasing.
