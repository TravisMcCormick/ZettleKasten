**Tags:** #LoadBalancing #Scalability #DevOps #HighAvailability #Architecture

---

### Definition

**Load Balancing** is the process of distributing incoming requests across several service instances to optimize resource use, maximize throughput, minimize response time, and avoid overload on any single resource.

### Key Concepts

- **Distribution Algorithm**: Methods like round-robin, least connections, IP hash, or weighted distribution
- **Health Checks**: Monitoring backend servers to ensure traffic only goes to healthy instances
- **Session Persistence**: Maintaining user sessions with the same backend server when needed
- **SSL Termination**: Offloading SSL/TLS encryption/decryption from backend servers

### Types of Load Balancers

- **Layer 4 (Transport)**: Operates at TCP/UDP level, routing based on IP and port
- **Layer 7 (Application)**: Operates at HTTP level, can route based on URL, headers, cookies
- **Hardware**: Dedicated physical appliances (F5, Citrix NetScaler)
- **Software**: Nginx, HAProxy, Traefik
- **Cloud**: AWS ELB/ALB, Azure Load Balancer, Google Cloud Load Balancing

### Benefits

- **Scalability**: Handle more traffic by adding instances
- **High Availability**: Continue operating even if some instances fail
- **Performance**: Distribute load to prevent any single server from becoming a bottleneck
- **Maintenance**: Enable zero-downtime deployments

### Personal Insight

Load balancing is fundamental to building scalable, reliable systems. Understanding the difference between Layer 4 and Layer 7 load balancing, and when to use each, is crucial for architecting modern applications. Proper health checks are just as important as the distribution algorithm itself.

---

### Related Notes

- [[Microservices Architecture]]
- [[health checks]]
- [[Gateway]]