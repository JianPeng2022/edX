## State of Serverless in Kubernetes
The smallest primitive for workloads in Kubernetes is the Pod, which can be made up of one or more containers - such as the main workload and then a helper, such as a proxy or a log collector. The Pod loads the code and user-space from a container image which is stored in a container registry.

To access Pods within a cluster, various Kubernetes networking primitives come into play, such as a Service, a LoadBalancer, and Ingress. Each of these provides a slightly different way to send traffic to the running workload.

Our bare essentials for Serverless on Kubernetes are:
- A container image with function code or an executable inside.
- A registry to host the container image.
- A Pod to run the container image.
- A Service to access the Pod.
  
Often, projects will add many more components on top of this stack, such as a UI, and API gateway, Ingress automation, auto-scaling, APIs, and many more.
