## Overview
This map covers concurrent programming concepts, synchronization primitives, and common concurrency problems across different programming paradigms.

---

## Concurrency Fundamentals

### Core Concepts
- [[Concurrency and Parallelism]]
- [[Processes and Threads]]
- [[Race Conditions]]
- [[Critical Section Problem]]

---

## Synchronization Primitives

### Mutual Exclusion
- [[Mutual Exclusion]]
- [[Mutexes]]
- [[Semaphores]]
- [[Monitors in Synchronization]]
- [[Synchronization Primitives]]

### Comparisons
- [[Differences Between Mutexes and Semaphores]]

---

## Synchronization Problems

### Common Issues
- [[Deadlocks and Starvation]]
- [[Avoiding Deadlocks and Starvation]]
- [[Priority Inversion]]

### Classic Problems
- [[Classic Synchronization Problems]]

---

## Implementation & Best Practices

### Implementation Details
- [[Implementation Details]]
- [[Kernel vs. User Space Synchronization]]
- [[System Calls for Synchronization]]

### Best Practices
- [[Best Practices in Synchronization]]
- [[Performance Considerations]]

---

## Real-Time Systems

### RTOS Considerations
- [[Real-Time Operating Systems (RTOS)]]
- [[Real-Time Constraints in Synchronization]]

---

## Go-Specific Concurrency

### Goroutines
- [[Go Concurrency Overview]]
- [[What Is a Goroutine]]
- [[Goroutine Lifecycle & Natural Termination]]
- [[Thread vs. Goroutine]]

### Coordination
- [[Why You Must Coordinate Completion]]
- [[Pattern - sync.WaitGroup]]
- [[Pattern - Channel-Fan-In]]
- [[Pattern - Context Cancellation]]

### Scheduler
- [[The Go Scheduler (G-M-P Model)]]
- [[Context-Switching (OS vs. Go)]]
