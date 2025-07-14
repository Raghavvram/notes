# Process Control Block (PCB)

**Last Updated:** 2025-07-15

A **Process Control Block (PCB)** is a fundamental data structure in an operating system (OS) that contains all the information about a process. It acts as the central repository for managing and controlling a process throughout its entire lifecycle, from creation to termination.

## 1. Structure and Role of the PCB

The PCB is essentially a **process's identity card** or **metadata container**. Every time a new process is created, the OS allocates and initializes a unique PCB for it. When the process completes its execution, its corresponding PCB is deallocated.

The OS relies heavily on the PCB to:
*   **Uniquely Identify Processes:** Each PCB has a unique Process ID (PID).
*   **Monitor Process State:** Track the current status and progress of a process.
*   **Facilitate Process Scheduling:** Determine which process should run next and manage context switching.
*   **Manage Resources:** Keep track of resources allocated to the process.

## 2. Information Stored in the PCB

The information stored in a PCB can vary slightly between operating systems, but generally includes:

### Process Identification
*   **Process ID (PID):** A unique numerical identifier assigned to the process.
*   **Parent Process ID (PPID):** The PID of the process that created this process.

### Process State
Indicates the current operational status of the process:
*   **New:** The process is being created.
*   **Ready:** The process is waiting to be assigned to a processor.
*   **Running:** The process is currently executing instructions on the CPU.
*   **Waiting (Blocked):** The process is waiting for some event to occur (e.g., I/O completion, signal).
*   **Terminated:** The process has finished execution.

### CPU State Information
This information is crucial for enabling context switching:
*   **Program Counter (PC):** Stores the address of the next instruction to be executed for this process.
*   **CPU Registers:** All general-purpose registers, stack pointers, and other CPU registers that hold the process's computational state.

### Memory Management Information
Details about the memory allocated to the process:
*   **Base and Limit Registers:** Define the memory boundaries allocated to the process in simple memory management schemes.
*   **Page Tables or Segment Tables:** Used in virtual memory systems to map logical addresses to physical addresses.

### CPU Scheduling Information
Data used by the OS scheduler to manage process execution:
*   **Process Priority:** A numerical value indicating the process's importance relative to others.
*   **Pointers to Scheduling Queues:** Pointers to various queues (e.g., ready queue, wait queues) where the process might reside.

### I/O Information
Information related to the process's I/O operations:
*   List of open files.
*   List of I/O devices allocated to the process.
*   Buffers for I/O operations.

### Accounting Information
Data used for resource usage tracking and billing (in multi-user systems):
*   CPU time consumed.
*   Time limits.
*   Account numbers.

## 3. Role in Context Switching

One of the most critical functions of the PCB is to facilitate **context switching**. When the CPU switches from executing one process to another, the OS performs the following steps:

1.  **Save State:** The OS saves the current state of the running process (including its program counter, CPU registers, and other relevant data) into its PCB.
2.  **Load State:** The OS then loads the saved state of the next process (from its PCB) into the CPU registers.

This mechanism allows the OS to pause one process and resume another seamlessly, giving the illusion of concurrent execution of multiple processes.

## 4. Where is the PCB Stored?

The **Process Control Block (PCB)** is stored in a protected area of memory managed by the operating system, typically within the **kernel space**. This ensures that user-level applications cannot directly access or modify the PCB, preventing accidental corruption or malicious manipulation of process information.

PCBs are often organized into a **process table** or a similar data structure maintained by the OS. Each entry in this table corresponds to a PCB for an active process.

## Conclusion

The PCB is an indispensable component of any modern operating system. It serves as the central data structure that enables the OS to manage, schedule, and control processes effectively, ensuring efficient multitasking and resource allocation within the system.