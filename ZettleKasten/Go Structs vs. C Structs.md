
---

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

---
### Related Notes:
- [Memory Management of Structs](Memory%20Management%20of%20Structs.md)
- [Defining a Struct in Go](Defining%20a%20Struct%20in%20Go.md)