
---

**Model:**
- **G** (goroutines)
- **M** (OS threads, “machines”)
- **P** (logical processors)

**How it works:**

1. A fixed number of Ps
2. Each P has a queue of Gs
3. An M picks up a P to run its G queue
4. Idle Ps “steal” work from busy Ps    

---
### Related Notes:
- [[Thread vs. Goroutine]]
- [[Context-Switching (OS vs. Go)]]