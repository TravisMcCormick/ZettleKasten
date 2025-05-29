
---

**Core Idea:** A goroutine ends when its function returns; Go’s garbage collector reclaims it.
- No manual “kill” API
- Return from `func` → goroutine exit

---
### Related Notes:
- [[Why You Must Coordinate Completion]]