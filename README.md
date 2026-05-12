# LTspice AI Reference

LTspice documentation for AI assistants and users.

## About LTspice

LTspice is a general-purpose SPICE simulator with built-in schematic capture and waveform viewer, developed by Analog Devices. Freely distributed, it includes a large collection of component models for simulating analog circuits with high confidence.

- Website: http://www.analog.com/ltspice
- Forum: https://ez.analog.com/design-tools-and-calculators/ltspice/

## Setup

From your project directory, run one of the following:

```bat
:: Per-user install
"%LOCALAPPDATA%\Programs\ADI\LTspice\LTspice.exe" -init_ai_ref

:: System-wide install
"C:\Program Files\ADI\LTspice\LTspice.exe" -init_ai_ref
```

This creates hard links in the current directory pointing to the reference files in `%LOCALAPPDATA%\LTspice\reference`. AI assistants will automatically use these files for LTspice guidance.

The links always point to the latest version and are updated automatically with LTspice. Do not edit the referenced files directly.

---

## Critical Conventions

### Engineering Multipliers

| Suffix | Value | Suffix | Value |
|--------|-------|--------|-------|
| T | 1e12 | m | 1e-3 |
| G | 1e9 | u | 1e-6 |
| Meg | 1e6 | n | 1e-9 |
| K | 1e3 | p | 1e-12 |
| mil | 25.4e-6 | f | 1e-15 |

**Pitfall**: `1M` = 1 milli (1e-3), NOT 1 mega. Use `1Meg` for megaohms.

**ALWAYS use `u` for micro (1e-6). NEVER use the μ symbol in netlists or code.**

```spice
C1 out 0 1u        ; 1 microfarad
R1 in out 2.2K     ; 2.2 kilohms
.tran 100u          ; 100 microseconds
```

### Node Naming

- Node `0` is always ground (global circuit common)
- `GND` is a synonym for `0`
- Names are case-insensitive
- Avoid spaces in node names

### File Paths

Always use complete absolute paths from command line:
```
LTspice.exe "C:\Projects\MyCircuit\filter.asc"
```

---

## Reference Files

| File | Use When... |
|------|-------------|
| [LTSPICE-QUICKSTART.md](LTSPICE-QUICKSTART.md) | Getting started, installation, interface modes, CLI |
| [SPICE-SYNTAX-REFERENCE.md](SPICE-SYNTAX-REFERENCE.md) | Netlist structure, encoding, multipliers, conventions |
| [CIRCUIT-ELEMENTS-REFERENCE.md](CIRCUIT-ELEMENTS-REFERENCE.md) | Component syntax (R, L, C, V, I, D, Q, M, sources, switches) |
| [SIMULATION-COMMANDS-REFERENCE.md](SIMULATION-COMMANDS-REFERENCE.md) | Dot commands (.tran, .ac, .dc, .meas, .step, .options, etc.) |
| [TROUBLESHOOTING-GUIDE.md](TROUBLESHOOTING-GUIDE.md) | Convergence failures, debugging, simulator options |
| [SCHEMATIC-REFERENCE.md](SCHEMATIC-REFERENCE.md) | .asc file format, schematic editing, symbols, hierarchy |
| [WAVEFORM-VIEWER-GUIDE.md](WAVEFORM-VIEWER-GUIDE.md) | Viewing results, probing, arithmetic, FFT, export |
| [DEVICE-MODELS-GUIDE.md](DEVICE-MODELS-GUIDE.md) | MOSFET/inductor/opamp models, third-party integration |
| [MEASURE-DATABASE-REFERENCE.md](MEASURE-DATABASE-REFERENCE.md) | .MEAS SQLite database schema, querying results |
| [FAQ-AND-TIPS.md](FAQ-AND-TIPS.md) | Updates, license, Linux, efficiency, SMPS Bode plots |

---

## Quick Examples

### Basic Transient Simulation

```spice
* RC Low-Pass Filter
V1 in 0 PULSE(0 5 0 1n 1n 0.5u 1u)
R1 in out 1K
C1 out 0 100n
.tran 5u
.end
```

### Parameter Sweep

```spice
.param Rval=1K
R1 in out {Rval}
.step param Rval 1K 10K 1K
.tran 10u
```

### AC Analysis

```spice
V1 in 0 AC 1
R1 in out 1K
C1 out 0 100n
.ac dec 100 1 10Meg
```

### Measurement

```spice
.meas TRAN Vmax MAX V(out)
.meas TRAN Trise TRIG V(out)=0.5 RISE=1 TARG V(out)=4.5 RISE=1
.meas AC fc WHEN mag(V(out))=mag(V(out))/sqrt(2) FALL=1
```

---

## Common Tasks

### Improving Convergence

See [TROUBLESHOOTING-GUIDE.md](TROUBLESHOOTING-GUIDE.md) — covers debugging convergence failures, circuit fixes, and simulator option adjustments for both DC operating point and transient analysis.

### Add a Third-Party Model

1. Set component Value to match model/subcircuit name
2. For subcircuits: change Prefix to `X` (Ctrl+right-click)
3. Add `.include "path/to/model.lib"` directive
4. See [DEVICE-MODELS-GUIDE.md](DEVICE-MODELS-GUIDE.md)

### Measure -3dB Bandwidth

```spice
.meas AC fc WHEN mag(V(out))=mag(V(out))/sqrt(2) FALL=1
```

### Efficiency Report

```spice
.tran 10m steady
```
Requires exactly one voltage source (input) and either one current source or Rload (output).

---

## File Locations

| Path | Content |
|------|---------|
| `%LOCALAPPDATA%\LTspice\` | Program files, standard libraries (DO NOT EDIT) |
| `%LOCALAPPDATA%\LTspice\examples\` | Example schematics |
| `%LOCALAPPDATA%\LTspice\lib\cmp\` | Standard component libraries |
| `Documents\LTspice\` | User files (custom models, symbols, libraries) |

User library files: `user.dio`, `user.bjt`, `user.mos`, `user.jft`, `user.ind`, `user.res`
