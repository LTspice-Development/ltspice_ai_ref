# LTspice Menu Reference

*Last updated: 2026-05-14*  
*LTspice version: 24+*

Complete hierarchical listing of all menu options and keyboard shortcuts.


## Menu Access Keys

All menus can be accessed via Alt+[letter]:
- **Alt+F** = File
- **Alt+E** = Edit  
- **Alt-I** = Hierarchy
- [] = View
- [] = Simulate
- **Alt+T** = Tools
- **Alt+P** = Plot Settings (Waveform Viewer)
- **Alt+W** = Window
- **Alt+H** = Help

Within each menu, underlined letters (mnemonics) can be pressed directly without Alt.

**Example**: To access File > New Schematic:
- Press Alt+F (opens File menu), then press N
- Or use the direct shortcut: Ctrl+N


## File Menu (Alt+F)

- **New Schematic** (N, Ctrl+N) — Create new blank schematic
- **New Symbol** — Create new component symbol
- **Open** (O, Ctrl+O) — Open schematic, netlist, or waveform file
- **Open Examples...** — Browse built-in example circuits
  - Educational/ — Analysis examples
  - Applications/ — ADI product circuits
- **New Library**
  - Capacitor
  - Inductor
  - Resistor
- **Save** (S, Ctrl+S) — Save current file
- **Save As...** (A, Ctrl+Shift+S) — Save with new filename
- **Close** (C, Ctrl+W) — Close current file
- **Print** (P, Ctrl+P)
- **Print Preview** (V)
- **Print Monochrome** (M) — Toggle: Print schematics in black and white
- **Recent Files** (submenu)
- **Exit** (X) — Close LTspice


## Edit Menu - Available when .ASC file is active

- **Undo** (O, Ctrl+Z) — Reverse last action
- **Redo** (Ctrl+Shift+Z) — Reapply last undone action
- **Text** (T, T) - Add text comment to schematic
- **SPICE Directive** (S, .) - Add SPICE directive to schematic
- **Configure SPICE Analysis** (A) - Opens Configure Analysis Dialog
- **Resistor** (R) - Add resistor to schematic
- **Capacitor** (C) - Add capacitor to schematic
- **Inductor** (L) - Add inductor to schematic
- **Diode** (D) - Add diode to schematic
- **Component** (P) - open component dialog
- **Rotate** (Ctrl+R) - Rotate selected
- **Mirror** (Ctrl+E) - Mirror selected
- **Draw Wire** (W) - Draw wire segment
- **Label Net** (N) - Add Label to a Net
- **Place GND** (G) - Place Ground Component
- **Place Bus Tap** (B) - Place bus tap
- **Delete** (Backspace or Delete)
- **Duplicate** (Ctrl+C) — Clone selected component
- **Move** (M) — Enter move mode
- **Stretch** (S) — Move with connected wires
- **Paste** (Ctrl+V) - Paste copied elements
- **Draw → ...**
  - **Line**
  - **Rectangle**
  - **Ellipse**
  - **Arc**
  - **Line Style** - open line style dialog


## View Menu - When Schematic Window is active

- **Zoom Area** (Z) — Drag to define zoom region
- **Zoom Back** (Shift+Z) — Return to previous zoom level
- **Zoom to Fit** (Space) — Fit entire schematic in window
- **Recenter** — Center view on schematic origin
- **Show Grid** (Ctrl+G) — Toggle grid visibility
- **Mark Unconn. Pins** (Ctrl+U) — Highlight unconnected component pins
- **Mark Anchors** (Ctrl+A) — Show anchor points for text/components
- **Bill of Materials** (submenu) — Generate component list
- **Efficiency Report** (submenu) — Power conversion efficiency analysis
- **Update and View SPICE Netlist** — Regenerate and display netlist
- **SPICE Output Log** (Ctrl+L) — Show simulation messages and errors
- **Visible Traces** — Select which waveforms to display
- **Autorange Y-axis** — Auto-scale vertical axis
- **Marching Waves** (submenu) — Animated waveform display options
- **Set Probe Reference** — Define voltage measurement reference node
- **Toolbar** (checkmark) — Toggle toolbar visibility
- **Status Bar** (checkmark) — Toggle status bar visibility
- **Window Tabs** (checkmark) — Toggle window tab display


## View Menu - When Waveform Viewer Window is active

- **Zoom Area** (Z) — Drag to define zoom region
- **Zoom Back** (Shift+Z) — Return to previous zoom level
- **Zoom to Fit** (Space) — Fit entire waveform in window
- **Recenter** — Center view on waveform
- **SPICE Output Log** (Ctrl+L) — Show simulation messages and errors
- **FFT** — Plot FFT
- **Toolbar** — Toggle toolbar visibility
- **Status Bar**  — Toggle status bar visibility
- **Window Tabs**  — Toggle window tab display



## Simulate Menu - Available when .ASC file is active

- **Run/Pause** (Alt+R) — Execute simulation
- **Stop** (Alt+S) — Halt running simulation
- **Efficiency Calculation** (submenu)
  - **Mark Start** — Begin efficiency calculation region
  - **Mark End** — End efficiency calculation region
- **Settings**
- **Configure Analysis** (C, A) - Opens Configure Analysis Dialog


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


## Plot Settings Menu (Waveform Viewer)

- **Visible Traces** — Select which waveforms to display
- **Edit Plot Defs File** — Modify plot definitions
- **Save Plot Settings** — Store current plot configuration
- **Open Plot Settings** — Load saved plot configuration
- **[ ] Add Plot Pane**
- **[ ] Tile Horizontal**
- **[ ] Tile Vertical**
- **[ ] Other options...**


## Window Menu - Available when any window is open

- **[ ] Cascade** — Arrange windows in cascade
- **[ ] Tile** — Arrange windows in grid
- **[ ] Close All**
- **[ ] List of open windows...**


## Help Menu

- **Help Topics** (F1) — Open help documentation
- **Keyboard Shortcut Cheat Sheet** — Always-on-top shortcut reference
  - **Edit Keyboard Shortcuts** button — Customize shortcuts
- **Open Examples...** — Browse example circuits
- **Check for LTspice updates** — Download latest program version
- **Show LTspice Change Log** — Program version history
- **Show Model Change Log** — Component/model update history
- **[ ] About LTspice** — Version and license information


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


## Symbol Editor Menu (When .asy file is open)

- **[ ] File → ...**
- **Edit** (submenu)
  - **Add Pin/Port** — Create symbol pin
  - **Attributes → Edit Attributes** — Set symbol properties
  - **Attributes → Attribute Window** — Visibility settings
- **[ ] Draw → ...**
- **[ ] Other menus...**


## Notes

- **Customization**: Keyboard shortcuts can be customized via Help > Keyboard Shortcut Cheat Sheet > Edit Keyboard Shortcuts
- **Context-sensitive**: Some menu items only appear in specific contexts (schematic vs. waveform viewer vs. symbol editor)
- **Platform**: This reference is for Windows version
- **Version-specific**: Menu options may vary between LTspice versions
