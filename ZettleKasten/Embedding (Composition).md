
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
- [Interfaces](Interfaces.md)
- [Best Practices for Go Structures](Best%20Practices%20for%20Go%20Structures.md)