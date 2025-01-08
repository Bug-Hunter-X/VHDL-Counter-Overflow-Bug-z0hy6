# VHDL Counter with Overflow Handling

This repository demonstrates a common error in VHDL counters: improper handling of overflow.  The `buggy_counter.vhdl` file contains a counter that doesn't gracefully handle reaching its maximum value, potentially leading to unexpected behavior.

The `fixed_counter.vhdl` file provides a corrected version, showing how to prevent overflow and ensure predictable counter operation.

## Bug Description

The original counter (`buggy_counter.vhdl`) uses an `if` statement to check for the maximum count and reset accordingly.  While functional, this approach is not ideal for larger counters as it is not scalable and can lead to inefficiencies.  Furthermore, it may not be suitable for all applications, such as counters that wrap around instead of resetting.

## Solution

The improved counter (`fixed_counter.vhdl`) uses modulo operation to implement a wrap-around counter. This approach is more scalable, efficient, and avoids the pitfalls of explicit `if` statements for overflow handling.

## Usage

You can simulate both versions of the counter using a VHDL simulator like ModelSim or GHDL to observe the differences in their behavior.  The `fixed_counter.vhdl` demonstrates a more robust method for handling counter overflow.