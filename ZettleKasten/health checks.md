**Tags:** #DevOps #Monitoring #HealthChecks #Availability #SiteReliability

---

### Definition

**Health Checks** are automated probesâ€”such as HTTP endpoints or shell commandsâ€”that verify an application is functioning correctly and ready to serve traffic. They are essential for monitoring system health, orchestration, and load balancing.

### Types of Health Checks

- **Liveness Probes**: Verify if the application is running (should restart if failing)
- **Readiness Probes**: Check if the application is ready to accept traffic (remove from load balancer if failing)
- **Startup Probes**: Verify initial startup completion (for slow-starting applications)

### Common Implementations

- **HTTP Endpoints**: `/health`, `/healthz`, `/ready` endpoints that return status codes
- **TCP Checks**: Verify if a port is accepting connections
- **Shell Commands**: Execute scripts to verify application state
- **Database Queries**: Test connectivity and query execution

### Best Practices

- **Lightweight Checks**: Keep health checks fast and non-resource intensive
- **Comprehensive Coverage**: Verify critical dependencies (databases, external services)
- **Separate Liveness and Readiness**: Different purposes require different checks
- **Timeout Configuration**: Set appropriate timeouts to avoid false negatives
- **Meaningful Responses**: Return detailed status information when possible

### Use Cases

- **Kubernetes**: Used for pod lifecycle management
- **Load Balancers**: Remove unhealthy instances from rotation
- **Monitoring Systems**: Alert on health check failures
- **Auto-Scaling**: Trigger scaling based on health status

### Personal Insight

Health checks are fundamental to building reliable distributed systems. They enable automated recovery and ensure users are only routed to healthy instances. Properly designed health checks can prevent cascading failures and improve overall system resilience.

---

### Related Notes

- [[process health checks]]
- [[Monitoring and Logging]]
- [[Container Orchestration with Kubernetes]]
