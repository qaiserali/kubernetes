### Run Wordpress and MySQL on kubernetes cluster
This directory contains an example of how to run a Wordpress and MySQL database on a kubernetes cluster.Both Wordpress and MySQL applications use PersistentVolumes and PersistentVolumeClaims to store data on your host machine. Kubernetes secret is used for storing sensitive data such as root and db passwords etc.

#### Kubernetes Secret object
A secret is an object for storing sensitive data such as MySQL user or database password. You can put all the secrets in the secret manifest file with base64 encoded format.

#### Persistent Volumes and Persistent Volumes Claims
PersistentVolumes(PV) is defined as a storage in the cluster, but their lifecycle is independent of the pods that uses them.  It’s a resource in the cluster just like a node in the cluster resource. PVs are volumes plugins and the API support a large variety of implementations of the storage such as NFS, iSCSI, cloud provides such as AzureFile, AzureDisk, AWSElasticBlockStore etc.

PersistentVolumeClaims(PVC) are pods requests to obtain storage/volumes.  It’s similar to the Pods but Pods consumes node resource such as Memory and CPU, and PVC consume PV resources such size and access mode (read-only, read/write). Once the request is obtained, the volume is then mounted to a specific path in the pod.   
