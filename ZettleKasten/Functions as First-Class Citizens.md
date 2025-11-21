**Tags:** #Golang #Programming #Functions #Fundamentals #HigherOrder

---

### Definition

In Go, **functions are first-class citizens**, meaning they can be treated like any other value. They can be assigned to variables, passed as arguments to other functions, and returned from functions.

### Code Example

```go
func greet(name string) string {
	return "Hello, " + name
}

func main() {
	f := greet
	fmt.Println(f("Bob"))
}
```

### Key Concepts

- **Assignable**: Functions can be assigned to variables.
- **Passable**: Functions can be passed as arguments to other functions.
- **Returnable**: Functions can be returned from other functions.
- **Enables**: Higher-order functions, callbacks, and functional programming patterns.

### Benefits

- **Flexibility**: Enables powerful abstraction patterns
- **Code Reusability**: Functions can be parameterized with behavior
- **Functional Programming**: Supports functional programming paradigms

### Personal Insight

First-class functions are one of Go's most powerful features, enabling elegant solutions to complex problems. They're essential for understanding Go's approach to abstraction and are fundamental to patterns like middleware, decorators, and dependency injection.

---

### Related Notes

- [[Go Functions Overview]]
- [[Anonymous Functions]]
- [[Higher-Order Functions]]
