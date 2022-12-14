# kubernetes
Logical Introduction to Kubernetes 

# Offical Definition
is open soruce container orchestration toll developed by Google. it helps you manage cotnainerized applications and helping you managing containers in different deployment environments for exmaple physical, cloud, virtual or even hyper dyploemnt enviroments. 
- what problems does kubernetes solve ? 
- what are the tasks of an orchestration tool ? 
chronologically the rise of micro services cause increased usage of container technologies because the containers actually offer the perfect host for small independent applications like Microsoft a nurse and the micro service technology actually resulted in applications that they're now comprised of hundreds or sometime maybe even thousands of containers now managing those loads of containers across multiple environments using scripts and self-made tools can be really complex and sometimes even impossible so that specific scenario actually caused the need for having container orchestration technologies so.
# Problem-solution case study 
- what features do orchestration tools offer ? 
  1. high availability  or no downtime
  2. Scalability or high performance 
  3. Disaster recovery - backup and restore 

# Basic architecture 
the Kubernetes cluster is made up with at least one master node and connected to it you have a couple workers node and each worker node had kubelete process running on it  and kubelete is kubernetes process that make the workers talk to each other each worker could have more than docker containers running on them. and here is were your applications running, 
 - Master-Slave 
 - K8S processes 
   is the responsible on managing the cluster properly on of such processess is the following: 
  1. API server: is actually an Entrypoint to K8S cluster for exmaples 
  UI , API , CLI 
  2. Controller manager: keep overview the what happening in the cluster 
  3. Scheduler: ensure Pods placement and controll the load of the whole cluster
  4. etcd: holding the current K8S configuration 
  5. Virtual Network: turns all the nodes inside the cluster into one powerfull machine and the Master Node will controll everything.  

# Basic concepts
Pod & Containers 
POD: is the smallest unit that you k8s user will confiure and interact with it , and pod is wrapper of a containner each worker node i ill have mulitple POD. 
Note: each pod is connected to a Virtual Network that means each POD could have internal unqiue IP address and the way that could commnect to each other they use interal IP address. 

# Example Configuration 
all the configuration go to Master Node and all the services talk to the API server just like Windows API , and most of the configuration is written in JSON or YMAL formt "Declarative fromat" 


# minikube  [minikube Startup](https://minikube.sigs.k8s.io/docs/start/)
minikube is local Kubernetes, focusing on making it easy to learn and develop for Kubernetes.

All you need is Docker (or similarly compatible) container or a Virtual Machine environment, and Kubernetes is a single command away: minikube start 


