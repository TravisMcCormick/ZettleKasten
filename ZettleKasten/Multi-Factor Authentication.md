**Tags**: #Security #Authentication #MFA #AccessControl

---

### Definition

**Multi-Factor Authentication (MFA)** is a security mechanism that requires users to provide two or more verification factors to gain access to a resource such as an application, online account, or VPN. MFA combines something you know (password), something you have (token), and something you are (biometrics).

### Authentication Factors

1. **Knowledge Factor**:
    - Something the user knows (e.g., password, PIN).
2. **Possession Factor**:
    - Something the user has (e.g., security token, smartphone).
3. **Inherence Factor**:
    - Something the user is (e.g., fingerprint, facial recognition).

### Common MFA Methods

- **One-Time Passwords (OTP)**:
    - Generated codes sent via SMS, email, or an authenticator app.
- **Hardware Tokens**:
    - Physical devices generating time-based codes.
- **Biometric Verification**:
    - Fingerprint, iris scan, or facial recognition.
- **Push Notifications**:
    - Approve login attempts via a mobile app.

### Benefits

- **Enhanced Security**:
    - Reduces the risk of unauthorized access from compromised credentials.
- **Compliance**:
    - Meets regulatory requirements for data protection.
- **User Trust**:
    - Increases confidence in the security of services.

### Implementation Considerations

- **User Experience**:
    - Balance security with convenience to minimize friction.
- **Backup Methods**:
    - Provide alternatives if a primary factor is unavailable.
- **Cost**:
    - Evaluate expenses for hardware tokens or third-party services.
- **Integration**:
    - Ensure compatibility with existing systems and applications.

### Personal Insight

**Implementing MFA is a critical step in strengthening access control**, significantly mitigating risks associated with single-factor authentication and enhancing overall security posture.

### Related Notes

- [[Secure Authentication Protocols]]
- [[Access Control Models]]
- [[Password Management]]
- [[Secure Communication]]