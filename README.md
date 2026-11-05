# TCAD Simulation and Electrical Characterization of a 4H-SiC Planar-Gate Power DMOSFET

<p align="center">
  <strong>Device Physics | Power Semiconductor Devices | TCAD | Silvaco ATLAS</strong>
</p>

---

## 1. Project Overview

This project presents a two-dimensional Technology Computer-Aided Design (TCAD) investigation of a vertical, n-channel, planar-gate 4H-Silicon Carbide (4H-SiC) Double-Diffused MOSFET (DMOSFET).

The study focuses on the physical structure, electrical characteristics, conduction mechanisms, and numerical behaviour of a representative 4H-SiC power MOSFET using **Silvaco ATLAS**.

The device is investigated through numerical simulations of its transfer characteristics, output characteristics, and off-state drain-voltage response. Particular attention is given to threshold-voltage extraction, subthreshold behaviour, specific ON-state resistance, JFET-region conduction, and the distribution of voltage within the device.

Rather than treating the device solely as a set of electrical characteristics, this project also examines the relationship between device geometry, doping concentration, electric-field distribution, and conduction resistance.

## 2. Research Objectives

The primary objectives of this investigation are:

- Develop a two-dimensional model of a vertical planar-gate 4H-SiC DMOSFET.
- Investigate the influence of device geometry and doping profiles on electrical behaviour.
- Obtain transfer and output characteristics under different gate-bias conditions.
- Extract threshold voltage and subthreshold swing from simulated transfer characteristics.
- Estimate specific ON-state resistance and examine its constituent contributions.
- Investigate JFET-region resistance and current-spreading effects.
- Analyse off-state leakage-current behaviour under increasing drain voltage.
- Examine electric-field and potential distributions within the semiconductor structure.
- Compare numerical simulation results with analytical semiconductor-device calculations.

## 3. Device Architecture and Specifications

The simulated structure represents a vertical n-channel 4H-SiC planar-gate DMOSFET.

### Principal device parameters

| Parameter | Value |
|---|---:|
| Semiconductor material | 4H-SiC |
| Device configuration | Vertical DMOSFET |
| Channel type | N-channel |
| Gate configuration | Planar gate |
| Cell pitch | 6.0 µm |
| Simulated half-cell width | 3.0 µm |
| Gate oxide thickness | 35 nm |
| Channel length | 0.5 µm |
| Drift-region thickness | 7.0 µm |
| Drift-region doping | 2 × 10¹⁶ cm⁻³ |
| Substrate thickness | 3.0 µm |
| Substrate doping | 2 × 10¹⁸ cm⁻³ |
| JFET-region width | 0.8 µm (full width) |
| Temperature | 300 K |

### Device regions

The simulated device consists of the following principal regions:

- **N+ source:** Provides the electron injection region.
- **P-well:** Forms the body region and accommodates the inversion channel.
- **N-type JFET region:** Provides the current path between adjacent P-wells.
- **N-type drift region:** Supports the applied drain voltage in the off-state.
- **N+ substrate:** Provides the low-resistance drain-side region.
- **Gate oxide and polysilicon gate:** Control the formation of the inversion channel.
- **Source and drain contacts:** Define the electrical terminals of the device.

## 4. Simulation Environment

| Component | Description |
|---|---|
| TCAD software | Silvaco ATLAS |
| Deck environment | DeckBuild |
| Plotting software | TonyPlot |
| Device modelling | Two-dimensional numerical simulation |
| Semiconductor material | 4H-SiC |
| Temperature | 300 K |
| Carrier transport | Drift-diffusion |
| Mobility modelling | Concentration- and field-dependent mobility |
| Recombination | Shockley-Read-Hall (SRH) |
| Impact ionization | SELB model for off-state analysis |
| Numerical methods | Gummel and Newton solution methods |

The simulation employs equilibrium initialization followed by bias-dependent electrical analysis. Different numerical solution strategies are used for on-state and off-state investigations to improve convergence.

## 5. Electrical Characterization

### 5.1 Transfer Characteristics (ID–VGS)

Transfer characteristics are obtained by sweeping the gate-to-source voltage from 0 V to 15 V at a constant drain-to-source voltage of 0.1 V.

Both linear and logarithmic current representations are used to examine the device response.

The logarithmic representation is particularly useful for investigating subthreshold current behaviour and the transition between the OFF-state and ON-state.

**Parameters investigated:**
- Threshold voltage (VTH)
- Maximum transconductance (gm)
- Subthreshold swing (SS)
- ON/OFF current ratio
- Gate-controlled channel formation

### 5.2 Output Characteristics (ID–VDS)

Output characteristics are investigated at different gate-to-source voltages of 5 V, 10 V, and 15 V.

The drain voltage is swept from 0 V to 10 V to examine the transition from the linear region towards saturation.

This analysis provides insight into:
- Gate-controlled drain current.
- Linear-region conduction.
- Saturation behaviour.
- Current enhancement with increasing gate overdrive.
- The influence of series and JFET-region resistance.

### 5.3 Off-State Breakdown and Leakage Analysis

The off-state response is investigated with the gate terminal held at 0 V while the drain voltage is increased.

The analysis examines:
- Drain leakage-current evolution.
- Electric-field development.
- Impact-ionization behaviour.
- Numerical convergence at high drain bias.
- Current-based leakage and breakdown-related criteria.

