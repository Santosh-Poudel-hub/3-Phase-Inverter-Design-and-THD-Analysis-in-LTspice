# 3-Phase Inverter Design and THD Analysis in LTspice

This project demonstrates the design and simulation of a balanced 3-phase inverter using Sinusoidal Pulse Width Modulation (SPWM). The simulation focuses on power quality metrics, specifically achieving grid-compliance levels for Total Harmonic Distortion (THD).

## Technical Specifications
- **Topology:** 3-Phase Bridge Inverter
- **Fundamental Frequency:** 50 Hz
- **Control Strategy:** SPWM
- **Output:** Balanced 3-phase current

## Simulation Performance
The model was simulated for 500ms to ensure steady-state stability, bypassing initial startup transients. Fourier analysis was performed on the output currents (I(L1), I(L2), I(L3)) up to the 40th harmonic.

### Key Results:
- **THD:** ~0.59% (Verified across all phases)
- **Phase Separation:** Precise 120° displacement (147.50°	, -92.52°	, 27.46°)
- **DC Offset:** -0.026A (Negligible bias)

## Repository Contents
- `Draft2.asc`: LTspice schematic file
- `Results/`: Screenshots of waveforms and SPICE error logs for Fourier components

## How to Run
1. Open `Draft2.asc` in LTspice.
2. Run the transient simulation (set for 500ms).
3. View the SPICE Error Log (`Cmd+L` on Mac) to verify THD results.
