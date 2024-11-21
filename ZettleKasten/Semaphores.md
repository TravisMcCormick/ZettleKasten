**Tags**: #Semaphores #Synchronization #Concurrency #Counting #Threads

---

### Definition

A **Semaphore** is a synchronization primitive used to control access to a common resource by multiple threads through the use of a counter, which represents the number of available resources or permits.

### Key Features

- **Types**:
    - **Counting Semaphore**:
        - Allows a set number of threads to access a resource.
    - **Binary Semaphore**:
        - Similar to a mutex but does not have ownership semantics.
- **Operations**:
    - **Wait (P operation)**:
        - Decrements the semaphore count; blocks if count is zero.
    - **Signal (V operation)**:
        - Increments the semaphore count; wakes blocked threads.
- **Use Cases**:
    - Resource counting (e.g., connection pools).
    - Signaling between threads (e.g., producer-consumer scenarios).
- **RTOS Usage**:
    - Used in interrupt service routines for signaling.
    - Require minimal latency for real-time constraints.

### Basic Usage

- **Initializing a Semaphore** (POSIX example):
    
``` c
    sem_t semaphore; sem_init(&semaphore, 0, initial_count);
```
    
- **Waiting on a Semaphore**:
    
``` c
    sem_wait(&semaphore); // Access shared resource
```
    
- **Signaling a Semaphore**:
    
``` c
    sem_post(&semaphore);
```
    

### Considerations

- **No Ownership**:
    - Any thread can signal or wait on the semaphore.
- **Potential for Misuse**:
    - Incorrect semaphore usage can lead to deadlocks or resource leaks.
- **Complexity**:
    - Counting semaphores can be more complex to manage than mutexes.

### Personal Insight

Semaphores are versatile but require careful management. They are powerful tools for controlling access to resources and coordinating thread activities.

### Related Notes

- [[Mutexes]]
- [[Synchronization Primitives]]
- [[Deadlocks and Starvation]]
- [[Real-Time Operating Systems (RTOS)]]