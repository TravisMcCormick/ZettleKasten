
---
1. **Composite Literal with Field Names** (idiomatic):=
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

---
### Related Notes:
- [[Memory Management of Structs]]
- [[Best Practices for Go Structures]]