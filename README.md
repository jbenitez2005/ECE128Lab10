Multiplier System – ROM → Register File → Multiplier → RAM
Project Description

This project implements a simple datapath controlled by a finite state machine (FSM). The system reads two 4-bit operands from a ROM, stores them into a small register file, multiplies them using a combinational multiplier, and writes the 8-bit product into RAM.
The top-level module coordinates all components through the control unit.
FPGA Implementation Instructions (Basys3)

Add all Verilog modules to a new Vivado project targeting Basys3 (xc7a35tcpg236-1).

Add the XDC constraints file and ensure the following ports are properly mapped:

Switches 0–5 → addr1 and addr2

Switch 6 → reset

LEDs 0–7 → result (RAM output)

LEDs 8–10 → state output (optional)

Set the top-level module (e.g., top_multiplier_system) as the synthesis top.

Run:

Synthesis

Implementation

Bitstream Generation

Program the Basys3 board.

Operation:

Use SW0–2 to pick ROM address for operand A.

Use SW3–5 to pick ROM address for operand B.

Toggle SW6 to reset.

LEDs 0–7 will display the product from RAM.

LEDs 8–10 show the control unit state.
