# Multiplier System – ROM → Register File → Multiplier → RAM

## Project Description
This project implements a simple datapath controlled by a finite state machine (FSM). The system reads two 4-bit operands from a ROM, stores them into a small register file, multiplies them using a combinational multiplier, and writes the 8-bit product into RAM.  
The top-level module coordinates all components through the control unit.

---

## FPGA Implementation Instructions (Basys3)

1. Create a new Vivado project targeting **Basys3 (xc7a35tcpg236-1)**.
2. Add all Verilog source files to the project.
3. Add the XDC constraints file and verify the following mappings:
   - **SW0–SW2** → `addr1`  
   - **SW3–SW5** → `addr2`  
   - **SW6** → `reset`  
   - **LED0–LED7** → product output (`result` from RAM)  
   - **LED8–LED10** → control unit state (optional)
4. Set your top-level module (e.g., `top_multiplier_system`) as the synthesis top.
5. Run:
   - Synthesis  
   - Implementation  
   - Bitstream Generation
6. Program the Basys3 board.

---

## Operation
- **SW0–2** select the ROM address for operand **A**.  
- **SW3–5** select the ROM address for operand **B**.  
- **SW6** resets the system.  
- **LEDs 0–7** display the 8-bit RAM output (the product).  
- **LEDs 8–10** display the current FSM state.

