![Kubernetes Logo](https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcR99vkXlOXicRs8PtMeSG4KiyWpULvHdG2QUA&s)

# Kubernetes
*[↑ Previous Article](./3-1-docker.md)*

Kubernetes, often abbreviated as K8s, is an open-source container orchestration platform designed to automate the deployment, scaling, and management of containerized applications. Originally developed by Google, Kubernetes has become the de facto standard for managing containerized workloads and services.

## How Kubernetes Works

Kubernetes works by organizing containers into groups called Pods, which are the smallest deployable units in Kubernetes. A Pod can contain one or more containers that share the same network namespace and storage, allowing them to communicate easily. Kubernetes abstracts the underlying infrastructure, enabling users to deploy applications seamlessly across a cluster of machines.

### Key Components of Kubernetes

![Kubernetes Nodes Pods](https://miro.medium.com/v2/resize:fit:1400/1*Ov0hT6_59NzMS7o2Ea-P-Q.png)

#### Pods

A Pod is the basic unit of deployment in Kubernetes. It can host one or multiple tightly coupled containers that share resources such as networking and storage. 

- **Lifecycle of a Pod**:
  - **Pending**: The Pod has been accepted but is not yet running.
  - **Running**: The Pod is actively running on a node.
  - **Succeeded**: All containers in the Pod have completed successfully.
  - **Failed**: All containers in the Pod have terminated, and at least one container has failed.

- **Learn More**: [Kubernetes Pods](https://kubernetes.io/docs/concepts/workloads/pods/)

#### Nodes

A Node is a physical or virtual machine that runs containerized applications. Each Node in a Kubernetes cluster has the services necessary to run Pods and is managed by the control plane.

- **Types of Nodes**:
  - **Master Node**: Manages the Kubernetes cluster and makes decisions about the cluster (scheduling, scaling, etc.).
  - **Worker Node**: Runs the application workloads in the Pods.

- **Learn More**: [Kubernetes Nodes](https://kubernetes.io/docs/concepts/architecture/nodes/)

#### Deployments

A Deployment provides declarative updates for Pods and ReplicaSets. It allows users to define the desired state of an application, and Kubernetes will automatically manage the deployment process to achieve that state.

- **Key Features**:
  - **Rolling Updates**: Gradually replaces Pods with new versions without downtime.
  - **Rollback**: Easily revert to a previous version of the application if needed.

- **Learn More**: [Kubernetes Deployments](https://kubernetes.io/docs/concepts/workloads/controllers/deployment/)

#### Services

Kubernetes Services provide stable endpoints for accessing Pods, enabling reliable communication between different parts of an application. A Service can expose a single Pod, a set of Pods, or all Pods in a Deployment.

- **Types of Services**:
  - **ClusterIP**: Exposes the Service on a cluster-internal IP.
  - **NodePort**: Exposes the Service on each Node’s IP at a static port.
  - **LoadBalancer**: Exposes the Service externally using a cloud provider’s load balancer.

- **Learn More**: [Kubernetes Services](https://kubernetes.io/docs/concepts/services-networking/service/)

#### ConfigMaps and Secrets

Kubernetes ConfigMaps and Secrets provide a way to manage configuration data and sensitive information separately from application code.

- **ConfigMaps**: Used to store non-sensitive configuration data as key-value pairs.
- **Secrets**: Specifically designed to hold sensitive information, such as passwords, tokens, and SSH keys.

- **Learn More**: 
  - [Kubernetes ConfigMaps](https://kubernetes.io/docs/concepts/configuration/configmap/)
  - [Kubernetes Secrets](https://kubernetes.io/docs/concepts/configuration/secret/)

### Kubernetes Architecture

![Kubernetes Architecture Diagram](https://www.cncf.io/wp-content/uploads/2020/09/Kubernetes-architecture-diagram-1-1-1024x698.png)

Kubernetes follows a master-slave architecture. The control plane, which consists of various components, manages the worker nodes and their Pods.

- **Control Plane Components**:
  - **API Server**: The front-end for the Kubernetes control plane.
  - **etcd**: A distributed key-value store used for storing cluster state data.
  - **Controller Manager**: Ensures the desired state of the cluster is maintained.
  - **Scheduler**: Assigns Pods to Nodes based on resource availability.

- **Learn More**: [Kubernetes Architecture](https://kubernetes.io/docs/concepts/overview/architecture/)

### Summary

Kubernetes provides powerful capabilities for managing containerized applications in production. With components like Pods, Nodes, Deployments, and Services, Kubernetes abstracts the complexities of container orchestration, enabling developers to focus on building applications rather than managing infrastructure. Its robust architecture and extensibility make it an essential tool in the modern DevOps landscape.

Kubernetes has become the standard for container orchestration, supporting a wide range of workloads and enabling organizations to achieve high availability and scalability.

## Learn More

- **Kubernetes Documentation**: [Kubernetes Docs](https://kubernetes.io/docs/home/)
- **Kubernetes GitHub**: [Kubernetes GitHub Repository](https://github.com/kubernetes/kubernetes)
