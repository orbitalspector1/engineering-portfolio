# EV High-Current Connector (50 V / 100 A)

**Narsipur Group, BITS Pilani Practice School** · Product Design Intern · Jul 2026 – present

> This is ongoing industry work under IP restriction. CAD, drawings and reports are not shared here. I'm happy to walk through the design in an interview.

## Summary

I owned the casing and locking design of a new EV connector, from market analysis to an FEA-checked design ready for prototyping quotes.

## What I did

- **Commercial assessment:** sized volume, 5-year CAGR and TAM for 18 applications using bottom-up proxy models. Mapped 41 supplier spring-contact configurations to SKUs and found that bought-in contacts cover 37.5% of product tiers, which hold 72.8% of volume.
- **Requirements:** graded every input by evidence quality and kept a cited register of 64 assumptions. Traced an inherited cycle-life target back to its source and, with manager approval, reset it from 10,000 to 500–2,000 matings.
- **Design:** 14 SolidWorks parts, 3 assemblies mated on real fit faces, an 11-drawing release set, a design-calculation workbook and an 8-tool injection-moulding BOM.
- **Design reviews:** found and fixed a non-engaging latch, a duplicate hard stop and an unsealed cavity before drawing release.
- **Tolerancing:** Monte Carlo tolerance stack-up; relaxed two 0.04 mm bands that no function needed, to ease moulding.
- **FEA:** set up a Gmsh + CalculiX workflow, validated within 4% of beam theory. Caught an over-constrained latch (~344 N to mate) before tooling. The redesign meets USCAR-2 retention (≥151 N vs 110 N required), with a fatigue safety factor ≥1.67 at 4,000 cycles.
- **Vendor outreach for prototyping:** reached out to moulding, 3D-printing and seal vendors; issued 3 RFQ packages (moulding, 3D printing, seals) and compared 7 vendors on MOQ, lead time and capability.

## Status

The results so far are from simulation. A first-article drop test is recommended for the latch side before tooling.

## Skills

Product development · DFM for injection moulding · FEA · GD&T and tolerance analysis · requirements engineering · market sizing · supplier sourcing

**Tools:** SolidWorks, Gmsh, CalculiX, Python (NumPy, Matplotlib), Excel, Git · **Standards:** USCAR-2, IP67 (IEC 60529 / ISO 20653), IEC 62196
