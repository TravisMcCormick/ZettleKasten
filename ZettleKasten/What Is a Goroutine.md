
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
- [What Is an OS Thread?](What%20Is%20an%20OS%20Thread?.md)
- [Why You Must Coordinate Completion](Why%20You%20Must%20Coordinate%20Completion.md)
