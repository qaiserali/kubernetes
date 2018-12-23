## Kubernetes commands

List of kubectl commands for managing kubernetes cluster

- [Pods](#pods)
- [Services](#services)
- [Deployments](#Deployments)
- [Nodes](#nodes)
- [Troubleshootings](#troubleshootings)

### Pods
Kubectl commands related to pods  

``$ kubectl get pods``                      Returns list all pods  
``$ kubectl -n {namespace} get pods``      List of all pods in given namespace   
``$ kubectl get pods -o wide``             List of pods with wider output (more columns)  
``$ kubectl get pods --all-namespaces ``  List of all pods in all namespaces  
``$ kubectl describe pod {pod-name}``      Describe pod with verbose output  
``$ watch kubectl pods``                   Pods status during execution  
  
### Deployments

Useful deployments commands

``$ kubectl get deployments``                                 Returns deployments list  
``$ kubectl -n {namespace} get deployments``                  Deployments list within a namespace  
``$ kubectl scale deployment {deployment-name} --replicas=5`` Scale deployment and set pods replicas to 5  
``$ kubectl delete deployment {deployment-name}``             Delete a deployment 
  
  
  
### Nodes
 
 Commands list related to kubernetes nodes  
 
``$ kubectl get nodes``                                      Returns list of all nodes  
``$ kubectl get node {node-name} --show-labels``             Show all labels for given node  
``$ kubectl describe node {node-name}``                      Describe node with verbose output   
``$ kubectl label node {node-name}  key=values``              Assign label to a node  
``$ kubectl label node {node-name} key=values --overwrite``   Overwrite a node label  
