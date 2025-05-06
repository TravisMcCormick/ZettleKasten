

---
- Define interfaces as sets of method signatures:
```go
type Stringer interface { String() string }
```

- Any struct implementing those methods satisfies the interface automatically.
- Favor **small** interfaces (one or few methods) and define them where they’re used.

---
### Related Notes:
- [Go Structs vs. C++ Classes](Go%20Structs%20vs.%20C++%20Classes.md)
- [Best Practices for Go Structures](Best%20Practices%20for%20Go%20Structures.md)