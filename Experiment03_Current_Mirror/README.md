# Experiment 03 – Design of Simple and Cascode Current Mirror

**Course:** Analog Electronics
**Author:** Thirupathi P, B.Tech ECE, IIIT Kottayam
**Tools:** Cadence Virtuoso (ADE L, Spectre), gpdk090 (90 nm CMOS, `nmos1v`)

## Objective
Design and simulate simple and cascode current mirrors, sized with the gm/ID methodology, to produce an output current of 1 mA, and study their current-transfer characteristics (ID vs VDS). Also size the mirrors for 2 mA.

## Design Method (gm/ID)
1. Sweep Vgs on a single NMOS (L = 100 nm, W = 1 µm, Vds = 1.2 V) and plot **ID/W vs gm/ID**.
2. At gm/ID = 15, read ID/W = 26.05 µA/µm.
3. Compute width: W = Iout / (ID/W).

| Iout | gm/ID | ID/W | W | L |
|---|---|---|---|---|
| 1 mA | 15 | 26.05 µA/µm | 38.38 µm | 100 nm |
| 2 mA | 15 | 26.05 µA/µm | 76.76 µm (or keep W and set I_REF = 2 mA) | 100 nm |

## Folder Structure
```
Experiment03_Current_Mirror
├── README.md
├── Schematic/     # NMOS sizing, simple mirror, cascode mirror schematics
├── Simulation/    # ADE L setup, design calculation tables
├── Waveforms/     # ID/W vs gm/ID, ID vs VDS plots
└── Report.pdf     # full lab report
```

## Results Summary
- The cascode mirror gives a flatter ID vs VDS curve (higher output resistance) and holds ≈ 1 mA across the sweep, closely matching I_REF.
- The simple mirror's output current keeps rising beyond 1 mA as VDS increases (channel-length modulation), so its mirroring accuracy is poor.
- Trade-off: the cascode needs a larger minimum output voltage (compliance voltage) to keep all devices in saturation.

See `Report.pdf` for full details.
