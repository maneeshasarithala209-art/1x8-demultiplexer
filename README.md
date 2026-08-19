# 1×8 Demultiplexer in Verilog

A simple implementation of a **1×8 Demultiplexer** using Verilog HDL.

## Overview

A demultiplexer routes one input to one of eight outputs depending on the select lines.

### Inputs

- din
- sel[2:0]

### Outputs

- dout[7:0]

## Truth Table

| SEL | Active Output |
|------|---------------|
|000|dout[0]|
|001|dout[1]|
|010|dout[2]|
|011|dout[3]|
|100|dout[4]|
|101|dout[5]|
|110|dout[6]|
|111|dout[7]|

## Project Structure

```
src/
tb/
sim/
images/
README.md
```

## Simulation

Compile:

```bash
iverilog -o demux src/demux1x8.v tb/demux1x8_tb.v
```

Run:

```bash
vvp demux
```

Open waveform:

```bash
gtkwave demux1x8.vcd
```

## Example Output

```
SEL=000 -> 00000001
SEL=001 -> 00000010
SEL=010 -> 00000100
...
```

## Author

Your Name

## License

MIT