Both linear and logarithmic current plots are used to distinguish low-current leakage behaviour from the rapid increase in drain current at elevated drain voltages.

**Important:** The highest simulated drain voltage and the onset of a leakage-current criterion are not automatically equivalent to a validated physical breakdown voltage. Numerical convergence limitations and the underlying breakdown mechanism must be considered when interpreting these results.

## 6. Electrical Parameter Extraction

The principal extracted and calculated quantities include:

| Parameter | Preliminary result |
|---|---:|
| Threshold voltage (VTH) | 8.43 V |
| Subthreshold swing (SS) | 147 mV/dec |
| Maximum transconductance (gm) | 1.91 mS/mm |
| Drain current at VGS = 15 V, VDS = 0.1 V | 1.45 mA/mm |
| Drain current at VGS = 10 V, VDS = 10 V | 39.9 mA/mm |
| Drain current at VGS = 15 V, VDS = 10 V | 80.0 mA/mm |
| Specific ON-resistance (RON,sp) | 2.08 mΩ·cm² |
| Channel resistance contribution | Approximately 3% |
| Gate-independent resistance contribution | Approximately 97% |

These values represent preliminary results from the specified simulation structure and bias conditions. They should not be interpreted as experimentally measured device specifications.

## 7. ON-State Resistance Decomposition

A significant part of this work investigates the contribution of the inversion channel and the gate-independent conduction path to the overall ON-state resistance.

The analysis uses a gate-voltage-dependent conductance model to separate the channel-dependent contribution from the approximately gate-independent resistance.

The investigation considers:

- Channel resistance.
- Drift-region resistance.
- JFET-region resistance.
- Current-spreading resistance.
- Source-side and contact-related resistance.

The preliminary resistance analysis indicates that the channel contributes approximately 3% of the extracted total resistance, while the remaining resistance is predominantly associated with the gate-independent conduction path.

This observation motivates further investigation of JFET geometry, current spreading, and source-side conduction.

## 8. Potential and Electric-Field Analysis

The internal potential distribution is examined to understand how the applied drain voltage is distributed across the device.

The analysis investigates the voltage drop through the channel, JFET region, drift region, and substrate.

Electric-field distribution is also examined to identify regions of enhanced field concentration, particularly near semiconductor junctions and the gate-oxide interface.

These simulations provide additional insight into the relationship between device geometry, electrostatic behaviour, and off-state voltage support.

## 9. Analytical Validation

Selected TCAD results are compared with analytical semiconductor-device calculations.

The analytical investigations include:

- MOSFET threshold-voltage estimation.
- Subthreshold-swing estimation.
- Drift-region resistance calculation.
- Parallel-plane breakdown-voltage estimation.
- Comparison of analytical and numerically extracted parameters.

The purpose of this comparison is to evaluate the physical consistency of the simulated results and identify differences arising from simplified analytical assumptions and the two-dimensional device model.



## 10. Reproducibility

The simulation can be reproduced using a compatible installation of Silvaco ATLAS.

General workflow:

1. Open the ATLAS simulation deck in DeckBuild.
2. Verify the device geometry, doping profiles, material parameters, and physical models.
3. Execute the simulation deck.
4. Generate the electrical characteristics and save the corresponding log files.
5. Open the generated output files in TonyPlot.
6. Apply the appropriate linear or logarithmic axis representation.
7. Extract the required electrical parameters and compare them with the analytical calculations.

Reproducibility of numerical results depends on the simulator version, physical-model configuration, mesh resolution, and convergence settings.

## 11. Limitations and Scope

This investigation is a numerical TCAD study rather than an experimental device-fabrication project.

The following limitations should be considered:

- The device is represented using a two-dimensional half-cell model.
- The investigation is conducted at 300 K.
- Interface-trap effects are not explicitly calibrated.
- Surface-mobility degradation is not fully modelled.
- The source-contact geometry and mesh resolution introduce modelling limitations.
- High-voltage solver convergence does not independently establish physical avalanche breakdown.
- The extracted electrical parameters are dependent on the selected device geometry and simulation models.

These limitations define the scope of the present investigation and provide directions for subsequent model refinement.

## 12. Future Work

Potential extensions of this investigation include:

- Refinement of the source-contact and JFET-region geometry.
- Mesh-convergence studies near critical junctions.
- Interface-trap and surface-mobility modelling.
- Improved calibration of impact-ionization parameters.
- Temperature-dependent electrical characterization.
- Investigation of alternative JFET widths and doping concentrations.
- Optimization of specific ON-resistance and blocking-voltage trade-offs.
- Comparison with experimentally characterized 4H-SiC power MOSFET structures.

## 13. References

The device structure and simulation methodology should be interpreted alongside the relevant published literature on 4H-SiC power MOSFETs, semiconductor transport models, and TCAD-based device characterization.

Specific literature references and simulator documentation should be added here as they are used in the final study.

---

## Project Status

**Status:** Numerical device modelling and electrical characterization.

**Technology:** 4H-SiC Power Semiconductor Devices.

**Simulation Platform:** Silvaco ATLAS.

**Focus:** Device physics, electrical characterization, resistance decomposition, and numerical analysis.

---

*This repository is intended for academic and research-oriented exploration of wide-bandgap semiconductor power devices. All reported values are simulation-derived unless explicitly stated otherwise.*
