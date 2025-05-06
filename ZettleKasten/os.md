
---

- For interacting with the operating system (files, environment, processes, standard input/output)

| Function                  | What it does                                                                                             |
| ------------------------- | -------------------------------------------------------------------------------------------------------- |
| os.Stdout                 | Represents standard output (your terminal). Used for writing output manually.                            |
| os.Stderr                 | Represents standard error (your terminal's error stream). Used for error messages.                       |
| os.Stdin                  | Represents standard input (user input via keyboard or piped data).                                       |
| os.Create("file.txt")\|   | Creates a new file named `file.txt` (or truncates it if it exists) and opens it for writing              |
| os.Open("file.txt")       | Opens an existing file named `file.txt` for reading.                                                     |
| os.Remove("file.txt")     | Deletes the file named `file.txt`                                                                        |
| os.Getenv("VAR")          | Retrieves the value of the environment variable named `VAR`.                                             |
| os.Setenv("VAR", "value") | Sets an environment variable `VAR` to the specified "value"                                              |
| os.Args                   | Slice of strings containing all command-line arguments passed to the program                             |
| os.Exit(1)                | Immediately terminates the program with the given exit code (`1` usually means error; `0` means success) |
| os.Getwd()                | Returns the current working directory of the program                                                     |
| os.Chdir("/path")         | Changes the working directory to the specified path.                                                     |

---