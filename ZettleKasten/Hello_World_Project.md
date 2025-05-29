
---

Description: Simple Hello World to show all the different prints in Go

---

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

---