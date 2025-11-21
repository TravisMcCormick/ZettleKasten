**Tags:** #golang #programming #functions

---

### **Definition**

Functions in Go can return one or more values. Return types are specified after the parameter list, and the `return` keyword sends values back to the caller.

### **Example**

```go
func add(a int, b int) int {
	return a + b
}

func main() {
	result := add(3, 4)
	fmt.Println(result) // 7
}
```

### **Key Ideas**

- Functions specify return types after the parameter list
- `return` keyword sends a value back to the caller
- Functions can have multiple return values
- Named return values are supported
- Common pattern: return value and error

---

### **Related Notes**

- [[Go Functions Overview]]
- [[Defining and Calling a Function]]
- [[Multiple Return Values]]
- [[Named Return Values]]
- [[Anonymous Functions]]
- [[Higher-Order Functions]]
