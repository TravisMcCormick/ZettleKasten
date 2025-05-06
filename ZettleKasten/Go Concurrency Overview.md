
---
Tags: #golang #concurrency #fundamentals

Concurrency in Go is built around **goroutines** and **channels**, enabling lightweight, scalable parallelism. Goroutines are user-space threads managed by the Go runtime. Channels provide typed communication and coordination between goroutines. Additional synchronization patterns—`sync.WaitGroup`, context cancellation, fan-in/fan-out—help manage lifecycle, cancellation, and data flow. Go’s scheduler multiplexes goroutines onto OS threads, hiding much of the complexity from the developer.

---
### Related Notes:

1. [What Is an OS Thread?](What%20Is%20an%20OS%20Thread?.md)
2. [What Is a Goroutine?](What%20Is%20a%20Goroutine?.md)
3. [Thread vs. Goroutine](Thread%20vs.%20Goroutine.md)
4. [The Go Scheduler (G-M-P Model)](The%20Go%20Scheduler%20(G-M-P%20Model).md)
5. [Context-Switching (OS vs. Go)](Context-Switching%20(OS%20vs.%20Go).md)
6. [Goroutine Lifecycle & Natural Termination](Goroutine%20Lifecycle%20&%20Natural%20Termination.md)
7. [Why You Must Coordinate Completion](Why%20You%20Must%20Coordinate%20Completion.md)
8. [Pattern - sync.WaitGroup](Pattern%20-%20sync.WaitGroup.md)
9. [Pattern - Channel-Fan-In](Pattern%20-%20Channel-Fan-In.md)
10. [Pattern - Context Cancellation](Pattern%20-%20Context%20Cancellation.md)