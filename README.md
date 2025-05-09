Create Ec2 instance with ubuntu and t2 medium
ssh into instance
pull the files from git- install.sh and config.yml
to install - chmod 777 install.sh 
./install.sh
sudo apt-get update
now install docker -> sudo apt-get install docker.io
docker ps -> to see if docker is installed
if get error then need to add this to user group -> sudo usermod -aG docker $USER && newgrp docker
now to create cluster -> kind create cluster   --name=tws-cluster --config=config.yml
Kubectl get nodes
kubectl get ns or kubectl get namespace
kubectl get pods -n ns_name
kubectl create namespace nginx-namespace
kubectl apply -f deployment.yml 

