
---

| Feature        | Thread (OS)                  | Goroutine (Go Runtime)            |
| -------------- | ---------------------------- | --------------------------------- |
| Managed by     | Operating System             | Go Runtime (user-space scheduler) |
| Memory         | ~1 MB stack                  | ~2 KB starting stack              |
| Creation Cost  | Expensive                    | Cheap                             |
| Scheduling     | By OS, costly context switch | Go's lightweight scheduler        |
| Blocking Model | Thread blocks                | Goroutine yields to others        |
| Scalability    | Limited (few thousands)      | High (millions possible)          |

---
### Related Notes:
- [[What is an OS Thread]]
- [[What is a Goroutine]]