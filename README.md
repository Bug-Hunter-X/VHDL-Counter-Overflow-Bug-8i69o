# VHDL Counter Overflow Bug
This repository demonstrates a common bug in VHDL code: an integer counter that may exhibit unexpected behavior due to potential overflow issues. The `buggy_counter.vhdl` file contains the buggy code, while `fixed_counter.vhdl` provides a corrected version.

## Bug Description
The original VHDL code implements a simple counter. However, there's a subtle issue: the integer type has a limited range (0 to 15). When the counter reaches 15, it wraps around to 0. This wrapping behavior might be unintentional in some applications.

## Solution
The `fixed_counter.vhdl` file addresses this issue by providing error handling for the situation when the counter reaches the upper bound of its range. This ensures that the counter behaves as intended under various conditions.

## How to Run
1. Use a VHDL simulator (e.g., ModelSim, GHDL, VUnit) to simulate both versions.
2. Observe the output of each version and compare the results.
3. This highlights the potential problems caused by the integer overflow and how they are resolved. 

## Note
This example showcases a common coding error and how to mitigate it.  Always carefully consider the ranges of your integer variables in VHDL to avoid unexpected overflow or underflow behaviors.