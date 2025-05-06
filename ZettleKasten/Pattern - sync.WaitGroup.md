
---

**Use Case:** Waiting for a known number of goroutines.

```go
var wg sync.WaitGroup
for i := 1; i <= N; i++ {
  wg.Add(1)
  go func(id int) {
    defer wg.Done()
    // work…
  }(i)
}
wg.Wait()
```

- `Add(n)` before spawn
- Each goroutine calls `Done()`
- `Wait()` blocks until counter is zero

---