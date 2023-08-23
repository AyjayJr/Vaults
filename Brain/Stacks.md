Most assembly languages will have subroutines (i.e. functions)

Thus, most CPUs have a Stack to account for this.

There is a stack pointer that can be moved around to keep track of which instruction is to be executed next and where to go back to when execution is finished. 

The stack pointer may be a normal register or a special register with special features depending on the processor.

The 8080 stack pointer has special push and pop instructions.