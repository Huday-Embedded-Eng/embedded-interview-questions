# embedded-interview-questions
Interview questions and answers for Embedded Systems, C/C++, ARM

--> 1.Explain about ARM7 Architecture?

A. ARM7 architecture is an older generation 32-bit RISC-based processor architecture.
It follows a Von Neumann architecture, where instructions and data share the same memory and bus.

ARM7 uses a 3-stage pipeline consisting of Fetch, Decode, and Execute, which improves instruction throughput.

It supports two instruction sets:
ARM mode, which uses 32-bit instructions
Thumb mode, which uses 16-bit instructions to improve code density and memory efficiency

ARM7TDMI-S stands for:

T – Thumb instruction support
D – On-chip debug support
M – Fast hardware multiplier
I – EmbeddedICE for debugging
S – Synthesizable core

Due to its low power consumption and simplicity, ARM7 is widely used in embedded systems such as microcontrollers.

--> 2.Difference between ARM7 and ARM Cortex M0+ Architecture ?

A. ARM7 is an older generation 32-bit RISC-based processor mainly designed for embedded control applications.
It follows a Von Neumann architecture, where instructions and data share the same memory and bus, which can lead to bus contention.
ARM7 does not include advanced features like NVIC, low-latency interrupts, or modern power-saving mechanisms.

ARM Cortex-M0 is a newer, low-power 32-bit RISC-based microcontroller core designed for real-time and IoT applications.
It follows a modified Harvard architecture, with separate instruction and data buses, allowing faster execution.
Cortex-M0 includes features like NVIC (Nested Vectored Interrupt Controller), better interrupt latency, and lower power consumption.

Due to these improvements, Cortex-M0 is preferred over ARM7 in modern embedded and IoT systems, though Wi-Fi is provided through external modules, not the core itself.
