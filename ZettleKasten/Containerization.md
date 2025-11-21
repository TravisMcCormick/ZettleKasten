**Tags:** #containerization #security #devops #docker #kubernetes

---

### **Definition**

**Containerization** is a lightweight virtualization method that packages applications and their dependencies into isolated, portable containers. Containers share the host operating system kernel but maintain separate user spaces, providing process isolation without the overhead of traditional virtual machines.

### **Key Layers of Container Security**

1. **Policy & Governance**
   - Implement Zero Trust principles
   - Block unsigned images
   - Deny root containers
   - Segment flat networks
   - Use default deny policies

2. **Supply Chain Integrity**
   - Generate Software Bill of Materials (SBOM) with Syft
   - Scan images with Trivy
   - Sign images with Cosign
   - Verify signatures before deployment
   - Deploy with enforced policies

3. **Image Hardening**
   - Use distroless Docker images
   - Implement multistage builds (separate build and runtime)
   - Avoid using `:latest` tags
   - Minimize attack surface

4. **Runtime Detection**
   - Behavioral detection with Falco
   - Real-time monitoring
   - Anomaly detection

5. **Network Segmentation**
   - Isolate container networks
   - Control ingress and egress traffic
   - Use service meshes like Cilium

6. **Observability**
   - Centralized logging
   - Metrics collection with Prometheus
   - Distributed tracing

### **Major Security Incidents**

- **Log4Shell (CVE-2021-44228)**: Critical vulnerability in Log4j library
- **Capital One Attack (2019)**: Misconfigured firewall in containerized environment
- **SolarWinds**: Supply chain attack
- **Codecov**: CI/CD pipeline compromise
- **3CX**: Supply chain compromise
- **Left Pad Incident**: NPM dependency crisis
- **Shai Hulud Worm**: Container escape malware

### **Security Frameworks and Standards**

- **SLSA Framework**: Supply chain security levels (0-4)
- **OPA (Open Policy Agent)**: Policy enforcement
- **Kyverno**: Kubernetes policy management

### **Best Practices**

- Never use root containers
- Always scan for vulnerabilities
- Sign and verify images
- Use minimal base images (Alpine, distroless)
- Be aware of Alpine's musl libc limitations
- Implement network policies
- Monitor runtime behavior
- Regular security audits

### **Related Notes**

- [[Docker]]
- [[Container Orchestration with Kubernetes]]
- [[DevOps Practices]]
- [[Virtualization vs. Containerization]]
- [[CI - CD pipeline]]
- [[Implement Network Segmentation]]
