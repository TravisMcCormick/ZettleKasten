**Tags:** #concurrency #synchronization #programming #deadlock #operating-systems

---

### **Definition**

Avoiding deadlocks and starvation involves implementing strategies in concurrent programming to ensure that multiple processes or threads do not get indefinitely blocked (deadlocks) or deprived of necessary resources (starvation). Deadlocks occur when a set of processes are each waiting for another to release a resource, creating a cycle of dependencies that halts progress. Starvation happens when a process never gets the resources it needs to proceed because other processes are continuously favored.

### **Causes**

- **Circular Wait:** Processes hold resources and wait for others in a circular chain.
- **Hold and Wait:** Processes holding resources can request additional resources.
- **No Preemption:** Resources cannot be forcibly taken away from processes.
- **Mutual Exclusion:** At least one resource must be held in a non-shareable mode.

### **Prevention Techniques**

- **Resource Ordering:** Assign a global order to resource acquisition to prevent circular wait.
- **Lock Timeouts:** Implement timeouts for resource requests to break potential deadlocks.
- **Deadlock Detection Algorithms:** Periodically check for deadlocks and recover if found.
- **Avoid Hold and Wait:** Require processes to request all needed resources at once.

### **Examples**

- **Dining Philosophers Problem:** A classic synchronization problem illustrating deadlock and starvation.
- **Database Transactions:** Ensuring that transactions do not cause deadlocks when accessing shared data.

### **Related Notes**

- [[Deadlocks and Starvation]]
- [[Best Practices in Synchronization]]
- [[Critical Section Problem]]
- [[Mutexes]]
- [[Synchronization Primitives]]
- [[Classic Synchronization Problems]]
- [[Monitors in Synchronization]]
- [[Kernel vs. User Space Synchronization]]