**Tags**: #ComputerArchitecture #CPU #Hardware #ComputerScience

---

### Definition

The **Central Processing Unit (CPU)** is the primary component of a computer that performs most of the processing inside a computer. It executes instructions from programs by performing basic arithmetic, logical, control, and input/output (I/O) operations specified by the instructions.

### Components

- **Arithmetic Logic Unit (ALU)**: Performs arithmetic and logical operations.
- **Control Unit (CU)**: Directs the operation of the processor by fetching instructions and decoding them.
- **Registers**: Small, fast storage locations within the CPU used to hold data and instructions temporarily.
- **Cache**:
    - **L1 Cache**: Smallest and fastest cache level, located closest to the CPU cores.
    - **L2 Cache**: Larger and slightly slower than L1, often shared between cores.
    - **L3 Cache**: Even larger and slower, typically shared across all cores in multi-core processors.

### Performance Metrics

- **Clock Speed**: Measured in GHz, indicates how many cycles a CPU can perform per second.
- **Cores and Threads**: Multiple cores and threads allow parallel processing, enhancing performance.
- **Cache Size**: Larger caches can store more data closer to the CPU, reducing access times.
- **Instruction Set Architecture (ISA)**: Defines the supported instructions and their execution.
- **Power Consumption**: Influences performance and thermal management.

### Types of CPUs

- **Single-Core CPU**: Contains one core; executes one thread at a time.
- **Multi-Core CPU**: Contains multiple cores; can execute multiple threads concurrently.
- **Embedded CPU**: Designed for specific applications within embedded systems.
- **Server CPU**: Optimized for handling large-scale computations and multi-threaded applications.

### Security Considerations

- **Hardware Vulnerabilities**: Such as Spectre and Meltdown, which exploit speculative execution.
- **Secure Boot**: Ensures that the CPU only executes trusted firmware and software during startup.
- **Trusted Execution Environments (TEE)**: Provides a secure area within the CPU for sensitive operations.

### Personal Insight

**The CPU is often referred to as the "brain" of the computer**, playing a crucial role in determining overall system performance and capabilities. Advances in CPU technology, such as increased core counts and enhanced instruction sets, continue to drive improvements in computing power and efficiency, enabling more complex and demanding applications.

### Related Notes

- [[Computer Architecture Basics]]
- [[Memory Hierarchy]]
- [[Instruction Set Architecture]]
- [[CPU Performance Metrics]]
- [[ZettleKasten/Hardware Security]]