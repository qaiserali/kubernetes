### Deploy Wordpress on a kubernetes cluster via Helm charts
This folder contains an example of how to deploy Wordpress on a minikube kubernetes cluster within a namespace via helm charts. Both Wordpress and MySQL database use PersistentVolume and PersistentVolumeClaim for storing data persistently on a hosting machine. Kubernetes secret is being used for storing sensitive data such as MySQL credentials with encryption. 

**Steps to deploy.**  

- Make sure that helm is installed on your cluster and working properly. Visit the link for more details https://docs.helm.sh/using_helm/  

- Deploy MySql stateful app   
`` helm install --namespace wordpress --name mysql mysql/ `` 

- Deploy Wordpress app  
`` helm install --namespace wordpress --name wordpress wordpress/``