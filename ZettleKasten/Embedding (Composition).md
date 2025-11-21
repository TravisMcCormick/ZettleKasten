**Tags:** #golang #programming #composition #structs #object-oriented

---

### **Definition**

**Embedding (Composition)** in Go allows you to embed structs without a field name to promote their fields and methods, creating a composition relationship rather than inheritance.

### **Example**

```go
type Address struct { City, State string }
type Person struct {
    Name    string
    Address  // embedded
}
```

### **Key Concepts**

- Access `p.City` directly; `p.City` is shorthand for `p.Address.City`
- Embedding is composition, not inheritance
- Embedded methods receive the embedded type as receiver
- Provides code reuse without inheritance complexity
- Can embed multiple types

---

### **Related Notes**

- [[Go Structs Overview]]
- [[Best Practices for Go Structures]]
- [[Interfaces]]
- [[Defining a Struct in Go]]
- [[Go Structs vs. C++ Classes]]
- [[Go Structs vs. Python Classes and Dicts]]
