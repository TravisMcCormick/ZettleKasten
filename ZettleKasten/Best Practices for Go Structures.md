**Tags:** #golang #programming #best-practices #software-development

---

### **Best Practices**

- **Design for Zero-Value Usability**: zero struct should work without extra init.
- **Export Only What's Needed**: capitalize only truly public fields.
- **Pointer vs. Value Receivers**: use pointer receivers if methods modify state or struct is large; value receivers otherwise—be consistent.
- **Value vs. Pointer**: small, immutable data can be value; large or shared data pointers.
- **Prefer Composition**: use embedding instead of inheritance.
- **Constructor Functions**: use `NewType` when complex initialization or invariants are needed.
- **Immutability by Convention**: keep fields unexported and expose only read methods if needed.
- **Tags for Metadata**: use `json`, `xml`, `db`, etc., tags to guide serialization or mapping.
- **Field Ordering**: for performance, group same-size fields together to minimize padding.
- **Deep vs. Shallow Copy**: remember that assigning structs copies fields; maps/slices inside remain shared references.
- **Concurrency**: protect mutable struct fields with synchronization primitives.

---

### **Related Notes**

- [[Go Structs Overview]]
- [[Defining a Struct in Go]]
- [[Initializing Go Structs]]
- [[Struct Tags]]
- [[Embedding (Composition)]]
- [[Memory Management of Structs]]
- [[Go Structs vs. C++ Classes]]
- [[Development Best Practices]]
