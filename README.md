9# embedded-interview-questions
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
I – EmbeddedICE integrated circuit emulator 
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

3.Difference between von-neumann and Hardvard architecture ?

A.Von Neumann → Single memory, single bus, one operation at a time

Harvard → Separate memory, separate buses, parallel operations

4. Explain about LPC2148 mcu?

A. LPC2148 is an ARM7-based 32-bit RISC microcontroller with a maximum clock speed of 60 MHz. It includes on-chip Flashmemory 512kb, SRAM 32kb, 10-bit ADC, DAC, UART, I2C, SPI, PWM, RTC, and supports EmbeddedICE for debugging. It is widely used in low-power embedded applications.

5.Explain about Raspberry pi pico W ?

A.RP2040 is a dual-core 32-bit RISC microcontroller based on ARM Cortex-M0+, used in Raspberry Pi Pico W. It uses a modified Harvard architecture and runs at up to 133 MHz. It has 264 KB on-chip SRAM and uses external QSPI Flash (typically 2 MB). It supports a 12-bit ADC, GPIO, UART, SPI, I2C, PWM, timers, RTC, and Pico W adds Wi-Fi, making it suitable for IoT applications.

