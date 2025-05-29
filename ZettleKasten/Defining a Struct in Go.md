
---

Go **structs** are custom data types that group together named fields under one name. To define one, use the `type` keyword, the struct name, and the `struct` keyword with its fields in braces:

```go
type Person struct {
    Name string
    Age  int
}
```

- **Exported vs. Unexported**: Field names starting with an uppercase letter (e.g., `Name`) are visible outside the package; lowercase names are private to the package.
- **Methods** can be attached later to give the struct behavior.

**Example Usage:**

```go
p := Person{}         // zero-value struct
p.Name = "Alice"
p.Age  = 30
fmt.Println(p.Name, p.Age)
```

---
### Related Notes:
- [[Initializing Go Structs]]
- [[Best Practices for Go Structures]]
