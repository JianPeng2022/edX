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

# 07 Site Reliability Engineering (SRE)
Site Reliability Engineering (SRE) is an approach to running large-scale, reliable services. Google is widely credited with formalizing and popularizing the term "SRE" and has since been adopted by many other tech companies. SRE blends aspects of software engineering with traditional IT and focuses on creating scalable and highly reliable software systems. The primary focus of SRE is to improve the reliability of services. Reliability is often measured through service level indicators (SLIs), service level objectives (SLOs), and service level agreements (SLAs).
- Focus on Reliability: SRE places a primary emphasis on ensuring the reliability and availability of services. SREs are specifically tasked with maintaining a high level of service reliability and meeting defined Service Level Objectives (SLOs).
- Error Budgets: SRE introduces the concept of error budgets, which quantifies the allowable amount of downtime or errors within a specific timeframe. This allows for a balance between reliability and innovation, as long as the error budget is not exhausted.
- Measurable Objectives: SREs set measurable objectives, such as SLOs and Service Level Indicators (SLIs), to quantify the performance and reliability of systems. These metrics guide decision-making and help prioritize efforts.
- Blame-Free Post-Mortems: SREs adopt a blame-free culture when responding to incidents. Post-mortem analyses are conducted to understand the root causes of issues and to implement preventative measures for the future.
- Automation: Automation is a core principle of SRE. SREs leverage automation to handle routine operational tasks, enabling them to focus on strategic improvements and proactive measures.
## Measuring Reliability with SLIs
Measuring reliability is a crucial aspect of SRE; and one of the key tools used for this is Service Level Indicators (SLIs). SLIs are specific, quantitative metrics that define the performance and reliability of a service. They are typically expressed as a ratio, percentage, or a specific numerical value. SLIs represent the aspects of a service that are most critical to its users. Selecting the right SLIs is crucial. They should align with user expectations and business goals. For example, latency might be a critical SLI if users value a fast response time, the time it takes for a request to be processed.

SLIs in Action:
- Monitoring: Use monitoring tools to continuously collect data on SLIs. For example, monitor the response time of API calls to calculate latency.
- Alerting: Set up alerts based on SLIs to notify teams when performance deviates from the defined objectives. If latency exceeds the acceptable threshold, it triggers an alert for investigation.
- Analysis and Improvement: Conduct regular analysis on SLI data to identify patterns and areas for improvement. If SLIs indicate an increase in errors, it might prompt a code review or optimization efforts.
## Embracing Risks with SLOs and Error Budgets
In SRE, embracing risks is an inherent part of the approach, and it's managed through the concepts of Service Level Objectives (SLOs) and error budgets.  
**SLOs** are specific, measurable targets that define the acceptable level of reliability for a service. They are expressed as a percentage or ratio and represent the agreed-upon performance level that a service should achieve. SLOs allow teams to set realistic goals based on user expectations and business requirements. For example, an SLO for availability might be set at 99.9%, indicating that the service should be available 99.9% of the time. SLOs provide a clear metric for measuring the success of a service. If the service consistently meets or exceeds its SLOs, it is considered reliable. **Error budgets** are closely tied to SLOs and represent the allowed amount of errors or downtime within a specified timeframe. The error budget is essentially the inverse of the SLO. For example, if the SLO for availability is 99.9%, the error budget allows for 0.1% downtime.

## Service Level Agreements (SLAs)
An SLA is a formal contract between a service provider and its customers, outlining the expected level of service. It defines the agreed-upon quality of service, including performance metrics, availability, and support expectations. In Site Reliability Engineering (SRE), a Service Level Agreement (SLA) plays a crucial role in managing expectations and ensuring a service meets user needs.  

Scenario: An e-commerce company relies on a critical service called "Product Catalog" to display product information to customers. The SRE team is responsible for ensuring the reliability of this service.
- SLI (Service Level Indicator): Uptime percentage of the Product Catalog service.
- SLO (Service Level Objective): The SLO for uptime could be set at 99.95% over a month. This means the service can be unavailable for a maximum of 43.8 minutes per month (0.05% of the total time).
- SLA (Service Level Agreement): The SLA would be a formal agreement between the SRE team and the e-commerce business stakeholders. It would outline the following the agreed-upon SLO for uptime (99.95%) and the consequences of missing the SLO. For instance, the SLA might specify a service credit for the business team if the uptime falls below 99.95% in a month. This credit could be used to offset the cost of the service due to the downtime.

## The 7 Principles of SRE
Embracing Risk: SREs aim to identify the acceptable level of risk and manage it appropriately. No system is ever truly perfect. SRE acknowledges that there will be failures and focuses on minimizing their impact and ensuring fast recovery.

Service Level Objectives (SLOs): A core principle of site reliability engineering (SRE) is the move towards well-defined and well-designed service levels. SLOs define the target level of reliability for a service. They are specific, measurable goals that represent the acceptable level of performance. SLOs provide a clear understanding of user expectations and guide the team in maintaining the desired level of service reliability. In other words, it's not just about setting goals, it's about setting the right goals that effectively measure performance.

Simplicity: In SRE, simplicity reigns supreme. Complex systems are like intricate puzzles – prone to errors, challenging to troubleshoot, and demanding in terms of maintenance. Simple systems are easier to manage and adjust, less complexity means quicker fixes and smoother operations, effortless to test and monitor; clearer insights translate to faster problem identification and resolution. Less prone to errors means fewer moving parts reduce the risk of malfunctions. This focus on simplicity translates to a core SRE goal: uneventful operations.

Toil Automation: Toil refers to repetitive, manual operational work that does not contribute to the overall stability or improvement of a system. SREs aim to automate toil wherever possible, freeing up time for strategic, high-impact work. Automation reduces errors and allows teams to focus on value-added tasks.

Monitoring and Alerting: Effective monitoring and alerting are crucial for identifying and responding to issues promptly. SREs use monitoring tools to collect data on the performance and health of services. Alerts are set up to notify teams when predefined thresholds are breached, enabling quick responses to incidents.

Capacity Planning: Capacity planning involves forecasting usage patterns and ensuring that systems can handle current and future loads. SREs aim to prevent both over-provisioning and under-provisioning of resources, striking a balance to ensure optimal system performance and reliability.

Emergency Response and Blameless Postmortems: SREs are equipped to respond rapidly and effectively to incidents. The focus is on minimizing downtime and restoring service functionality. A blame-free post-mortem culture is embraced, allowing teams to learn from incidents and implement improvements to prevent future occurrences. Instead of focusing solely on fault-finding, incident reviews (often called postmortems) aim to identify the root cause of problems with a different approach. This shift in perspective is reflected in the name itself - a postmortem is less accusatory than a traditional "root cause analysis" (RCA). The goal is to learn from mistakes and improve the system, not to point fingers. Postmortems go beyond just identifying the root cause. They also ask crucial questions about how to better detect, respond to, and fix issues faster. This focus on improving response is often a challenge for organizations used to traditional blame-oriented RCAs. Building a "blameless culture" where learning is prioritized is key to getting the most out of postmortem.

Which of the following will help balance release velocity with system reliability? (Select all answers that apply)
- **SLOs**
- **Error budget**
- SLAs
