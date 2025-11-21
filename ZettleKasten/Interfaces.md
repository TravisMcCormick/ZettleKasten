**Tags:** #Golang #Interfaces #Programming #Fundamentals #Polymorphism

---

### Definition

**Interfaces** in Go define sets of method signatures that types must implement. Go uses implicit interface satisfaction—any type that implements the required methods automatically satisfies the interface, enabling polymorphism without explicit declarations.

### Key Concepts

- Define interfaces as sets of method signatures:
```go
type Stringer interface { String() string }
```

- Any struct implementing those methods satisfies the interface automatically.
- Favor **small** interfaces (one or few methods) and define them where they're used.

### Best Practices

- **Small Interfaces**: The smaller the interface, the more powerful it is (interface segregation)
- **Define at Use Site**: Define interfaces where they're consumed, not where they're implemented
- **Implicit Satisfaction**: No explicit "implements" keyword required
- **Composition Over Inheritance**: Combine small interfaces to build larger ones

### Common Go Interfaces

- `io.Reader` and `io.Writer`: Fundamental I/O abstractions
- `error`: Built-in error handling interface
- `fmt.Stringer`: Custom string representation

### Personal Insight

Go's approach to interfaces is one of its most elegant features. Implicit interface satisfaction and the emphasis on small interfaces lead to highly decoupled, testable code. The "accept interfaces, return structs" principle is fundamental to idiomatic Go design.

---

### Related Notes

- [[Go Structs Overview]]
- [[Go Structs vs. C++ Classes]]
- [[Best Practices for Go Structures]]
- [[Embedding (Composition)]]