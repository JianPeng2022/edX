# 03 Introduction to Containers and Kubernetes
Imagine a container as a standardized box that holds everything your application needs to run - its code, libraries, runtime environment, and system configuration. Unlike virtual machines, which virtualize the entire hardware stack, containers share the underlying operating system (OS) with other containers, making them much more lightweight and efficient.
## The Difference Between Containers and Virtual Machines
Virtual machines provide a fully isolated virtual environment, complete with an operating system and all necessary dependencies. Each VM runs on a hypervisor, a layer that abstracts the physical hardware and allows multiple VMs to coexist on a single physical machine. Here are some key characteristics of virtual machines:
- **Strong isolation**: Each VM operates as an independent entity, with its own dedicated resources and a separate OS instance. This isolation makes VMs highly secure, as vulnerabilities within one VM do not impact others.
- **Compatibility**: Virtual machines can run different operating systems within the same hardware. This makes VMs versatile and allows for running legacy applications or different operating system versions in parallel.
- **Complete abstraction**: VMs completely abstract the underlying hardware, providing hardware-level virtualization. This means VMs operate as if they are running on dedicated physical machines, giving them full control over the virtual environment.
- **Resource overhead**: VMs consume more resources compared to containers due to the need for a separate OS instance for each VM. This can result in higher infrastructure costs and slower startup times compared to containers.

Containers provide a way to package and run applications with their dependencies, isolated from the underlying host system. The core idea behind containers is to offer a lightweight and highly efficient alternative to traditional VMs. Here are some key characteristics of containers:
- **Resource efficiency**: Containers share the host system's operating system (OS) kernel, eliminating the need for multiple OS instances. This reduces the overhead and frees up resources, making containers significantly more resource-efficient compared to VMs.
- **Rapid startup and scalability**: Containers can start and stop almost instantaneously, often in seconds. This rapid startup time makes them highly scalable and allows for horizontal scaling, meaning you can easily spin up multiple instances of an application to handle an increased workload.
- **Isolation and security**: Containers are isolated from one another and from the host system, providing strong isolation of resources. However, since they share the OS kernel, a vulnerability in the kernel can potentially affect all containers running on the host.
- **Ease of management**: Containers are easier to manage due to their lightweight nature. They can be deployed, updated, and rolled back effortlessly, making them ideal for applications that require frequent updates and continuous integration/continuous deployment (CI/CD) workflows.
## Docker: What’s under the hood?
**Docker Engine**, often simply referred to as Docker, is the heart of Docker technology, providing the necessary functionality to create and manage container lifecycle. Its architecture allows for seamless development, shipment, and running of applications in containers. Docker Engine is modular in nature and consists of many modules that help in container lifecycle management.
- Docker uses **containerd** as its container runtime. Containerd is an industry-standard core container runtime that provides the basic functionality for container execution and management. It handles low-level container operations, such as container creation, execution, and deletion.
- At the core of containerd is **runC**, which is the industry-standard container runtime. runC is responsible for spawning and running containers based on OCI (Open Container Initiative) specifications. It handles the container lifecycle, including creating and running containers from container images.
- Docker initially used **libcontainer** as its container execution library. However, with the development of containerd, libcontainer's functionality was incorporated into container.

**Docker Client**: Docker client is a command-line tool that allows users to interact with the Docker daemon (Docker Engine). Users issue commands to the Docker client, which then communicates with the Docker daemon to perform actions like building, running, and managing containers.  

**Docker images** are lightweight, standalone, and executable packages that include the application and all its dependencies. Images are built from a set of instructions defined in a Dockerfile. They are stored in a registry, such as Docker Hub or a private registry, and can be easily shared and distributed.

**Docker Registry**: Docker images are stored in registries, which are repositories for sharing and distributing container images. Docker Hub is the default public registry; users can also set up private registries for internal use. Images can be pulled from registries when needed for running containers.

**Docker Compose** is a tool for defining and running multi-container Docker applications. It allows users to describe the services, networks, and volumes in a *docker-compose.yml* file, making it easy to define complex applications with multiple components.

**Docker Swarm** is Docker's native clustering and orchestration solution. It allows users to create and manage a swarm of Docker nodes, turning them into a single virtual Docker host. Swarm enables the deployment and scaling of services across multiple containers.

**Networking and Storage Drivers** Docker provides various networking and storage drivers that allow containers to communicate with each other and with external networks. Networking and storage drivers can be configured based on the specific requirements of the application.  

Overall, **Podman**'s architecture offers a secure and user-friendly alternative to managing containers, especially in environments where security is paramount. Its daemonless and rootless features, along with compatibility with Docker, make it a popular choice in the containerization ecosystem.

## The Need for Container Orchestration (Kubernetes, Docker Swarm, Apache Mesos, Nomad)
**Automating container management**: Manually managing a large number of containers is error-prone and time-consuming. Container orchestration platforms automate many tasks, including:
- Deployment: Orchestrators can automatically deploy containers to different nodes in a cluster, ensuring that applications are available and running smoothly.
- Scaling: Orchestrators can automatically scale containerized applications up or down based on demand, ensuring optimal resource utilization.
- Health monitoring: Orchestrators can monitor the health of containers and automatically restart them if they fail, ensuring application uptime.
- Networking: Orchestrators can configure and manage networks for containerized applications, ensuring that they can communicate with each other and external resources.

**Streamlining complex workflows**: Container orchestration platforms can help to simplify and streamline complex workflows, such as continuous integration and continuous delivery (CI/CD) pipelines. These platforms can automate the build, test, and deployment of containerized applications, allowing developers to focus on writing code and delivering value.

**Improving resource utilization**: Container orchestration platforms can help improve resource utilization by ensuring that containers are only running when needed. This can lead to significant cost savings, especially in cloud environments where resources are billed per hour. 

**Enforcing consistency and control**: Container orchestration platforms can help to enforce consistency and control over containerized applications. This is important for ensuring that applications are deployed in a consistent manner and that they meet security and compliance requirements.

**Enabling multi-cloud deployments**: Container orchestration platforms can enable multi-cloud deployments, where applications are deployed across multiple cloud providers. This can provide greater flexibility and resilience, as well as reduce reliance on any single vendor.
