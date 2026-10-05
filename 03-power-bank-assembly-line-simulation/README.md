# Power Bank Assembly Line Simulation (JaamSim)

A discrete-event simulation of a power bank assembly line, built in [JaamSim](https://jaamsim.com/) (free and open source).

## Model

- **9 suppliers** (Bengaluru, Delhi, Gurugram, Pune, Mumbai) deliver 9 component types: battery, casing, charging cable, LED, wire, input and output ports, protection circuit and power-management board. Each has its own arrival interval (2–20 min).
- **8 workstations** with service times: power-control unit (3.5 min), PCB assembly (5 min), terminal soldering (5 min), battery-to-PCB (1.5 min), DC power testing (3 min), housing (5 min), final test (10 min) and packaging (1.5 min).
- **5 assembly (combine) points** where sub-assemblies meet, 20 buffer queues, and a conveyor to shipping.

## Use

Open `model/power_bank_assembly_line.cfg` in JaamSim and press Run. The model can be used to study throughput, queue build-up between stations and supplier lead-time effects.

**Skills:** discrete-event simulation · production line design · bottleneck and buffer analysis
