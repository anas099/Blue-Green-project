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
- instead of defining the mail SMTP as stage it can be added in jenkins System as below and create function to reconfigure it if needed
	- Generate APP password from Gmail
   	- Enter Systems from Manage jenkins
   	- smtp serve: smtp.gmail.com
   	- default user e-mail: @gmail.com
   	- use SMTP authentcation & add mail & key
    	- use ssl  
   	- port: 587
   	  
