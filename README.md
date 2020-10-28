
Deploy EKS on fargate steps: 
1.	Prerequisite : 
•	Install AWS CLI
•	Install kubectl CLI
•	Install eksctl CLI

https://github.com/stacksimplify/aws-eks-kubernetes-masterclass/tree/master/01-EKS-Create-Cluster-using-eksctl/01-01-Install-CLIs


2.	Create EKS Cluster & Node Groups: 
o	Understand about EKS Core Objects
o	Control Plane
o	Worker Nodes & Node Groups
o	Fargate Profiles
o	VPC
o	Create EKS Cluster
o	Associate EKS Cluster to IAM OIDC Provider
o	Create EKS Node Groups
o	Verify Cluster, Node Groups, EC2 Instances, IAM Policies and Node Groups

https://github.com/stacksimplify/aws-eks-kubernetes-masterclass/tree/master/01-EKS-Create-Cluster-using-eksctl/01-02-Create-EKSCluster-and-NodeGroups


3.	ALB Install Ingress Controller:

https://github.com/stacksimplify/aws-eks-kubernetes-masterclass/tree/master/08-ELB-Application-LoadBalancers/08-01-ALB-Ingress-Install


4.	EKS Fargate Profiles:
o	Assumptions:
o	We already havea EKS Cluster whose name is eksdemo1 created using eksctl
o	We already have a Managed Node Group with private networking enabled with two worker nodes
o	We are going to create a fargate profile using eksctl on our existing EKS Cluster eksdemo1
o	We are going to deploy a simple workload
o	Deployment: Nginx App 1
o	NodePort Service: Nginx App1
o	Ingress Service: Application Load Balancer
o	Ingress manifest going to have a additional annotation related to target-type: ip as these are going to be fargate workloads we are not going to have Dedicated EC2 Worker Node - Node Ports
https://github.com/stacksimplify/aws-eks-kubernetes-masterclass/tree/master/09-EKS-Workloads-on-Fargate/09-01-Fargate-Profile-Basic



