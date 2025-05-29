**Tags:** #Networking #Protocols #TCPIPModel

---
**More Details:**

- **How It Works:** TCP sends data in a specific order and makes sure each piece of information reaches the other computer. If something is missing or arrives out of order, TCP will resend it.
- **Connection-Oriented:** Before sending data, TCP establishes a connection between the two computers. They agree on how to communicate before any actual data is sent.
- **Reliability:** TCP ensures that all data arrives correctly and in the right order, making it very reliable.
- **Uses:** TCP is used when accuracy is crucial, such as:
    - **Web Browsing:** Loading websites where all the information needs to be correct.
    - **Email:** Sending messages where you need to make sure the entire email arrives.
- **Example:** Imagine TCP as sending a series of numbered letters through the mail. If a letter gets lost, you know exactly which one it was and can resend it, ensuring your friend gets the complete message in order.

### **Definition**

The **TCP/IP Model** is a concise framework used to design and implement network communications, consisting of four abstraction layers:

1. **Link Layer (Network Interface):**
    
    - Corresponds to OSI Layers 1 & 2.
    - Handles physical hardware and data link protocols.
2. **Internet Layer:**
    
    - Corresponds to OSI Layer 3.
    - Responsible for addressing, packaging, and routing functions.
3. **Transport Layer:**
    
    - Corresponds to OSI Layer 4.
    - Provides end-to-end communication services.
4. **Application Layer:**
    
    - Corresponds to OSI Layers 5, 6, & 7.
    - Supports application and higher-level protocols.

### **Importance**

- **Foundation of the Internet:** The protocols in the TCP/IP suite are the basis for global internet communication.
- **Interoperability:** Allows different types of computers and networks to communicate.

### **Related Notes**

- [[Networking Protocols]]
- [[OSI Model Overview]]
- [[Transport Layer]]