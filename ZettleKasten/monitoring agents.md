**Tags:** #Monitoring #DevOps #Observability #Agents #Infrastructure

---

### Definition

**Monitoring Agents** are daemons installed on hosts to collect metrics, logs, and emit alerts for anomalous conditions. They provide visibility into system and application performance by continuously gathering and reporting telemetry data.

### Common Agents

- **Node Exporter**: Prometheus agent for hardware and OS metrics
- **Telegraf**: InfluxDB agent supporting multiple input/output plugins
- **Datadog Agent**: Proprietary agent for Datadog platform
- **New Relic Agent**: Application performance monitoring
- **Elastic Beats**: Lightweight data shippers (Filebeat, Metricbeat, etc.)

### Functions

- **Metrics Collection**: CPU, memory, disk, network statistics
- **Log Shipping**: Forward application and system logs to central repositories
- **Health Checks**: Perform local checks and report status
- **Event Detection**: Identify anomalies and trigger alerts
- **Tag Enrichment**: Add metadata to collected data

### Deployment Considerations

- **Resource Overhead**: Agents consume CPU and memory
- **Network Impact**: Data transmission bandwidth
- **Security**: Agents need appropriate permissions
- **Update Management**: Keeping agents up-to-date across fleet
- **Configuration Management**: Consistent configuration across instances

### Personal Insight

Monitoring agents are the eyes and ears of your infrastructure. While they add overhead, the visibility they provide is essential for maintaining reliable systems. Choose lightweight agents and configure them judiciously to balance coverage with resource impact.

---

### Related Notes

- [[Monitoring and Logging]]
- [[health checks]]
- [[Integrated log management]]
- [[DevOps Practices]]