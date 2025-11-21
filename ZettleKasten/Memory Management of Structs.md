**Tags:** #Golang #Memory #GarbageCollection #Structs #Programming

---

### Definition

**Memory Management of Structs** in Go describes how the Go runtime handles allocation and deallocation of struct instances through garbage collection, eliminating manual memory management.

### Key Concepts

- Go is **garbage-collected**. You never manually `free` or `delete` a struct.
- When no references to a struct remain, the GC reclaims its memory automatically.
- If a struct holds external resources (files, connections), provide an explicit `Close()` or similar method to release them.

### Allocation

- **Stack Allocation**: Small, short-lived structs may be allocated on the stack
- **Heap Allocation**: Larger or escaped structs are allocated on the heap
- **Escape Analysis**: Compiler determines whether a struct can stay on the stack

### Best Practices

- **Resource Cleanup**: Implement Close() methods for structs holding external resources
- **Defer Pattern**: Use `defer` to ensure cleanup happens
- **Pool Reuse**: Consider sync.Pool for frequently allocated structs
- **Avoid Leaks**: Ensure no dangling references prevent garbage collection

### Personal Insight

Go's garbage collection simplifies memory management compared to C/C++, but understanding how it works helps write more efficient code. Knowing when to use pointers vs values affects both performance and memory usage.

---

### Related Notes

- [[Go Structs Overview]]
- [[Initializing Go Structs]]
- [[Best Practices for Go Structures]]
- [[memory footprint]]
- [[Memory Hierarchy]]