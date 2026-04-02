# PovoTune

**BD5A ECU Reverse-Engineering / Exploration App**

This is a no-warranties, no guarantees, web-based tool for exploring and researching the Subaru BD5A Legacy RS ECU firmware (JECS / Mitsubishi M7700). It runs entirely in the browser with no server or installation required. It should work for other M7700 bin's also, but no promises.

## Live App

**[Launch PovoTune](https://smoodiver.github.io/povotune/)**

## Reference Documentation

**[Reference & User Guide](https://smoodiver.github.io/povotune/reference/)**

Browse the research to date:

- **[Memory Tables](https://smoodiver.github.io/povotune/reference/rom.html)** ROM data tables, calibration maps, axes, constants, and thresholds
- **[Functions](https://smoodiver.github.io/povotune/reference/functions/)** 210 analysed firmware functions with algorithm detail, inputs/outputs, and cross-references

## Features

- **Disassembly viewer** Full M7700 disassembly with syntax highlighting, branch target links, and inline annotations
- **Hex dump viewer** Interactive hex browser with byte-level selection, search, colour-coded object types, and right-click context menus for defining tables and functions
- **Knowledge graph** Force-directed graph visualisation showing function calls, memory access, and data flow relationships
- **Address space map** Minimap showing the full 64 KB address space at a glance
- **In-browser analysis** Load a raw `.bin` firmware dump and run automated recursive descent analysis entirely client-side
- **Project persistence** All annotations, renamed functions, and data definitions auto-save to IndexedDB and can be exported as portable JSON

## Getting Started

1. Open the [live app](https://smoodiver.github.io/povotune/)
2. Click **Factory BD5A ROM** to load the pre-analysed firmware project to get started.
3. Or load your own `.bin` firmware dump or `.json` project file

See the [User Guide](https://smoodiver.github.io/povotune/reference/) for detailed usage instructions covering all views and interactions.

## Technology

Fully static single-page application. All processing happens in your browser. If it's slow, that'll be why.

- React + Vite
- IndexedDB for local persistence
- D3.js for graph visualisation
- M7700 instruction decoder and recursive descent analyser

## License

All rights reserved.
