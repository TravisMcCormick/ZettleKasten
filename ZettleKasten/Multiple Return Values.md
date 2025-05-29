
---

```go
func divide(dividend, divisor int) (int, int) {
	quotient := dividend / divisor
	remainder := dividend % divisor
	return quotient, remainder
} 

func main() {
	q, r := divide(13, 5)
	fmt.Println(q, r) // 2 3 
}
```

---
### **Key Ideas:**

- Functions can return multiple values using parentheses.
- Often used in error handling and complex computations.