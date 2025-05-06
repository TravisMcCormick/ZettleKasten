
---

**Use Case:** Collecting results from an unknown or variable number of goroutines.

```go
results := make(chan string, N)
for i := 1; i <= N; i++ {
  go func(id int) {
    results <- fmt.Sprintf("Worker %d done", id)
  }(i)
}
for j := 1; j <= N; j++ {
  fmt.Println(<-results)
}
```

- Goroutines send on a buffered channel
- Main reads exactly N values

---