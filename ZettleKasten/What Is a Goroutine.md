
---

**Definition:** A lightweight, user-space thread managed by the Go runtime.  
**Key Properties:**
- Starts with ≈2 KB stack
- Scheduled by Go’s runtime (not the OS)
- Cheap to create and destroy
- Millions can coexist with minimal overhead
```go
go func() {
    fmt.Println("Hello from a goroutine!")
}()
```


---
### Related Notes:
- [[What Is an OS Thread]]
- [[Why You Must Coordinate Completion]]
