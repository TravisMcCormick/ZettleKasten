**Tags:** #golang #programming #functions

---

### **Definition**

Anonymous (unnamed) functions are defined inline without a name. They are useful for simple operations and passing as arguments to other functions.

### **Example**

```go
func main() {
	add := func(a, b int) int {
		return a + b
	}
	fmt.Println(add(2, 3)) // 5
}
```

### **Key Ideas**

- Anonymous functions can be assigned to variables
- Useful for simple operations and passing as arguments
- Can capture variables from surrounding scope (closures)
- Commonly used in goroutines and defer statements

---

### **Related Notes**

- [[Go Functions Overview]]
- [[Defining and Calling a Function]]
- [[Higher-Order Functions]]
- [[Functions as First-Class Citizens]]
- [[Go Concurrency Overview]]
