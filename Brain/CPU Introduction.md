# Quick intro

## Registers and Instructions

A CPU is a machine built to execute a program.

The fundamental blocks of a CPU are **registers** and **instructions**.

You can think of registers as **variables**.

CPUs also all have a Program Counter (PC). You can think of this as a **Pointer**. It indicates where a computer is in it's program sequence.

To a CPU a program is a sequence of hex numbers. Each assembly language instruction corresponds to 1-3 bytes in the program. Learning which number corresponds to which instructions is where a processor data book helps.

Instruction names are often mnemonic for what the instruction actually does. The 8080's mnemonic for load is **MOV (move)**, and **ADD** does just what you think it should.

## Timing

Each instruction takes a certain amount of time to execute and is measured in cycles e.g. MOV on 8080 takes 1 cycle.

This is important for emulation as we have to emulate the correct speed for instructions if we want the game to play correctly.
