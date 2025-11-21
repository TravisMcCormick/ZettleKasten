**Tags:** #Golang #Programming #IO #Formatting #StandardLibrary

---

### Definition

The **fmt package** in Go provides formatted I/O functions for printing, scanning, and string formatting. It's one of the most commonly used packages in Go, essential for console output, string formatting, and error creation.

### Overview

| Function                            | What is Does                                                                                                                                               |
| ----------------------------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------- |
| fmt.Println("Hello, World")         | Prints text with a newline automatically at the end.                                                                                                       |
| fmt.Print("Hello, World")           | Prints literal text (what you give it) exactly as-is, no formatting.                                                                                       |
| fmt.Printf("Hello, World")          | Prints formatted text, using placeholders (like `%s`, `%d`, `%f`).                                                                                         |
| fmt.Sprint("Hello world")           | Returns the string "Hello world" â€” it does not print to the console.  <br>(You could assign it to a variable.)                                             |
| fmt.Sprintln("Hello world")         | Returns the string "Hello world\n" â€” with a newline character at the end.  <br>(Again, it doesnâ€™t print until you explicitly output it.)                   |
| fmt.Sprintf("Hello world")          | Returns a formatted string ("Hello world") â€” same idea as `Printf`, but it returns it instead of printing.  <br>(Useful for building strings dynamically.) |
| fmt.Fprint(writer, "Hello world")   | Writes Hello world to an io.Writer (like a file, buffer, or network socket), without a newline.                                                            |
| fmt.Fprintln(writer, "Hello world") | Writes Hello world to an io.Writer and adds a newline at the end.                                                                                          |
| fmt.Fprintf(writer, "Hello world")  | Writes Hello world to an io.Writer with formatting rules, but no automatic newline.                                                                        |
| fmt.Errorf("Hello world")           | Creates a new `error` object with the message "Hello world".  <br>    (Commonly used when returning dynamic or structured errors.)                         |

### Common Format Verbs

- `%s` - String
- `%d` - Decimal integer
- `%f` - Floating point number
- `%t` - Boolean
- `%v` - Default format (any value)
- `%T` - Type of value
- `%p` - Pointer address

### Personal Insight

The fmt package is fundamental to Go programming. Understanding the difference between Print, Sprint, and Fprint families is crucial for effective Go development, especially when working with different output targets like files, network connections, or string builders.

---

### Related Notes

- [[Go Functions Overview]]
