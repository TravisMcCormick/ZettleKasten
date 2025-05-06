
---

```go
func apply(op func(int, int) int, a, b int) int {
	return op(a, b)
}

func add(x, y int) int {
	return x + y
}

func main() {
	result := apply(add, 2, 3)
	fmt.Println(result) // 5
}
```

---
### Key Ideas:

- Functions can accept other functions as parameters.
- Enables functional programming styles and abstractions.