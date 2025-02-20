# Uncommon VHDL Counter Bug

This repository demonstrates a subtle bug in a VHDL counter implementation. The bug is related to a missing `else` branch in a conditional signal assignment within a clocked process. This can lead to unexpected behavior under certain conditions. 

## Bug Description

The `bug.vhdl` file contains a counter that is supposed to increment from 0 to 15 and then wrap around to 0. However, there's a missing `else` case when the counter reaches its maximum value. This means if it is not 15, then the value isn't updated. 

## Bug Solution

The `bugSolution.vhdl` file provides a corrected version of the counter. It includes an explicit `else` branch to handle cases where the counter is not equal to 15 and fix the counter logic. 

## How to Reproduce

1.  Synthesize or simulate `bug.vhdl`. Observe the counter's behavior.
2.  Synthesize or simulate `bugSolution.vhdl`. Compare its behavior with the buggy version. 

This example highlights the importance of carefully considering all possible cases in conditional logic, especially within concurrent processes in hardware description languages.