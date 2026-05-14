# LTspice Menu Reference

*Last updated: 2026-05-14*  
*LTspice version: 24+*

Complete hierarchical listing of all menu options and keyboard shortcuts.

---

## How to Complete This Document

1. Open LTspice
2. Go through each menu systematically
3. Fill in missing items marked with `[ ]`
4. Add keyboard shortcuts shown in the menus (e.g., Ctrl+N, F2)

---

## File Menu

- **New Schematic** (Ctrl+N) — Create new blank schematic
- **New Symbol** — Create new component symbol
- **Open** (Ctrl+O) — Open schematic, netlist, or waveform file
- **Open Examples...** — Browse built-in example circuits
  - Educational/ — Analysis examples
  - Applications/ — ADI product circuits
- **New Library**
  - Capacitor
  - Inductor
  - Resistor
- **Close** — Close current file
- **Save** (Ctrl+S) — Save current file
- **Save As...** — Save with new filename
- **[ ] Export**
  - **Export Netlist** — Generate PCB netlist
  - **[ ] Other export options...**
- **[ ] Print** (Ctrl+P)
- **[ ] Print Preview**
- **[ ] Recent Files** (submenu)
- **Exit** (Alt+F4) — Close LTspice

---

## Edit Menu - Available when .ASC file is active

- **Undo** (Ctrl+Z) — Reverse last action
- **Redo** (Ctrl+Y) — Reapply last undone action
- **Cut** (Ctrl+X) — Cut selected objects
- **Copy** (Ctrl+C) — Copy selected objects
- **Paste** (Ctrl+V) — Paste from clipboard
- **[ ] Delete** (Delete/F5)
- **[ ] Select All**
- **Component** (F2) — Place component from library
- **[ ] Wire** (F3)
- **[ ] Label** (F4)
- **Delete** (F5) — Enter delete mode
- **Duplicate** (F6) — Clone selected component
- **Move** (F7) — Enter move mode
- **Drag** (F8) — Move with connected wires
- **[ ] Draw → ...**
  - **[ ] Rectangle**
  - **[ ] Circle**
  - **[ ] Arc**
  - **[ ] Text** (T)
  - **[ ] SPICE Directive** (S)
  - **[ ] SPICE Comment**
- **[ ] Rotate** (Ctrl+R)
- **[ ] Mirror** (Ctrl+E)
- **Attributes** (submenu)
  - **Edit Attributes** — Modify visible attributes
  - **Attribute Window** — Show/hide all attributes (Ctrl+right-click)
- **[ ] Other options...**

---

## View Menu

### Schematic Window
- **[ ] Zoom In** (Ctrl++)
- **[ ] Zoom Out** (Ctrl+-)
- **[ ] Zoom to Fit**
- **SPICE Netlist** — Display generated netlist for current schematic
- **SPICE Error Log** — Show simulation messages and errors
- **[ ] Mark** — Highlight net
- **[ ] Other options...**

### Waveform Viewer Window
- **Add Trace** — Add waveform expression
- **FFT** — Compute frequency spectrum of selected waveform
- **Efficiency Report** — Show power conversion efficiency
- **[ ] Zoom In**
- **[ ] Zoom Out**
- **[ ] Auto-range**
- **[ ] Other options...**

---

## Simulate Menu - Available when .ASC file is active

- **Run** (Alt+R) — Execute simulation
- **[ ] Stop** — Halt running simulation
- **[ ] Halt**
- **Edit Simulation Cmd** — Modify simulation parameters
- **Efficiency Calculation** (submenu)
  - **Mark Start** — Begin efficiency calculation region
  - **Mark End** — End efficiency calculation region
- **[ ] Other options...**

---

## Tools Menu

- **Settings** — Open comprehensive settings dialog
  - **General** tab
  - **Schematic** tab
  - **Waveform** tab
  - **Search Paths** tab
  - **Hacks!** tab
  - **Save Defaults** tab
- **Update Components** — Download latest component libraries
- **[ ] Sync Release**
- **Color Preferences** — Customize UI colors
  - Schematic colors
  - Waveform colors
  - Netlist editor colors
- **Export Netlist** — Generate netlist for PCB layout
- **Write to .wmf file** — Export waveform as metafile (waveform viewer)
- **[ ] Control Panel**
- **[ ] Other options...**

---

## Plot Settings Menu (Waveform Viewer)

