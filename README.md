# vga-template
A template for 640x480 VGA graphics on the DE2-115 FPGA board.

The core of this is the vga module. The vga_template module provides an example on how to use the vga module and should compile as is.

The vga module takes in a 50MHz clock signal, clk, and uses this to maintain it's own internal clock at 25MHz.

The vga module outputs an x and y, which signify the x and y position of the pixel about to be drawn. On the next vga clock pulse, the values provided to r, g, and b will be shown at the x y location. Since the vga clock is half the speed of the base clock, you have one clock pulse to set r, g, and b to the desired values.

vga_output_data should be directly sent to the pins defined in the assignments and should not require any modification.