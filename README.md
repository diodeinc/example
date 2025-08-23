# PCB example board

This repo demonstrates designing PCBs with the Zener language (`.zen`) and the open-source `pcb` compiler. You describe parts and connectivity in `.zen`, compose them into boards, and generate KiCad projects for layout/manufacturing.

## Prerequisites

To recreate this example step by step, visit the [tutorial](https://docs.pcb.new/pages/example)

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
├── modules                 # Reusable modules made manually (.zen)
├── boards                  # Board compositions (.zen)
└── pcb.toml                # Workspace + dependencies
```

## What is a .zen file?

- Component(...): Defines a part by symbol/footprint and pins
- io(...): Declares typed ports/nets (e.g., `Net`, `Ground`)
- Module("path"): Reuses another `.zen` module
- Wiring: Connect modules/components by shared nets
- Layout(...): Hints where to emit previews/outputs

See `modules/Antenna.zen`, `modules/SMAConnector.zen`, and the composed board `boards/EX0001/EX0001.zen` for examples.

## Typical workflow

1. Install the `pcb` compiler and KiCad 9 (see docs link above)
2. Explore modules in `modules/` and the board in `boards/EX0001/EX0001.zen`
3. Run the compiler, targeting the board `.zen`, to generate outputs (KiCad project, previews, docs). Refer to the docs for exact commands on your platform
4. Open the generated KiCad project to place/route

Notes:
- `pcb.toml` declares the workspace and pulls the Zener stdlib
- A spec is included at `boards/EX0001/docs/spec.md`

## Goals of this example

- Model reusable hardware blocks in `.zen`
- Compose modules into a complete board
- Produce KiCad files from a high-level Zener description
