
---

```go
func sum(numbers ...int) int {
	total := 0
	for _, n := range numbers {
		total += n
	}
	return total
}

func main() {
	fmt.Println(sum(1, 2, 3, 4)) // 10
}
```

---
### Key Ideas:

- Use ...type in the parameter list to accept a variable number of arguments.
- Inside the function, the variadic parameter behaves like a slice.