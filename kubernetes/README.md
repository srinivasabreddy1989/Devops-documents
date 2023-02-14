Kubernetes is an open source container orchestration engine for automating deployment, scaling, and management of containerized applications.

Latest version
    v1.26 ---> https://kubernetes.io/docs/home/supported-doc-versions/

Different ways to setup kubernetes:
    choose an installation type based on: ease of maintenance, security, control, available resources

clusters: A cluster is a set of nodes (physical or virtual machines) running Kubernetes agents, managed by the control plane
    110 pods per node
    5,000 nodes

Control plane components:
    etcd storage: 

For best practice:
    consider for large clusters
    Running in multiple zones
    validate node setup
    enforce pod security standards

Kubernetes Components:
    1. Worker nodes:
    2. control plane:

Control plane:
    1. Kube-apiserver
    2. etcd: highly-available key value store
    3. kube-scheduler: 
    4. kube-control manager: 
worker node:
    kubelet: An agent that runs on each node in the cluster
    kube-proxy: kube-proxy is a network proxy that runs on each node in your cluster
Container runtime:
Addons: 
DNS: 
webUI:
container resource monitoring: 
cluster level logging:

The Kubernetes API: The API server exposes an HTTP API that lets end users, different parts of your cluster

Imperative commands: use to create kubernetes objects using commands
imperative object configuration: using yml and json files
Declarative object configuration: 