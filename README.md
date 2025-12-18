9# embedded-interview-questions
Interview questions and answers for these
Technical Skills:-
Embedded C, C/C++
ARM7TDMI-S (LPC21xx Series)
ARM Cortex-M0+ (Raspberry Pi Pico – RP2040)
Bare-Metal Programming
Interrupt Handling (External, Timer, Peripheral Interrupts)
RTOS Basics
GPIO, ADC, UART, SPI, I2C
Keil, Arduino IDE
Git & GitHub
Proteus Simulation & Debugging

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

--> 3. Difference between von-neumann and Hardvard architecture ?

A.Von Neumann → Single memory, single bus, one operation at a time

Harvard → Separate memory, separate buses, parallel operations

--> 4. Explain about LPC2148 mcu?

A. LPC2148 is an ARM7-based 32-bit RISC microcontroller with a maximum clock speed of 60 MHz. It includes on-chip Flashmemory 512kb, SRAM 32kb, 10-bit ADC, DAC, UART, I2C, SPI, PWM, RTC, and supports EmbeddedICE for debugging. It is widely used in low-power embedded applications.

--> 5. Explain about Raspberry pi pico W ?

A.RP2040 is a dual-core 32-bit RISC microcontroller based on ARM Cortex-M0+, used in Raspberry Pi Pico W. It uses a modified Harvard architecture and runs at up to 133 MHz. It has 264 KB on-chip SRAM and uses external QSPI Flash (typically 2 MB). It supports a 12-bit ADC, GPIO, UART, SPI, I2C, PWM, timers, RTC, and Pico W adds Wi-Fi, making it suitable for IoT applications.


--> 6. What is a Core?

A: A core is the main part of a processor that executes instructions. It contains the ALU, registers, and control unit.

--> 7. What is the difference between Core and Processor?

Answer:
A core executes instructions, while a processor may contain one or more cores.

--> 8. What is bare-metal programming?

Answer:
Bare-metal programming is writing code that runs directly on hardware without an OS.

--> 9. Interrupt vs polling?

Answer:
Polling continuously checks a condition, while an interrupt notifies the CPU only when an event occurs.

--> 10. What is volatile keyword?

Answer:
volatile tells the compiler that a variable can change unexpectedly, so it should not optimize it.

--> 11. Difference between C and Embedded C?

Answer:
Embedded C is an extension of c used to write programs for hardware control with direct register access.
where as C is a general-purpose programming language used to develop software applications, supporting both low-level and high-level programming concepts.

--> 12. What is static keyword?

Answer:
static preserves variable value between function calls and limits scope.

--> 13. Macro vs function?

Answer:
Macros are preprocessor directives with no type checking, while functions are compiled and safer.

--> 14. What is bit masking?

Answer:
Bit masking is used to set, clear, or toggle specific bits in a register.

-->15. What is memory-mapped I/O?

Answer:
Peripheral registers are accessed like memory locations using pointers.

-->16.What is pipeline?

Answer:
Pipeline divides instruction execution into stages to increase speed.

-->17. What is NVIC?

Answer:
NVIC handles interrupt prioritization and control in Cortex-M processors.

-->18. What is vector table?

Answer:
A vector table stores addresses of interrupt service routines.

-->19. What precautions in ISR?

Answer:
ISR should be short, avoid delays, and not use blocking functions.

--> 20. What is interrupt latency?

Answer:
Time taken from interrupt occurrence to ISR execution.

--> 21. What is hex file?

Answer:
Hex file contains machine code to be flashed into MCU.

--> 22. What is const?

Answer:
const prevents modification of a variable after initialization.

--> 23.What causes stack overflow?

Answer:
Deep recursion, large local variables, or infinite function calls.

--> 24. What is typedef?

Answer:
typedef creates an alias name for a data type.

--> 26. What is a timer?

Answer:
A hardware counter used for delays, event timing, and interrupts.

-->  27. Why C is used in embedded systems?

Answer:
Efficient, fast, hardware-level control.

--> 28. Why volatile is used with bitwise register access?

Answer:
To prevent compiler optimization of hardware registers.

--> 29. How do you set a bit?

num = num | (1 << pos);

--> 29. How do you clear a bit?

num = num & ~(1 << pos);

--> 30. How do you toggle a bit?

num = num ^ (1 << pos);

--> 31. How do you check if a bit is set?

if(num & (1 << pos))
    printf("Bit is set");

--> 32. What is a Peripheral Interrupt? 

Answer:
A peripheral interrupt is an interrupt generated by an on-chip peripheral (like Timer, UART, ADC, SPI, I2C) to notify the CPU that a specific event has occurred and requires immediate attention.
    
--> 33. What is an External Interrupt? 

Answer:
An external interrupt is an interrupt generated by an external signal applied to a microcontroller pin to immediately notify the CPU when an external event occurs.

--> 34. what are the 7 Modes of ARM ?

Answer:
ARM7 supports seven modes: User, FIQ, IRQ, Supervisor, Abort, Undefined, and System modes, each designed for efficient exception and interrupt handling.

🔹 List of 7 ARM Modes

1️⃣ User Mode (USR)
Normal program execution mode
No access to privileged resources

2️⃣ FIQ Mode (FIQ)
Fast Interrupt Request mode
Used for high-priority interrupts

3️⃣ IRQ Mode (IRQ)
Normal Interrupt Request mode
Used for standard interrupts

4️⃣ Supervisor Mode (SVC)
Entered after reset
Used by OS or privileged tasks

5️⃣ Abort Mode (ABT)
Entered on memory access faults

6️⃣ Undefined Mode (UND)
Entered when an undefined instruction is executed

7️⃣ System Mode (SYS)
Privileged mode like Supervisor
Used for running OS tasks
