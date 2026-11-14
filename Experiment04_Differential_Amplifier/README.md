# Experiment 04: Differential Amplifier
 
## 1. Aim
To design a differential amplifier, verify that all transistors operate in saturation, and measure its differential gain, common-mode gain, CMRR, bandwidth, input common-mode range and power consumption.
 
## 2. Design Specifications
| Parameter | Value |
|---|---|
| Technology | GPDK 90 nm |
| Supply (Vdd) | 1.2 V |
| Tail current (Itail) | [value] µA |
| Input pair (W/L) | [value] |
| Load type | [resistive / current-mirror active load] |
| Load (W/L or R) | [value] |
| Tail transistor (W/L) | [value] |
| Load capacitance | [value] fF |
| Target differential gain | [value] dB |
 
## 3. Circuit Description
The circuit has an NMOS input pair (M1, M2) with a common source node, a tail current source (M5) biased by a current mirror, and a [resistive / PMOS current-mirror] load (M3, M4).
 
The tail current splits equally between the two branches when the inputs are equal. A differential input unbalances the currents and produces a differential output.
 
Key equations:
- Differential gain: Ad ≈ gm1 × (ro2 || ro4) for an active load, or gm1 × RD for a resistive load
- CMRR = |Ad / Acm|
- Power = Vdd × (Itail + Ibias)
 
![Schematic](Schematic/diff_amp_schematic.png)
 
## 4. Simulation Procedure
1. Draw the schematic and the testbench with the supply, the bias current and the input sources.
2. Run an operating-point analysis and confirm that all transistors are in saturation.
3. Run a DC sweep of the differential input to get the transfer characteristic and output swing.
4. Run an AC analysis with a differential input (1 V AC, opposite phase on each side) to get Ad and the 3 dB bandwidth.
5. Run an AC analysis with a common-mode input (same AC on both inputs) to get Acm.
6. Compute CMRR = Ad / Acm (in dB: Ad(dB) - Acm(dB)).
7. Sweep the input common-mode voltage to find the input common-mode range (ICMR).
8. Run a transient analysis with a small sine input to check linearity.
9. Measure the average supply current and compute the power.
 
## 5. Results
**DC operating point**
![DC OP](Results/DC_operating_point.png)
 
**DC transfer characteristic**
![DC](Results/DC_transfer.png)
 
**AC response (differential gain and bandwidth)**
![AC](Results/AC_gain.png)
 
**Common-mode gain and CMRR**
![CMRR](Results/CMRR.png)
 
**Transient response**
![Transient](Results/Transient.png)
 
| Parameter | Value |
|---|---|
| Differential gain (Ad) | [value] dB |
| 3 dB bandwidth | [value] MHz |
| Common-mode gain (Acm) | [value] dB |
| CMRR | [value] dB |
| ICMR | [value] V to [value] V |
| Output swing | [value] V to [value] V |
| Power consumption | [value] µW |
 
## 6. Observations
- All transistors operate in saturation at the chosen bias point.
- The gain is flat at low frequency and rolls off beyond the 3 dB bandwidth because of the load capacitance.
- A larger tail-source output resistance gives a lower Acm and a higher CMRR.
- The output stays linear only for small differential inputs, and saturates once the tail current is steered fully to one side.
 
## 7. Conclusion
The differential amplifier amplifies the difference between the inputs and rejects the common-mode signal. The gain, bandwidth, CMRR and power in the table above summarise its performance, and a larger tail-source output resistance or a longer input-pair channel would trade speed for higher gain and CMRR.
 
