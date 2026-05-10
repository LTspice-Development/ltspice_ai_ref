# LTspice AI Reference

Official LTspice documentation optimized for AI assistants (Claude Code, GitHub Copilot, etc.).

## Overview

This reference collection provides comprehensive LTspice documentation in a format that AI coding assistants can efficiently parse and use to help you design and simulate circuits. The files are installed with LTspice and automatically updated with new releases.

## Setup

Initialize AI reference files in your project directory:

```bash
cd <your_project_directory>
"C:\Program Files\ADI\LTspice\LTspice.exe" -init_ai_ref
```

This creates symlinks from your project to the reference files located in `%LOCALAPPDATA%\LTspice\`, making them available to AI assistants while keeping them centrally updated.

**Important**: Run this command from within your LTspice project directory where you want AI assistance.

## Reference Files

| File | Content |
|------|---------|
| [CLAUDE.md](CLAUDE.md) | Central index and critical conventions |
| [LTSPICE-QUICKSTART.md](LTSPICE-QUICKSTART.md) | Installation, interface, CLI usage |
| [SPICE-SYNTAX-REFERENCE.md](SPICE-SYNTAX-REFERENCE.md) | Netlist structure, encoding, multipliers |
| [CIRCUIT-ELEMENTS-REFERENCE.md](CIRCUIT-ELEMENTS-REFERENCE.md) | Component syntax (R, L, C, V, I, D, Q, M, etc.) |
| [SIMULATION-COMMANDS-REFERENCE.md](SIMULATION-COMMANDS-REFERENCE.md) | Dot commands (.tran, .ac, .dc, .meas, .step, .options) |
| [TROUBLESHOOTING-GUIDE.md](TROUBLESHOOTING-GUIDE.md) | Convergence failures, debugging, simulator options |
| [SCHEMATIC-REFERENCE.md](SCHEMATIC-REFERENCE.md) | .asc file format, schematic editing |
| [WAVEFORM-VIEWER-GUIDE.md](WAVEFORM-VIEWER-GUIDE.md) | Viewing results, probing, analysis |
| [DEVICE-MODELS-GUIDE.md](DEVICE-MODELS-GUIDE.md) | MOSFET/inductor/opamp models, integration |
| [MEASURE-DATABASE-REFERENCE.md](MEASURE-DATABASE-REFERENCE.md) | .MEAS SQLite database schema |
| [FAQ-AND-TIPS.md](FAQ-AND-TIPS.md) | Tips, efficiency, advanced techniques |

## Critical Conventions for AI Assistants

### Unit Notation

**ALWAYS use `u` for micro (1e-6). NEVER use μ in netlists or code.**

```spice
C1 out 0 1u        ; 1 microfarad (CORRECT)
C1 out 0 1μF       ; WRONG - will cause errors
.tran 100u         ; 100 microseconds
```

### Engineering Multipliers

- `K` = 1e3 (kilo)
- `Meg` = 1e6 (mega) — **NOT `M`**
- `m` = 1e-3 (milli)
- `u` = 1e-6 (micro)
- `n` = 1e-9 (nano)
- `p` = 1e-12 (pico)

**Pitfall**: `1M` = 1 milli (1e-3). Use `1Meg` for megaohms.

### File Paths

Always use complete absolute paths in command line:
```bash
ltspice.exe "C:\Projects\MyCircuit\filter.asc"
```

## Quick Examples

### RC Low-Pass Filter

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

### AC Analysis with Measurement

```spice
V1 in 0 AC 1
R1 in out 1K
C1 out 0 100n
.ac dec 100 1 10Meg
.meas AC fc WHEN mag(V(out))=mag(V(out))/sqrt(2) FALL=1
```

## Updates

Reference files are automatically updated when you update LTspice. Symlinks in your project directories will point to the latest version.

## For AI Assistant Developers

These markdown files use structured formatting optimized for:
- Quick lookup of syntax rules
- Component and command reference tables
- Common troubleshooting patterns
- Example code snippets

AI assistants should:
1. Read [CLAUDE.md](CLAUDE.md) first for routing to specific references
2. Enforce the `u` (not μ) convention strictly
3. Use absolute paths for file references
4. Default to provided examples and patterns

## Resources

- LTspice Website: http://www.analog.com/ltspice
- Forum: https://ez.analog.com/design-tools-and-calculators/ltspice/

---

**Note**: These files are symlinked from your LTspice installation. Do not edit them directly; they will be overwritten by updates. For feedback, visit the LTspice forum.
