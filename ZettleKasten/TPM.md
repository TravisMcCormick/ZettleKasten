**Tags:** #hardware #security #cryptography #trusted-computing

---

### **Definition**

**TPM (Trusted Platform Module)** is a specialized hardware chip on a computer's motherboard that provides hardware-based security functions. It serves as a secure cryptoprocessor designed to carry out cryptographic operations and store sensitive data like encryption keys, passwords, and digital certificates in a tamper-resistant manner.

### **Core Functions**

- **Secure Key Generation**: Creates cryptographic keys in hardware
- **Secure Key Storage**: Stores keys that never leave the TPM
- **Platform Integrity**: Measures and verifies system boot state
- **Random Number Generation**: Provides hardware-based random numbers
- **Sealed Storage**: Encrypts data tied to specific platform configuration
- **Attestation**: Proves the state of the system to remote parties
- **Digital Signing**: Signs data using keys stored in TPM

### **Key Components**

1. **Cryptographic Processor**: Performs encryption/decryption operations
2. **Persistent Memory**: Stores keys and owner authorization data
3. **Volatile Memory**: Temporary storage for Platform Configuration Registers (PCRs)
4. **I/O Interface**: Communication with main processor (LPC, SPI, or I2C bus)
5. **Random Number Generator (RNG)**: Hardware entropy source

### **TPM Versions**

- **TPM 1.2**: Legacy standard, still widely used
- **TPM 2.0**: Current standard with enhanced algorithms and flexibility
  - Supports more cryptographic algorithms
  - Better key hierarchy
  - Improved authorization mechanisms
  - Crypto-agility (algorithm flexibility)

### **Types of TPM**

- **Discrete TPM (dTPM)**: Separate dedicated chip on motherboard
- **Integrated TPM (iTPM)**: Integrated into chipset
- **Firmware TPM (fTPM)**: Software running in trusted execution environment
- **Virtual TPM (vTPM)**: Software emulation for virtual machines

### **Platform Configuration Registers (PCRs)**

- 24 PCR slots (TPM 2.0) storing measurements
- Extended during boot process (cannot be directly written)
- Store hashes of firmware, bootloader, OS components
- Used for measured boot and attestation

### **Use Cases**

- **BitLocker Drive Encryption**: Windows full-disk encryption
- **Secure Boot**: Ensures only trusted software loads during boot
- **Device Authentication**: Proves device identity
- **Credential Protection**: Stores certificates and keys
- **Digital Rights Management (DRM)**: Content protection
- **Remote Attestation**: Proves system state to remote services
- **VPN Authentication**: Hardware-backed credentials
- **Passwordless Authentication**: FIDO2/WebAuthn support

### **Measured Boot Process**

1. **BIOS/UEFI**: Measured and extends PCR
2. **Boot loader**: Measured before execution
3. **OS Kernel**: Measured during load
4. **Drivers and Components**: Measured as loaded
5. **Attestation**: Remote parties can verify measurements

### **Security Benefits**

- **Hardware Root of Trust**: Security anchored in dedicated hardware
- **Tamper-Resistance**: Physical security of keys
- **Anti-Replay**: Prevents replay of old system states
- **Protection Against Firmware Attacks**: Detects boot-time compromises
- **Key Isolation**: Keys never exposed to OS or applications
- **Brute-Force Protection**: Dictionary attack lockout

### **Limitations**

- **Not a Silver Bullet**: Protects keys, doesn't prevent all attacks
- **Evil Maid Attacks**: Physical access can compromise unsealed data
- **OS-Level Compromise**: TPM can't protect running system
- **Complexity**: Proper implementation is challenging
- **Attestation Privacy**: Can reveal information about system
- **Performance**: Some operations slower than software

### **Windows Requirements**

- **Windows 11**: Requires TPM 2.0 for installation
- **BitLocker**: Recommended (but not required) for full functionality
- **Device Encryption**: Requires TPM 2.0
- **Windows Hello**: Can use TPM for biometric data protection

### **Linux Support**

- **tpm2-tools**: Command-line utilities for TPM 2.0
- **tpm2-tss**: TPM 2.0 Software Stack
- **LUKS**: Full-disk encryption with TPM support
- **systemd-cryptsetup**: TPM-based unlock
- **IMA/EVM**: Integrity Measurement Architecture

### **Best Practices**

- Enable TPM in BIOS/UEFI if discrete TPM present
- Take ownership and set strong passwords
- Regular firmware updates
- Backup recovery keys for encryption
- Use TPM for most sensitive operations
- Implement measured boot for critical systems
- Combine TPM with other security measures
- Clear TPM when transferring ownership of device

### **Common Commands (Windows)**

```powershell
# Check TPM status
Get-Tpm

# Clear TPM (reset)
Clear-Tpm

# Initialize TPM
Initialize-Tpm
```

### **Common Tools (Linux)**

```bash
# Check TPM version
cat /sys/class/tpm/tpm0/tpm_version_major

# Read PCR values
tpm2_pcrread

# Generate random bytes
tpm2_getrandom
```

### **Related Notes**

- [[Hardware Security]]
- [[Data Encryption Techniques]]
- [[Cryptographic Key Management]]
- [[Cryptographic Algorithms]]
- [[Digital Certificates]]
- [[Authentication Mechanisms]]
- [[Computer Hardware Components]]
- [[Encrypt Sensitive Data]]
- [[Physical Security Measures]]

