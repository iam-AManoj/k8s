# Kubernetes Architecture


![Kubernetes Architecture](https://media.dev.to/cdn-cgi/image/width=1200,height=600,fit=cover,gravity=auto,format=auto/https%3A%2F%2Fdev-to-uploads.s3.amazonaws.com%2Fuploads%2Farticles%2Fefj4eq30q56ute916yfi.png)

## Control Plane (Master Node)

- **API Server**: The core component of Kubernetes, which accepts all incoming requests and exposes Kubernetes to the external world.
- **etcd**: The key-value store that holds all the cluster-related information.
- **Scheduler**: Responsible for scheduling pods or resources on Kubernetes, receiving information from the API server, and acting on it.
- **Controller Manager**: Ensures that controllers like the Replica Set are running as expected.
- **Cloud Controller Manager**: Functions similarly to tools like Terraform, integrating with cloud provider APIs.

## Data Plane (Worker Node)

- **Kubelet**: Responsible for creating pods and ensuring they are always running.
- **Kube Proxy**: Manages networking, similar to Docker0, and provides default load balancing.
- **Container Runtime**: Runs the container inside the pod.

