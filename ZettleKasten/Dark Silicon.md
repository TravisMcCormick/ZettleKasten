**Tags:** #computer-architecture #hardware #power-management #chip-design

---

### **Definition**

**Dark Silicon** refers to portions of a microprocessor chip that must remain powered off (dark) at any given time due to power consumption and thermal constraints, even though those transistors are physically present and functional.

### **Characteristics**

- **Power Wall**: Physical limitation preventing all transistors from being powered simultaneously
- **Thermal Constraints**: Heat dissipation limits active chip area
- **Dennard Scaling Breakdown**: End of voltage scaling benefits that previously managed power density
- **Utilization Trade-offs**: More transistors available than can be used at once

### **Causes**

- **Moore's Law Continuation**: Transistor counts continue to increase
- **Power Density Limits**: Cannot safely dissipate heat from all active transistors
- **Voltage Scaling Plateau**: Cannot reduce voltage further without reliability issues
- **Thermal Design Power (TDP)**: Fixed power budget for chip operation

### **Implications**

- **Specialized Accelerators**: Chips include specialized units (GPU cores, AI accelerators) used only when needed
- **Dynamic Resource Allocation**: Cores and functional units powered on/off dynamically
- **Heterogeneous Computing**: Mix of different processor types (big.LITTLE architecture)
- **Performance Limitations**: Cannot run all features simultaneously at full speed

### **Mitigation Strategies**

- **Power Gating**: Selectively shutting down unused circuit blocks
- **Dynamic Voltage and Frequency Scaling (DVFS)**: Adjusting power based on workload
- **Specialized Accelerators**: Purpose-built circuits for specific tasks (more efficient)
- **Heterogeneous Architectures**: Different cores for different efficiency/performance needs
- **3D Chip Stacking**: Improved thermal management through vertical integration

### **Related Notes**

- [[CPU (Central Processing Unit)]]
- [[Computer Architecture Basics]]
- [[CPU Performance Metrics]]
- [[Computer Hardware Components]]
- [[System Interconnects]]
- [[Instruction Set Architecture]]

