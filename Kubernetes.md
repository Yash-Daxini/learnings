### Server 
- Physical machine which is on 24/7. It has public internet access and static IP address. Using public internet and static IP external user can access the server.

### Server Deployment Models

#### Traditional deployement
- Multiple applications run on a single physical server, sharing resources such as CPU, memory, and storage. This approach can lead to resource contention, where one application may consume more resources than others, affecting performance and stability. Solution for the problems is to use separate physical servers for each application but this increases the cost. 

#### Virtulization
- The server is running a hypervisor that allows for the creation and management of virtual machines (VMs). Each VM can run its own operating system and applications, providing isolation and resource allocation. Single physical server contains multiple VMs and each run its own app. But virtulization images are very heavy because it contains whole operating system.

#### Containerization
- Containers are light weight VMs. It is kind of virtuliztion but it not contains OS layer. Containerization uses host system's kernel. The server supports containerization technologies, allowing applications to be packaged into containers. This enables lightweight deployment, scaling, and management of applications across different environments.

### Why container orchestration required?
- Management of containers are not easy. Container maintainance means updating the container image, redeploying the container, and ensuring that the application runs smoothly. This can be complex, especially in large-scale environments with many containers.

### Container Orchestration 
- To simplify the management of containers, container orchestration tools are used. These tools automate the deployment, scaling, and operation of application containers across clusters of hosts. They help manage the lifecycle of containers, ensuring that applications are running as expected and can scale based on demand.

- Container orchestration tools provide framework for managing containers and microservices architecture at scale, making it easier to deploy the same application across different environments without redesigning it.

- Google's Borg system is a cluster manager that runs hundreds of thousands of jobs, from many thousands of different applications, across a number of clusters each with up to tens of thousands of machines.

### Kubernates
- It is developed by Google and it's donated to CNCF (Cloud Native Computing Foundation). Kubernetes is an open-source container orchestration platform that automates the deployment, scaling, and management of containerized applications. It provides a robust framework for running applications in a distributed environment, ensuring high availability and scalability.

- It's also know as K8s.

- AWS ECS - Elastic container service. It is also maintains the containers but it becomes platform dependent. It is possilble that other cloud services might not provide this functionality.

Kubernetes is a cloud agnostic.

### Kubernetes cluster
- It is a set of node machines that run containerized applications.

#### Architecture of Kubernetes

Terms use in kubernetes'c cluster architecture: 

**1. Control Plane**

   1. kube-Scheduler: Looks for a Pods not yet bound to a Node and assigns each pod to suitable node.
   2. kube-Controller-manager: Runs controller to implement kubernetes API behavior.
   3. etcd - KV store: Consistent and highly available key-value store used for storing all cluster data, including configuration and state information. It is the backbone of Kubernetes, ensuring that the desired state of the cluster is maintained.
   4. Kube-API server: The core component server that exposes the Kubernetes API and serves as the main entry point for managing the cluster. It handles requests from users, CLI tools, and other components.
    5. CCM (Cloud control manager): Manages cloud-specific control logic, such as managing load balancers and storage volumes in a cloud environment. Integrates with underlying cloud providers.

2. Worker Node
3. Kubelet: It ensures that PODS are runnig on the worker node. It communicates with the kube-API server to receive instructions and report the status of the pods running on the node.
4. Kube proxy: It is a network proxy that runs on each worker node. It maintains network rules for pod communication and load balancing, ensuring that traffic is properly routed to the appropriate pods based on their labels and selectors.
5. CRI (Container runtime interface): It is responsible for running containers.
   - Containerd: A container runtime that provides the basic functionalities required to run containers.
   - Docker: A popular container runtime that allows for building, running, and managing containers.
   - CRI-O: An alternative container runtime designed specifically for Kubernetes.

6. PODS: Pods represents a set of running containers in your cluster. A pod can contain one or more containers that share the same network namespace and storage volumes. Pods are the smallest deployable units in Kubernetes and are used to run applications.

7. CCM (Cloud control manager)

8. Node: Node is a worker machine in Kubernetes, which can be a physical or virtual machine. Each node runs the necessary services to manage pods and provide the runtime environment for containers. Nodes are managed by the control plane and can be dynamically added or removed from the cluster.
