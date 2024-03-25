# 06 Introduction to Observability
Observability is the ability to understand the internal state of a system based on its external outputs. This means being able to infer what is happening inside the system based on the information it produces, such as logs, metrics, and traces.
Observability is becoming increasingly important in the modern world of software development, where systems are becoming ever more complex and distributed. With traditional monitoring approaches, it can be difficult to understand what is happening inside a system and why it is behaving in a certain way. Observability provides a way to overcome this challenge by giving us a more holistic view of the system.
**Logs** are digital records of events that have occurred within a system. These records are sequential and time-stamped, offering a granular, time-stamped audit trail of activities. Logs can include a wide range of data, from the simple recording of user access to detailed error messages that software developers use to debug issues. In the context of observability, logs provide the narrative detail that complements the quantitative data from metrics and the flow of information from traces. They enable developers and operations teams to drill down to the root cause of issues, understand system behavior over time, and maintain operational excellence.
- **Application Logs** record the events happening within the application layer, such as user actions, system errors, or transactions. These logs are crucial for understanding how applications behave in real-world scenarios and for identifying application-level issues.
- **System Logs** document events at the operating system level, including system calls, scheduled tasks, and messages from the kernel. These logs help in diagnosing hardware and software issues not directly related to the application but affecting its performance.
- **Audit Logs** focus on security-related events, tracking user activities and changes to the system configurations. They are essential for compliance, security monitoring, and forensic analysis.

**Metrics** in observability are defined as numerical values that represent the characteristics of a system at a given point in time. These can range from simple measurements, like CPU utilization and memory usage, to more complex aggregations, such as request rates, error counts, or transaction durations. Unlike logs, which provide detailed, event-driven records, or traces, that map the journey of requests through a system, metrics offer a high-level, aggregated view of system behavior and performance. This quantifiable data is crucial for setting benchmarks, identifying trends, and triggering alerts when exceeding predefined thresholds.
- **System Metrics** provide insights into the health and performance of the underlying infrastructure, such as CPU load, memory consumption, disk I/O, and network bandwidth.
- **Application Metrics** are focused on the software layer and tracking application performance, including request latency, throughput, error rates, and transaction volumes.
- **Business Metrics**(like daily active users, conversion rates, and revenue metrics), though not directly related to system or application health, offer a view into the impact of system performance on business outcomes.

**Traces** are another pillar of observability, which act as the guiding light, illuminating the intricate pathways taken by user interactions within your system. They represent the journey of a single request or transaction across a distributed system, capturing the path it takes and measuring its latency across various services. By embracing their power and implementing them strategically, you gain a deeper understanding of system behavior, pinpoint issues efficiently, and optimize for a seamless user experience. Remember, the journey to true observability requires combining the quantitative power of metrics, the detailed narratives of logs, and the visual representation of traces, providing a complete picture of your system's inner workings and empowering you to build and manage truly reliable and performant software experiences.
- A trace typically consists of several key components:
- A span represents a single operation or component interaction within a trace, often including start and end times, thus allowing for latency measurement.
- A trace context carries the trace's identity across process, network, and service boundaries, ensuring that all spans belonging to a single trace are correctly associated.
Annotations and metadata are additional information attached to spans, such as user IDs, error messages, or other contextual data, enriching the trace with details that aid in analysis and debugging.

Tracing can be categorized into several types, each serving different monitoring and diagnostic needs:
- Distributed Tracing tracks the journey of requests through microservices or distributed architectures, highlighting the interactions and latency between services.
- Real User Monitoring (RUM) captures traces of actual user interactions with a system, providing insights into user experience and performance issues.
- Synthetic Monitoring uses simulated requests to monitor system performance and availability in a controlled manner, complementing real user data with consistent, baseline measurements.

Monitoring and Metrics:
-Prometheus: An open-source monitoring and alerting toolkit designed for reliability and scalability. It collects metrics from configured targets, stores them, and makes them available for querying.
-Grafana: A popular open-source platform for visualizing and analyzing metrics. Grafana integrates with various data sources, including Prometheus, InfluxDB, and Elasticsearch.
-InfluxDB: A high-performance, distributed, and scalable time-series database. It is commonly used for storing and querying metrics data.
-Datadog: A cloud-based observability platform that integrates monitoring, logging, and APM (Application Performance Monitoring) capabilities. It supports a wide range of integrations.

Logging:
- ELK Stack (Elasticsearch, Logstash, Kibana): Elasticsearch is a distributed search and analytics engine, Logstash is a log pipeline tool, and Kibana is a visualization platform. Together, they form a powerful stack for log management.
- Splunk: A widely used platform for searching, monitoring, and analyzing machine-generated data, including logs. It provides powerful search and visualization features.
  
Tracing:
- Jaeger: An open-source, end-to-end distributed tracing system. It helps in monitoring and troubleshooting the latency of requests in complex, microservices-based architectures.
- Zipkin: Another open-source distributed tracing system. Zipkin allows users to trace requests as they travel through various services in a distributed system.
  
Application Performance Monitoring (APM):
- New Relic: A cloud-based APM tool that provides detailed insights into application performance. It offers features like transaction tracing, error tracking, and infrastructure monitoring.
- AppDynamics: A comprehensive APM solution that provides real-time monitoring of applications, user experience, and infrastructure. It helps in identifying performance bottlenecks.
  
Infrastructure Monitoring:
- Nagios: A widely used open-source infrastructure monitoring solution. Nagios can monitor hosts, services, and network devices, providing alerts in case of issues.
- Zabbix: An open-source monitoring solution that offers features for monitoring servers, networks, applications, and services. It supports a range of data visualization options.
Cloud Native Observability:
- AWS CloudWatch: Amazon's monitoring and observability service for AWS resources. It provides metrics, logs, and traces for AWS services and applications.
- Azure Monitor: Microsoft Azure's observability service, offering insights into the performance and health of applications and infrastructure on the Azure platform.
