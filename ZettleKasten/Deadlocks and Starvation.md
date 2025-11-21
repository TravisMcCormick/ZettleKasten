**Tags:** #concurrency #synchronization #deadlock #starvation #threading

---

### Definition

- **Deadlock**: A situation where two or more threads are blocked forever, each waiting for the other to release resources.
- **Starvation**: A thread waits indefinitely because other threads are continually monopolizing the resource.

### Key Features

- **Deadlocks**:
    - **Conditions**:
        - Mutual exclusion.
        - Hold and wait.
        - No preemption.
        - Circular wait.
    - **Detection and Recovery**:
        - Deadlock detection algorithms.
        - Resource preemption.
- **Starvation**:
    - Occurs due to unfair scheduling or resource allocation.
    - More prevalent in systems without proper priority management.
- **RTOS Considerations**:
    - Deadlocks and starvation can cause missed deadlines, leading to system failure.
    - Employ strategies like priority inheritance to mitigate issues.

### Prevention Strategies

- **Deadlocks**:
    - Resource hierarchy (lock ordering).
    - Avoid hold and wait by acquiring all resources at once.
- **Starvation**:
    - Use fair scheduling algorithms.
    - Implement aging to increase priority over time.

### Personal Insight

Deadlocks and starvation are critical issues that can severely impact system reliability. Preventative design and careful resource management are essential.

### **Related Notes**

- [[Avoiding Deadlocks and Starvation]]
- [[Mutexes]]
- [[Synchronization Primitives]]
- [[Critical Section Problem]]
- [[Priority Inversion]]
- [[Classic Synchronization Problems]]
- [[Mutual Exclusion]]
- [[Concurrency and Parallelism]]
- [[Best Practices in Synchronization]]