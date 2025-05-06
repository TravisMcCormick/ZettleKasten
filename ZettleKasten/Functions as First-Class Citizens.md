
---

```go
func greet(name string) string {
	return "Hello, " + name
}

func main() {
	f := greet
	fmt.Println(f("Bob"))
}
```

---
### Key Ideas:

- Functions can be assigned to variables.
- Functions can be passed as arguments or returned from other functions.