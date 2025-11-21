**Tags:** #Golang #C #Structs #Programming #Comparison #DataStructures

---

### Definition

A comparison between Go structs and C structs, highlighting their similarities and differences in memory layout, functionality, and language features.

### Comparison

**Similarities**
- Contiguous memory layout, similar to C structs.
- Value-type semantics: assignment copies all fields.

**Differences**

- **Struct Tags**: Go supports back-tick metadata (e.g., `json:"id"`).
- **Methods**: Go structs can have attached methods; C structs cannot.
- **Encapsulation**: Go fields can be unexported; C struct fields are all visible if the struct is visible.
- **Initialization**: Go always zeroes new structs; C local structs may be uninitialized.
- **Memory**: Go is garbage-collected; C requires manual `malloc`/`free`.
- **Type Safety**: Go disallows unsafe pointer casts that C would allow.

### Personal Insight

Go structs modernize the C struct concept by adding methods, encapsulation, and memory safety while maintaining the efficiency of value semantics. The garbage collection and type safety make Go structs safer and more convenient than C structs, though at the cost of some low-level control.

---

### Related Notes

- [[Go Structs Overview]]
- [[Memory Management of Structs]]
- [[Defining a Struct in Go]]
- [[Go Structs vs. C++ Classes]]
