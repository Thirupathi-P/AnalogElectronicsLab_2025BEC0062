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

## Design specification :




## Circuit description :




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
