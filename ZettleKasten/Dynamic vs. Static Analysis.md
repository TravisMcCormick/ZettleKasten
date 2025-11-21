**Tags:** #reverse-engineering #analysis #malware-analysis #security-testing

---

### Definition

**Dynamic Analysis** involves examining a program by executing it and observing its behavior, whereas **Static Analysis** examines code or binaries without execution. Both are essential techniques in reverse engineering and software testing.

### Static Analysis

- **Characteristics**:
    - Analyzes code without running it.
    - Tools: Disassemblers, decompilers.
- **Advantages**:
    - Safe from malicious code execution.
    - Can inspect all possible code paths.
- **Disadvantages**:
    - Cannot reveal runtime behavior.
    - Obfuscated code may hinder analysis.

### Dynamic Analysis

- **Characteristics**:
    - Involves running the program.
    - Tools: Debuggers, sandbox environments.
- **Advantages**:
    - Observes actual behavior.
    - Detects runtime issues like memory leaks.
- **Disadvantages**:
    - Risk of executing malicious code.
    - May not cover all execution paths.

### Use Cases

- **Security Testing**: Identify vulnerabilities and exploits.
- **Malware Analysis**: Understand malicious behavior.
- **Performance Profiling**: Optimize resource usage.

### Security Considerations

- **Isolation**: Use virtual machines or sandboxes during dynamic analysis.
- **Legal Compliance**: Ensure analysis activities are permitted.

### Personal Insight

**Employing both dynamic and static analysis provides a comprehensive understanding of software**, essential for thorough security assessments and reverse engineering efforts.

### **Related Notes**

- [[Techniques for Reverse Engineering]]
- [[Malware Analysis Techniques]]
- [[IDA Pro]]
- [[Ghidra]]
- [[Binary Ninja]]
- [[Debugging Techniques]]
- [[Debugging Tools]]
- [[Assembly Language Fundamentals]]
- [[Anti-Debugging Techniques]]