**Tags:** #Golang #Concurrency #Programming #Fundamentals #Goroutines #Channels

---

### Definition

Concurrency in Go is built around **goroutines** and **channels**, enabling lightweight, scalable parallelism. Goroutines are user-space threads managed by the Go runtime. Channels provide typed communication and coordination between goroutines. Additional synchronization patterns—`sync.WaitGroup`, context cancellation, fan-in/fan-out—help manage lifecycle, cancellation, and data flow. Go's scheduler multiplexes goroutines onto OS threads, hiding much of the complexity from the developer.

---
### Related Notes:

1. [[What Is an OS Thread]]
2. [[What Is a Goroutine]]
3. [[Thread vs. Goroutine]]
4. [[The Go Scheduler (G-M-P Model)]]
5. [[Context-Switching (OS vs. Go)]]
6. [[Goroutine Lifecycle & Natural Termination]]
7. [[Why You Must Coordinate Completion]]
8. [[Pattern - sync.WaitGroup]]
9. [[Pattern - Channel-Fan-In]]
10. [[Pattern - Context Cancellation]]