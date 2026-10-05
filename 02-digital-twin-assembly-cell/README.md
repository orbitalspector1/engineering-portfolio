# Digital Twin of a Laser-Engraving Assembly Cell

**BITS Pilani WILP, SMCC Lab** · Aug 2026 – present

> Work in progress. Model code and machine data are kept internal for now; this page describes the project.

## The cell

A five-station lab cell. A magazine feeds wooden blocks onto 3 conveyors, pneumatic cylinders transfer them, a platform lifts each block for laser engraving, and the block is ejected to a bin. It runs on a Siemens S7 PLC with Janatics pneumatics and a SCADA PC.

## What I did

- Wrote the 42-step operating sequence that the model reproduces, covering two routes (engrave and bypass).
- Measured the cell: conveyor lengths, all 10 proximity-sensor positions, workpiece size and mass, and platform travel. Documented cylinder and valve nameplates and converted vendor CAD to STEP.
- Extracted the machine-history database from the SCADA PC (10 real cycles) and measured operator dwell (n = 7, mean 14.0 s, range 6–29 s).
- Made the scope decisions: fidelity to the real machine over runtime, and Siemens NX MCD as the final twin platform. Specified operator-in-the-loop input (engrave/skip, then "engraving done").
- Led development of a MATLAB/Simulink/Stateflow physics model (11 pneumatic actuators on 13 solenoid coils, conveyors, contact, and a 44-state PLC sequencer), and validated it against measured data.

## Results so far

- Calibrated against 10 real PLC cycles: cycle-time error cut from 3.4x to 1.12x (57.4 s modelled vs 64.0 s measured).
- Cycle time modelled as a distribution using a Monte Carlo operator model, not a constant.
- Sensitivity sweep: of 78 unmeasured parameters, only 4 shift machine time by more than 1%, so those are the next to measure.
- 233 model parameters each tagged by source (measured, vendor, assumed); 121 PLC tags mapped.

## Next

Build the Siemens NX MCD model and connect it to PLC data over OPC UA. Close the remaining ~12% timing gap by measuring the 4 sensitive parameters.

**Tools:** MATLAB, Simulink, Stateflow, Simulink Test, Python, SQLite, Git, Siemens TIA Portal (read-only), OPC UA, Siemens NX MCD
