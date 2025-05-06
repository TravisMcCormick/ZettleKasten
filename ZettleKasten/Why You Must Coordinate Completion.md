
---

**Problem:** If `main()` exits before other goroutines return, they are abruptly terminated.  
**Solution:** Employ synchronization so `main()` blocks until all children finish.

---
### Related Notes:
- [Pattern - sync.WaitGroup](Pattern%20-%20sync.WaitGroup.md)
- [Pattern - Channel-Fan-In](Pattern%20-%20Channel-Fan-In.md)