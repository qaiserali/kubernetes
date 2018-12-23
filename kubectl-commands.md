## Kubernetes commands

List of kubectl commands for managing kubernetes cluster

- [Pods](#pods)
- [Services](#services)
- [Deployments](#deployments)
- [Nodes](#nodes)
- [Taints and Tolerations](#taints-and-tolerations)
- [Namespaces](#namespaces)
- [ResourceQuotas](#resource-quotas)
- [Troubleshootings](#troubleshootings)

### Pods

``$ kubectl get pods``                      Returns list all pods  
``$ kubectl -n {namespace} get pods``       List of all pods in given namespace   
``$ kubectl get pods -o wide``              List of pods with wider output (more columns)  
``$ kubectl get pods --all-namespaces ``    List of all pods in all namespaces  
``$ kubectl describe pod {pod-name}``       Describe pod with verbose output  
``$ watch kubectl pods``                    Pods status during execution  
``$ kubectl delete pod {pod-name}``         Delete a pod  
``$ kubectl get rs``		 	    Get replicas set 
  
### Deployments

``$ kubectl get deployments``                                 Returns deployments list  
``$ kubectl get deploy`` 			              Deployment list. deploy shortcut can be used instead of deployment  
``$ kubectl -n {namespace} get deployments``                  Deployments list within a namespace  
``$ kubectl scale deployment {deployment-name} --replicas=5`` Scale deployment and set pods replicas to 5  
``$ kubectl delete deployment {deployment-name}``             Delete a deployment  
``$ kubectl delete -f .``                                     Delete all deployments 
  

### Taints and Tolerations

``$ kubectl taint nodes {node-name} key=value:NoSchedule``    No pod will be schedule on a given node, unless it has a matching toleration  
``$ kubectl taint nodes {node-name} key=value:NoExecute``     Any pod that don't tolerate the given taint will be evicated immediately   
``$ kubectl taint nodes {node-name} key:NoSchedule-``         Delete taint with type NoSchedule and key=key. The minus(-) sign in the end is used to delete a taint   
``$ kubectl taint nodes {node-name} key2:NoExecute-``         Delete taint with type NoExecute and key=key2  

### Namespaces

``$ kubectl create namespace {my-namespace}``                                     Create a namespace  
``$ kubctl get namespaces``                                                       List all namespaces  
``$ kubectl get ns``                                                              ns can be used instead of namespace  
``$ export CONTEXT=$(kubectl config view | awk '/current-context/{print $2}')``  
 `` $ kubectl config set-context $CONTEXT --namespace={my-namespace}``            Set a default namespace to launch resources in   


### Resource Quotas

``$ kubectl -n {namespace} get quota``                                   Quota usage within a namespace  
``$ kubectl -n {namespace} describe quota {quota-name}``                 Describe a resource quota   
``$ kubectl -n {namespace} get limits``                                  Returns list of current limits  
``$ kubectl -n {namespace} describe limits {limit-name}``                Show resources requests and max limits

  
### Nodes
 
``$ kubectl get nodes``                                       Returns list of all nodes  
``$ kubectl get node {node-name} --show-labels``              Show all labels for given node  
``$ kubectl describe node {node-name}``                       Describe node with verbose output   
``$ kubectl label node {node-name}  key=values``              Assign label to a node  
``$ kubectl label node {node-name} key=values --overwrite``   Overwrite a node label  
