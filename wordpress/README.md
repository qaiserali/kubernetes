### Run Wordpress on a kubernetes cluster
This folder contains an example of how to run a Wordpress on a minikube kubernetes cluster within a namespace. Both Wordpress and MySQL database use PersistentVolume and 
PersistentVolumeClaim for storing data persistently on a hosting machine. Kubernetes secret is being used for storing the sensitive data such as MySQL credentials with encryption. 
