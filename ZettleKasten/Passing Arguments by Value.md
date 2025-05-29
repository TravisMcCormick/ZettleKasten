
---

```go
func increment(x int) {
	x++
}

func main() {
	a := 5
	increment(a)
	fmt.Println(a) // 5, because passed by value
}
```

---
### Key Ideas:

- In Go, function arguments are passed by value by default.
- Changes to the parameter inside the function do not affect the original argument.

---
### Related Notes:

- [[Passing Arguments by Pointer]]

---