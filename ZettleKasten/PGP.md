**Tags:** #cryptography #encryption #security #privacy #email

---

### **Definition**

**PGP (Pretty Good Privacy)** is an encryption program that provides cryptographic privacy and authentication for data communication. It is commonly used for securing emails, files, and directories through encryption and digital signatures.

### **Core Functions**

- **Encryption**: Protects message confidentiality using hybrid encryption
- **Digital Signatures**: Verifies sender identity and message integrity
- **Key Management**: Generates and manages public/private key pairs
- **Compression**: Reduces message size before encryption

### **How PGP Works**

1. **Hybrid Encryption System**:
   - Uses symmetric encryption (fast) for the message content
   - Uses asymmetric encryption (secure) for the session key
   - Combines speed of symmetric with security of asymmetric encryption

2. **Encryption Process**:
   - Generate random session key
   - Encrypt message with session key (symmetric)
   - Encrypt session key with recipient's public key (asymmetric)
   - Send both encrypted message and encrypted session key

3. **Decryption Process**:
   - Recipient uses private key to decrypt session key
   - Use session key to decrypt actual message

### **Key Components**

- **Public Key**: Shared openly, used by others to encrypt messages to you
- **Private Key**: Kept secret, used to decrypt messages and sign documents
- **Key Pair**: Mathematically related public and private keys
- **Key Ring**: Collection of public keys from contacts
- **Key Fingerprint**: Short identifier to verify key authenticity
- **Web of Trust**: Decentralized trust model for key validation

### **Common Uses**

- Email encryption and signing
- File encryption
- Disk encryption
- Code signing
- Secure file transfer
- Identity verification

### **PGP Variants**

- **PGP (Original)**: Proprietary version by PGP Corporation (now Symantec)
- **OpenPGP**: Open standard (RFC 4880)
- **GPG (GnuPG)**: Free, open-source implementation of OpenPGP
- **Mailvelope**: Browser extension for webmail

### **Advantages**

- Strong end-to-end encryption
- Sender authentication through signatures
- Open standard with multiple implementations
- No central authority required (Web of Trust)
- Free implementations available

### **Challenges**

- Complex key management
- User interface difficulties
- Key distribution and verification problems
- Metadata not protected (sender, recipient, subject remain visible)
- Declining use in favor of Signal Protocol and modern alternatives

### **Best Practices**

- Keep private key secure and backed up
- Use strong passphrase for private key
- Regularly update keys with longer key lengths (4096-bit RSA or modern ECC)
- Verify key fingerprints out-of-band
- Revoke compromised keys immediately
- Set expiration dates on keys

### **Related Notes**

- [[Cryptographic Algorithms]]
- [[Symmetric vs. Asymmetric Encryption]]
- [[Digital Certificates]]
- [[Cryptographic Key Management]]
- [[Data Encryption Techniques]]
- [[Hash Functions]]
- [[Email Protocols]]
- [[Authentication Mechanisms]]

