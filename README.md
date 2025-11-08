# RV901 Board modifications

inputs (bottom of the board):
U608, 605, 601, 604, 600
force to input (A->B; DIR = H)
need to force VCC = 3.3V

outputs (top of the board)
U603, 607, 602, 606
force to output (B->A; DIR = L)



mods:
 - cut VCC for bottom row buffers in two places
 - connect cut VCC trace to NOR FLASH pin 8
 - connect bottom row DIR to VCC using 10k resistor
 - connect bottom row DIR to VCC using 1uF capacitor (delay line)
 - remove U609
 - connect pin 1 of U608 to bottom row DIR
 - cut top row DIR line - it is already connected to GND via R608