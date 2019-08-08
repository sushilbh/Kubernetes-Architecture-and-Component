Kubernetes Architecture and Component

What is Kubernetes?
-	Kubernetes is an open-source container-orchestration system for automating application deployment, scaling and management.
What is Node?
-	Node is worker machine in k8s. It can have multiple PODS
What are Components of Kubernetes Master Node?
-	API Server- Component on the master that exposes the Kubernetes API. It is the front-end for the Kubernetes
-	Scheduler- The Kuberentes scheduler is in charge of scheduling pods on to nodes.. when you deploy new application in Kubernetes cluster the scheduler will decide which node to start the application.
-	Controller-manager- it will check the status of the application.
-	ETCD- it is a distributed key-value store. In fact,  ETCD is the primary data store of Kubernetes; storing and replicating all Kubernetes Cluster state.

What are the component of Kubernetes Worker Node?
-	Kubelt- Will talk with API server. So when we want to acquire status and want to communicate with the worker nodes to get the status of app, network, node you talk to the kublet and kublet will talk to container runtime and it will report the status of the nodes, application and memory uses, CPU uses, network uses.
-	Kubeproxy- communicates with API server. It will do the filtering and traffic redirection using ip table by default.


What are other Components?

Workloads
1.	Pods – Group of containers that are deployed together on the same host.
2.	Deployments – set of multiple identical Pods with no unique identities.
3.	Stateful Sets - manages the deployment and scaling of a set of Pods and provides guarantees about the ordering and qniueness of these pods
4.	Secrets- it let you store and manage sensitive information such as password, OAuth Tokens, and ssh keys
5.	Config Maps- It allows you to decouple configuration artifacts from image content to keep containerized application portable.
6.	Corn Jobs – Cron jobs creates Jobs on time-based schedule. It runs a job periodically on a given schedule.
7.	Jobs - Job creates one or more pods and ensure that a specified number of them successfully terminate.
8.	Daemon sets- When nodes are removed from the cluster, pods are garbage collected. Deleting a DaemonSet will clean up the pods it created.
9.	Replica Sets – A ReplicaSet’s purpose is to maintain a stable set of replica Pods running at any given time. As such, it is often used to guarantee the availability of a specified number of identical Pods.
10.	Replication Controllers- It ensures that a specified number of pod replicas are running at any one time. In other words, it makes sure that a pod or similar set of pods is always up and running.
11.	Horizontal Pod Autoscalers – it automatically scales the number of pods in a replication controller, deployment or replica set based on observed CPU utilization. 

Networking
1.	Services – Services enables communication between various component with in and outside of application. Services helps us connect application together with other application or users.
2.	Routes
3.	Ingress – Intregess exposes HTTP and HTTPS routes from outside the cluster to services within the cluster. Traffice routing is controlled by rules defined on the ingress resource.
4.	Network Policies – This is a specification of how groups of pods are allowed to communicate with each other and other network endpoints. They are implemented by the network plugins. Networkpoly use the label to select pods and define rules with specify what traffic allowed to the selected pods.
Storage:
1.	Persistent Volumes – Persistent volumes are admin provisioned volumes and created with particular filesystem, size and volume IDS.
2.	Storage Classes- 
Builds:
1.	Build Config
2.	Builds
3.	Image Streams
Monitoring:
1.	Alerts- monitor the health of container. 
2.	Silences
3.	Metrics
4.	Dashboards
Compute:
1.	Nodes
2.	Machines
3.	Machine Sets
4.	Machine Configs
5.	Machine Config Pools
Administration:
1.	Cluster Status
2.	Cluster Setting
3.	Namespaces – are virtual  luster inside k8s cluster. They are used in environments with many users spread across multiple teams or projects.
4.	Services Accounts
5.	Roles
6.	Role Bindings
7.	Resource Quotas
8.	Limit Ranges
9.	Custom Resource Definitions



