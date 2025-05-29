
---
- Attach metadata to fields with backticks:
```go
type User struct {
    ID   int    `json:"id"`
    Name string `json:"name,omitempty"`
}
```
- Common uses: JSON, XML, database mapping, validation.
- Accessible via reflection if you need custom processing.

---
### Related Notes:
- [[Best Practices for Go Structures]]