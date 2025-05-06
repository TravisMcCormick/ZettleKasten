
---

**OS Threads:**
- Involves kernel calls (register/memory save & restore)
- High latency

**Goroutines:**
- User-space switch by runtime
- Faster, lower overhead

**Impact:**
- High scalability for I/O-bound and massively concurrent tasks

---