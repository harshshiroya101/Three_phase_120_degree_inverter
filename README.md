# Three-Phase 120-Degree Inverter

## Overview
This project contains a MATLAB/Simulink model (`Three_phase_120_degree_inverter.slx`) for studying the operation of a three-phase inverter using 120-degree conduction.

In 120-degree conduction mode, each power switch is commanded to conduct for 120 electrical degrees per cycle. The switching sequence is arranged so that three-phase AC output can be synthesized from a DC input.

## Project File
- `Three_phase_120_degree_inverter.slx` — MATLAB/Simulink model of the inverter.

## Requirements
- MATLAB
- Simulink
- Any additional Simulink toolboxes required by the blocks used in the model

The exact MATLAB release and toolbox requirements should be checked against the model's blocks.

## How to Run
1. Open MATLAB with Simulink installed.
2. Set the MATLAB Current Folder to the directory containing `Three_phase_120_degree_inverter.slx`.
3. Open the model in Simulink.
4. Check the DC input, switching pulse generation, inverter switches, load parameters, and measurement blocks.
5. Set the simulation stop time and solver settings as appropriate.
6. Click **Run** to simulate the inverter.
7. Inspect the gate pulses, phase voltages, line-to-line voltages, and phase currents using the available scopes or logged signals.

You can also open the model from the MATLAB Command Window:

```matlab
open_system('Three_phase_120_degree_inverter.slx');
```

## Operating Principle
A three-phase 120-degree conduction inverter typically uses six power switches. Each switch is gated for 120 electrical degrees, with switching commands displaced by 60 electrical degrees in sequence. At a given instant, two switches normally conduct—one connected to the positive DC bus and one to the negative DC bus—while the remaining phase is not actively connected to either DC rail during its non-conducting interval. The exact waveforms depend on the inverter topology, load, and switching implementation.

## Suggested Checks
- Confirm the six gate signals follow the intended 120-degree conduction sequence.
- Check that the gate pulses are correctly displaced in electrical angle.
- Verify DC-link voltage and load parameters.
- Inspect phase and line-to-line voltage waveforms.
- Check phase-current waveforms and whether they match the selected load model.
- Confirm that switch devices and solver settings are appropriate for the simulation.
- Look for unexpected simultaneous gating, current spikes, or numerical solver warnings.

## Expected Observations
For a conventional three-phase 120-degree conduction inverter, the output line-to-line voltages are typically six-step waveforms. Phase-voltage and current waveforms depend on the load connection and whether the load is resistive, inductive, or otherwise modeled. Use the simulation results from this model to document the actual behavior; no numerical results are assumed in this README.

## Notes
- This README is based on the model filename and the standard operating principle of a three-phase 120-degree conduction inverter. Confirm the actual topology, control logic, parameters, and waveforms by inspecting the supplied Simulink model.
- Add screenshots, parameter tables, and measured results if this project is being submitted as a lab or academic report.

## License
No license has been specified. Add a license if you intend to distribute the project.
