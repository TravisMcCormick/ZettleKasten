
---

- For input and out

| Function                            | What is Does                                                                                                                                               |
| ----------------------------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------- |
| fmt.Println("Hello, World")         | Prints text with a newline automatically at the end.                                                                                                       |
| fmt.Print("Hello, World")           | Prints literal text (what you give it) exactly as-is, no formatting.                                                                                       |
| fmt.Printf("Hello, World")          | Prints formatted text, using placeholders (like `%s`, `%d`, `%f`).                                                                                         |
| fmt.Sprint("Hello world")           | Returns the string "Hello world" — it does not print to the console.  <br>(You could assign it to a variable.)                                             |
| fmt.Sprintln("Hello world")         | Returns the string "Hello world\n" — with a newline character at the end.  <br>(Again, it doesn’t print until you explicitly output it.)                   |
| fmt.Sprintf("Hello world")          | Returns a formatted string ("Hello world") — same idea as `Printf`, but it returns it instead of printing.  <br>(Useful for building strings dynamically.) |
| fmt.Fprint(writer, "Hello world")   | Writes Hello world to an io.Writer (like a file, buffer, or network socket), without a newline.                                                            |
| fmt.Fprintln(writer, "Hello world") | Writes Hello world to an io.Writer and adds a newline at the end.                                                                                          |
| fmt.Fprintf(writer, "Hello world")  | Writes Hello world to an io.Writer with formatting rules, but no automatic newline.                                                                        |
| fmt.Errorf("Hello world")           | Creates a new `error` object with the message "Hello world".  <br>    (Commonly used when returning dynamic or structured errors.)                         |

---