- **Visible Traces** — Select which waveforms to display
- **Edit Plot Defs File** — Modify plot definitions
- **Save Plot Settings** — Store current plot configuration
- **Open Plot Settings** — Load saved plot configuration
- **[ ] Add Plot Pane**
- **[ ] Tile Horizontal**
- **[ ] Tile Vertical**
- **[ ] Other options...**

---

## Window Menu - Available when any window is open

- **[ ] Cascade** — Arrange windows in cascade
- **[ ] Tile** — Arrange windows in grid
- **[ ] Close All**
- **[ ] List of open windows...**

---

## Help Menu

- **Help Topics** (F1) — Open help documentation
- **Keyboard Shortcut Cheat Sheet** — Always-on-top shortcut reference
  - **Edit Keyboard Shortcuts** button — Customize shortcuts
- **Open Examples...** — Browse example circuits
- **Check for LTspice updates** — Download latest program version
- **Show LTspice Change Log** — Program version history
- **Show Model Change Log** — Component/model update history
- **[ ] About LTspice** — Version and license information

---

## Context Menu Actions (Right-Click)

### On Schematic Component Body
- **Assisted Mode**: Component-specific editor dialog
- **Expert Mode**: Direct attribute editing (click on visible text)
- **Super Expert Mode** (Ctrl+right-click): Full attribute editor with visibility

### On Schematic Wire/Node
- **[ ] Add net label**
- **[ ] Highlight net**
- **[ ] Other options...**

### On Waveform Trace Label
- **Edit expression** — Modify waveform arithmetic
- **Delete trace**
- **[ ] Other options...**

### On Waveform Plot Area
- **Add pane above**
- **Add pane below**
- **Move pane**
- **[ ] Other options...**

---

## Common Keyboard Shortcuts

### Schematic Editing
| Shortcut | Action |
|----------|--------|
| F2 | Place component |
| F3 | Draw wire |
| F4 | Net label |
| F5 | Delete mode |
| F6 | Duplicate |
| F7 | Move |
| F8 | Drag |
| T | Text comment |
| S | SPICE directive |
| G | Ground symbol |
| R | Resistor (quick component) |
| C | Capacitor (quick component) |
| L | Inductor (quick component) |
| D | Diode (quick component) |
| Ctrl+R | Rotate |
| Ctrl+E | Mirror |
| Esc | Cancel current operation |

### Simulation
| Shortcut | Action |
|----------|--------|
| Alt+R | Run simulation |

### Waveform Viewer
| Shortcut | Action |
|----------|--------|
| Alt+Click component | Plot power dissipation |
| Alt+Click wire | Plot wire current |
| Ctrl+Click trace label | Compute average/RMS |
| Ctrl+Mouse wheel | Preview zoom |
| Ctrl+release (drag) | Copy trace to another pane |

### General
| Shortcut | Action |
|----------|--------|
| Ctrl+N | New schematic |
| Ctrl+O | Open file |
| Ctrl+S | Save |
| Ctrl+Z | Undo |
| Ctrl+Y | Redo |
| Ctrl+C | Copy |
| Ctrl+V | Paste |
| F1 | Help |

---

## Symbol Editor Menu (When .asy file is open)

- **[ ] File → ...**
- **Edit** (submenu)
  - **Add Pin/Port** — Create symbol pin
  - **Attributes → Edit Attributes** — Set symbol properties
  - **Attributes → Attribute Window** — Visibility settings
- **[ ] Draw → ...**
- **[ ] Other menus...**

---

## Notes

- **Customization**: Keyboard shortcuts can be customized via Help > Keyboard Shortcut Cheat Sheet > Edit Keyboard Shortcuts
- **Context-sensitive**: Some menu items only appear in specific contexts (schematic vs. waveform viewer vs. symbol editor)
- **Platform**: This reference is for Windows version
- **Version-specific**: Menu options may vary between LTspice versions

---

## How to Extract Complete List

1. **Manual Method**: 
   - Open LTspice
   - Click through each menu
   - Note items and shortcuts
   - Fill in `[ ]` placeholders above

2. **Using Cheat Sheet**:
   - Help > Keyboard Shortcut Cheat Sheet
   - Click "Edit Keyboard Shortcuts"
   - Export/copy the keyboard mapping file

3. **Screenshots**: 
   - Take screenshots of each menu
   - Reference while filling in this document