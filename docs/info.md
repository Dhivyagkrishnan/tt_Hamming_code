<!---

This file is used to generate your project datasheet. Please fill in the information below and delete any unused
sections.

You can also include images in this folder and reference them in the markdown. Each image must be less than
512 kb in size, and the combined size of all images must be less than 1 MB.
-->

## How it works

Hamming (7,4) code takes 4 data bits and adds 3 parity bits to form a 7-bit code that can detect and correct single-bit errors. Parity bits are placed at positions 1, 2, and 4, calculated using XOR of specific data bits. At the receiver, the syndrome is computed to locate the error bit, which is then flipped to recover the original data. This makes it a simple and effective single-error correction scheme in digital systems.

## How to test
We can test by encoding a 4-bit data, then intentionally flipping one bit in the 7-bit codeword to simulate an error. Pass this through the decoder — the syndrome should point to the flipped bit, and the corrected output must match the original data.

## External hardware

 FPGA / CPLD board (to synthesize and test the design in hardware).

Input switches (to provide 4-bit data and to inject errors).

LEDs/7-segment display (to observe encoded, received, and corrected outputs).

PC with FPGA toolchain (Vivado/Quartus) for programming and simulation.
