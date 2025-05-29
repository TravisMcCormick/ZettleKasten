
---
-  Embed structs without a field name to promote their fields and methods:
```go
type Address struct { City, State string }
type Person struct {
    Name    string
    Address  // embedded
}
```

- Access `p.City` directly; `p.City` is shorthand for `p.Address.City`.
- Embedding is composition, not inheritance: embedded methods receive the embedded type as receiver.

---
### Related Notes:
- [[Interfaces]]
- [[Best Practices for Go Structures]]