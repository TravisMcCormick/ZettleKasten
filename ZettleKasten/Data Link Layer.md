**Tags:** #networking #osi-model #data-link-layer #protocols

---

### **Definition**

The **Data Link Layer** is the second layer (Layer 2) in the OSI Model. It provides node-to-node data transfer—a link between two directly connected nodes. It also handles error detection and correction from the Physical Layer.

### **Functions**

1. **Framing:**
    
    - Encapsulates packets received from the Network Layer into frames for transmission.
    - Adds headers and trailers containing control information.
2. **Physical Addressing:**
    
    - Uses MAC addresses to identify devices on the same network.
3. **Error Detection and Correction:**
    
    - Implements mechanisms like Cyclic Redundancy Check (CRC) to detect errors in frames.
4. **Flow Control:**
    
    - Manages the pacing of data transmission between devices to prevent overwhelming a receiver.
5. **Media Access Control:**
    
    - Coordinates access to the shared physical medium to avoid collisions (e.g., CSMA/CD in Ethernet).

### **Sub-Layers**

The Data Link Layer is divided into two sub-layers:

- **Logical Link Control (LLC):**
    
    - Handles error checking and flow control.
    - Provides a standardized interface for the Network Layer protocols.
- **Media Access Control (MAC):**
    
    - Controls how devices on the network gain access to the medium and permission to transmit data.

### **Importance in Networking**

- **Reliable Transmission:** Ensures data is transferred reliably over the physical medium.
- **Interoperability:** Standardizes protocols to allow devices from different manufacturers to communicate.

### **Personal Insight**

The Data Link Layer is crucial for local network communication. It bridges the gap between the physical signals on the hardware and the higher-level protocols, ensuring data integrity and proper delivery.

### **Related Notes**

- [[OSI Model]]
- [[OSI Model Overview]]
- [[Physical Layer]]
- [[Network Layer]]
- [[MAC Addresses]]
- [[Ethernet Protocol]]
- [[Address Resolution Protocol (ARP)]]
- [[Switches and Hubs]]
- [[Networking Protocols]]