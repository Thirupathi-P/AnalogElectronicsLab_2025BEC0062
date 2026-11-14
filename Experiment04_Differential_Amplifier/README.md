# Experiment 04 – Differential Amplifier

**Course:** Analog Electronics
**Author:** Thirupathi P, B.Tech ECE, IIIT Kottayam
**Tools:** Cadence Virtuoso (ADE L, Spectre), gpdk090 (90 nm CMOS, `nmos1v`, `pmos1v`)

## Objective
Design and simulate a differential amplifier and study its differential-mode and common-mode gain using DC and AC analysis, then extend the design to a 5-transistor OTA (5T-OTA).

## Design Specifications
| Circuit | Parameters |
|---|---|
| Resistive-load differential amplifier | VDD = 1.2 V, ISS = 200 µA, RD = 5 kΩ, W/L = 2 µm / 100 nm |
| 5T-OTA | VDD = 2.5 V, Ibias = 30 µA, W/L = 120 nm / 100 nm |

## Folder Structure
```
Experiment04_Differential_Amplifier
├── README.md
├── Schematic/     # circuit schematics, 5T-OTA symbol, testbench
├── Simulation/    # ADE L setups, parametric analysis, source properties, theory notes
├── Waveforms/     # DC, AC, transient output plots
└── Report.pdf     # full lab report
```

## Results Summary
| Quantity | Result |
|---|---|
| Common-mode output at Vi1 − Vi2 = 0 | Vx = Vy = 0.7 V (ID1 = ID2 = 100 µA) |
| Single-ended output swing | 0.2 V to 1.2 V |
| Differential output saturation | ±ISS·RD = ±1.0 V |
| Mid-band differential gain Ad | ≈ 15.54 dB (5.98 V/V) |
| −3 dB bandwidth | ≈ 20 GHz |
| Single-ended gain (Vx or Vy) | ≈ 2.99 V/V (9.52 dB), half of Ad |
| Common-mode gain Acm (low freq.) | ≈ −127.3 dB |
| CMRR (low freq.) | ≈ 142.8 dB |
| 5T-OTA DC transfer | Vout swings 2.5 V → ≈ 1.18 V around V1 ≈ 1.5–1.6 V (V2 = 1.6 V) |

## Contents
- **DC analysis:** Vx, Vy vs (Vi1 − Vi2); ID1, ID2 vs (Vi1 − Vi2); (Vx − Vy) vs (Vi1 − Vi2)
- **AC analysis:** differential gain (dB20), single-ended gain, common-mode gain, common-mode differential gain
- **5T-OTA:** active PMOS current-mirror load schematic, custom symbol, testbench, DC/AC/transient analysis

See `Report.pdf` for full observations.
