# Blue-Green-project

- install kubectl & azure cli
- AZ login
  az group create --name myResourceGroup --location southcentralus
  az aks create --resource-group myResourceGroup --name myAKSCluster --node-count 1 --enable-addons monitoring --generate-ssh-keys
  
  connect to the cluster:
  
   az aks get-credentials --resource-group myResourceGroup --name myAKSCluster --overwrite-existing
	  
- Setup AKS credentials id (K8s) 
	
	- create global credentials:
		secretfile
		- add kubeconfig file 
		
- create Jenkins Job (pipeline)
	- Name: Jenkinsjob
	- code from SCM (git)
	- repo (https://github.com/anas099/Blue-Green-project/tree/main)
	- branch (*/main)
	- script path (Jenkinsfile)
