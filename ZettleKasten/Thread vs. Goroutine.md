
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
- [What Is an OS Thread?](What%20Is%20an%20OS%20Thread?.md)
- [What Is a Goroutine?](What%20Is%20a%20Goroutine?.md)