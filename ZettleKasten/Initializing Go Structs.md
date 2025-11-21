**Tags:** #Golang #Structs #Programming #Initialization #Fundamentals

---

### Definition

**Initializing Go Structs** covers the various methods for creating and initializing struct instances in Go, from composite literals to constructor functions.

### Initialization Methods

1. **Composite Literal with Field Names** (idiomatic):
```go
p := Person{Name: "Bob", Age: 25}
```

2. **Composite Literal by Order** (less clear):
```go
    q := Person{"Carol", 40}
```

3. **Zero Value + Assignment**:
```go
var r Person r.Name = "Dan"
```

4. **Pointer Allocation**:
```go
s := &Person{Name: "Eve", Age: 22} 
t := new(Person)  // zero-valued, pointer
```

5. **Constructor Function**:
```go
func NewPerson(name string) *Person {     
	return &Person{Name: name, Age: 18} 
}
```


Fields not specified are set to their zero value (e.g., `""` for strings, `0` for ints).

### Personal Insight

The composite literal with field names is the most idiomatic Go approach, providing clarity and maintainability. Constructor functions are useful when initialization logic is needed. Understanding zero values is crucial for writing correct Go code.

---

### Related Notes

- [[Go Structs Overview]]
- [[Defining a Struct in Go]]
- [[Memory Management of Structs]]
- [[Best Practices for Go Structures]]