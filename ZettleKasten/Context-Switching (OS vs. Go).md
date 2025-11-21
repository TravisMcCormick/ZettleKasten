**Tags:** #golang #concurrency #operating-systems #performance #goroutines

---

### **Definition**

**Context-Switching** refers to the process of storing and restoring the state (context) of a process or thread so that execution can be resumed from the same point at a later time. This process differs significantly between OS-level threads and Go's goroutines.

### **OS Threads**

- Involves kernel calls (register/memory save & restore)
- High latency due to kernel involvement
- More resource-intensive
- Managed by the operating system kernel
- Heavier weight context switch

### **Goroutines**

- User-space switch by Go runtime
- Faster, lower overhead
- Managed by Go scheduler without kernel involvement
- Lightweight context switch
- Can have hundreds of thousands of goroutines efficiently

### **Impact**

- High scalability for I/O-bound and massively concurrent tasks
- Go's approach enables handling many more concurrent operations with less overhead
- Better CPU cache utilization with goroutines
- Reduced memory footprint per concurrent operation

---

### **Related Notes**

- [[Go Concurrency Overview]]
- [[What Is a Goroutine]]
- [[What Is an OS Thread]]
- [[Thread vs. Goroutine]]
- [[The Go Scheduler (G-M-P Model)]]
- [[Goroutine Lifecycle & Natural Termination]]
- [[Processes and Threads]]
- [[Concurrency and Parallelism]]
- [[Performance Considerations]]
