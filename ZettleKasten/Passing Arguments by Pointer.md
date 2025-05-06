
---

```go
func increment(x *int) {
	*x++
}

func main() {
	a := 5
	increment(&a)
	fmt.Println(a) // 6
}
```

---
### Key Ideas:

- Passing pointers allows modifying the original argument.
- Use & to pass the address of a variable, and * to dereference the pointer.

---
### Related Notes:

- [Passing Arguments by Value](Passing%20Arguments%20by%20Value.md)

---