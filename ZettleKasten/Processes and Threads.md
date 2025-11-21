**Tags:** #operating-systems #processes #threads #concurrency #multithreading

---

### Definition

- **Process**: An independent program in execution, with its own memory space.
- **Thread**: The smallest unit of processing within a process, sharing the same memory and resources.

### Key Features

- **Processes**:
    - Isolated memory spaces.
    - Communication via inter-process communication (IPC) mechanisms.
- **Threads**:
    - Shared memory within the same process.
    - Lightweight and faster context switching.
- **Multi-threading**:
    - Allows concurrent execution within a single process.
    - Improves application responsiveness.
- **Use Cases**:
    - Processes for running separate applications.
    - Threads for parallel tasks within an application.

### Personal Insight

Threads offer a powerful way to improve application performance through concurrency but require careful synchronization to prevent race conditions due to shared memory access.

### **Related Notes**

- [[Concurrency and Parallelism]]
- [[Synchronization Primitives]]
- [[Mutexes]]
- [[Thread vs. Goroutine]]
- [[What Is an OS Thread]]
- [[What Is a Goroutine]]
- [[Operating System Fundamentals]]
- [[Context-Switching (OS vs. Go)]]
- [[Go Concurrency Overview]]