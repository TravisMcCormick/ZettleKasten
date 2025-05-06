
---

**Use Case:** Graceful shutdown or early exit of multiple goroutines.

```go
ctx, cancel := context.WithCancel(context.Background())
go worker(ctx)
// …
cancel() // signals all workers to stop

```

- Goroutines must `select` on `ctx.Done()`
- Cooperative “kill” mechanism

---
### Related Notes:
- [Goroutine Lifecycle & Natural Termination](Goroutine%20Lifecycle%20&%20Natural%20Termination.md)