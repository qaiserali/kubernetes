## Kubernetes commands

List of kubectl commands for managing kubernetes cluster

- [Pods](#pods)
- [Services](#services)
- [Nodes](#nodes)
- [Troubleshootings](#troubleshootings)

### Pods
Kubectl commands related to pods  

``$ kubectl get pods``   Returns list all pods
`` $ kubectl -n {namespace} get pods``  Returns list of all pods in given namespace
 `` $ kubectl get pods --all-namespaces ``  Returns list of all pods in all namespaces
  
### Nodes
 
 Commands list related to kubernetes nodes  
 
 ``$ kubectl get nodes``  Returns list of all nodes
 ``$ kubectl node {node-name} --show-labels``  Show all labels for given node
 ``$ kubectl describe node {node-name}``  Describe node with verbose output