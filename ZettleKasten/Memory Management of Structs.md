
---

- Go is **garbage-collected**. You never manually `free` or `delete` a struct.
- When no references to a struct remain, the GC reclaims its memory automatically.
- If a struct holds external resources (files, connections), provide an explicit `Close()` or similar method to release them.

---
### Related Notes:
- [Best Practices for Go Structures](Best%20Practices%20for%20Go%20Structures.md)