# PCB example board

This repository contains schematics and boards built using the `pcb` command line utility by Diode, using the Zener language and open source compiler

## Prerequisites

For the most up to date information, visit our documentation at [`docs.pcb.new`](https://docs.pcb.new)

The open source PCB compiler is available at [`github.com/diodeinc/pcb`](https://github.com/diodeinc/pcb)

1. **KiCad 9.0**
   - Required for PCB layout
   - Download from [KiCad website](https://kicad.org/download)

## Project Structure

```
.
├── README.md
├── components              # Auto-generated component definitions (do not edit)
├── modules                 # User-authored reusable modules (.zen files)
├── boards                  # Board designs that use modules (.zen files)
└── pcb.toml               # Project configuration
```

