Explanation for Deployment Choices in Kubernetes
Choice of Kubernetes Objects:
1. Deployment for Backend
I chose to use a Deployment object for the backend service.
2. Service for Backend and Client:
 I used Service objects for both the backend and client applications.The backend service is of type ClusterIP, making it accessible only within the cluster, while the client service is also of type ClusterIP, allowing internal communication.

Method Used to Expose Pods:
I exposed the backend service internally within the cluster using a ClusterIP service. This means the service is only accessible within the Kubernetes cluster and not from the internet. 

Use of Persistent Storage:
I utilized a PersistentVolumeClaim (PVC) to provide persistent storage for the backend service. The PVC named "server-pvc" requests 1Gi of storage with ReadWriteOnce access mode

Git Workflow:
I followed a typical Git workflow for this task. I created separate YAML files for each Kubernetes object (Deployment and Service) to maintain a modular and organized structure. These files were committed to my Git repository. I regularly commited and wrote descreptive commit messages.