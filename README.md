# Analog Electronics Lab

## Cadence Lab Experiments

**Tools:** Cadence Virtuoso (ADE L, Spectre), Assura (DRC, LVS), Quantus QRC, gpdk090 (90 nm CMOS PDK)

- EXP - 1 : MOSFET (NMOS) Characterization
- EXP - 2 : CMOS Inverter Layout
- EXP - 3 : Current Mirror
- EXP - 4 : Differential Amplifier

## Repository Structure

| Experiment | Description |
|---|---|
| [Experiment01_NMOS_Characterization](./Experiment01_NMOS_Characterization) | NMOS transfer and drain characteristics using ADE-L, and gm/ID based device sizing |
| [Experiment02_CMOS_Inverter_Layout](./Experiment02_CMOS_Inverter_Layout) | CMOS inverter schematic-to-layout flow, DRC/LVS, parasitic extraction (QRC) and pre- vs post-layout delay comparison |
| [Experiment03_Current_Mirror](./Experiment03_Current_Mirror) | Simple and cascode current mirror design using the gm/ID methodology |
| [Experiment04_Differential_Amplifier](./Experiment04_Differential_Amplifier) | Resistive-load differential amplifier (DC and AC analysis, CMRR) and 5T-OTA |

Each experiment folder contains its own `README.md` with the objective, design parameters and results, along with schematic screenshots, simulation setups, waveforms, and a final `Report.pdf`.
