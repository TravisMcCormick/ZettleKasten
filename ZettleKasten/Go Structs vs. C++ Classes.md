
---
**Similarities**
- Both group data into a composite type.
- Both support methods: Go methods use a receiver parameter.
- You can create values or pointers in both.

**Key Differences**
- **No Inheritance** in Go; use **composition** via embedding.
- **Interfaces** replace virtual methods and class hierarchies.
- **Visibility** is by name capitalization, not `public`/`private`/`protected`.
- **Constructors/Destructors**: Go uses plain functions (`NewType`); no destructors—use explicit `Close()` if needed.
- **Zero Values**: Go structs always initialize to usable zero values; C++ requires explicit constructors.

**Embedding Example**:
```go
type Animal struct { Name string }
func (a *Animal) Speak() { fmt.Println(a.Name, "makes a sound") }

type Dog struct {
    Animal  // embedding
}
func (d *Dog) WagTail() { /* ... */ }

// Usage:
d := Dog{Animal{Name: "Fido"}}
d.Speak()
d.WagTail()
```

---
### Related Notes:
- [[Defining a Struct in Go]]
- [[Embedding (Composition)]]
- [[Interfaces]]