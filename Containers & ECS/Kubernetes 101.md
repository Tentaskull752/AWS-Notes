
#### Personal Summary 

  - A cluster is a highly available collection of resources and services, which are then organized to work as one unit. There are two distinct parts, the Control Plane and the Node. 
  - Cluster Node: a Virtual Machine or Physical server which functions as a worker in the cluster
  - The Control Plane manages the cluster, scheduling, application, scaling, and deploying. 
  - Kubelet: an agent within the node to interact with the control plane. 
  - Kubernetes API: used for communication between control plane and kublet agent. 
  - Containerd or Docker is software for handling container operations and container runtime.
  - PODS - DONT THINK ABOUT CONTAINERS, THINK ABOUT PODS. These are the smallest units of computing in kubernetes. SHARED STORAGE AND NETWORKING. ONE CONTAINER TO ONE POD IS VERY COMMON. Pods are NON-PERMANENT. 
  - kube-apiserver: front end for kubernetes control plane and is what nodes and other cluster elements interact with. Can be scaled horizontally.
  - kube-scheduler: can determine pods that are not assigned to nodes, and then assigned a node to those pods.
  - etcd: provides high-availability key value store used within the cluster. Main backing store for the cluster.
- Kube-proxy: network proxy on each node that coordinated networking with the control plane. Helps implement services and configure rules allowing communication with pods in and out of the cluster.