**Tags:** #Golang #Programming #Tutorial #CodeExample #fmt

---

### Definition

A **Hello World Project** demonstrating all the different print functions available in Go's fmt package. This example showcases Print, Println, Printf, Sprint, Sprintln, Sprintf, Fprint, Fprintln, Fprintf, and Errorf functions.

### Purpose

- **Educational**: Demonstrates the differences between print function variants
- **Reference**: Provides a quick reference for fmt package usage
- **Comparison**: Shows how each function behaves differently

---

### Code Example

```go
package main

import (
"fmt"
"os"
)

func main() {
	fmt.Print("Hello world")
	fmt.Print(" <- still same line\n")
	fmt.Println("Hello world")
	fmt.Printf("Hello world\n")
	
	str1 := fmt.Sprint("Hello world")
	fmt.Println("Sprint result:", str1)
	  
	str2 := fmt.Sprintln("Hello world")
	fmt.Print("Sprintln result:", str2)
	
	str3 := fmt.Sprintf("Hello world")
	fmt.Println("Sprintf result:", str3)
	  
	fmt.Fprint(os.Stdout, "Hello world (Fprint)")
	fmt.Fprint(os.Stdout, "\n")
	  
	fmt.Fprintln(os.Stdout, "Hello world (Fprintln)")
	
	fmt.Fprintf(os.Stdout, "Hello world (Fprintf)\n")
	
	err := fmt.Errorf("hello world (errorf)")
	fmt.Println("Generated error:", err)
}
```

### Key Takeaways

- **Print family**: Outputs directly to stdout
- **Sprint family**: Returns strings instead of printing
- **Fprint family**: Writes to any io.Writer interface
- **Errorf**: Creates error objects with formatted messages

### Personal Insight

This comprehensive example is invaluable for understanding Go's formatted I/O system. The distinction between Print/Sprint/Fprint families is fundamental to effective Go programming, especially when working with different output targets like files, network connections, or string builders.

---

### Related Notes

- [[fmt]]
- [[Go Functions Overview]]
