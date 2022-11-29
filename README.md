# Task

#### to run vm vagrant file 
'''
vagrant up
'''

## setup kubernetes cluster with vagrant
#### Kubernetes-Kubeadm Vagrant Github Repository
'''
git clone https://github.com/ahmadjubair33/vagrant-kubernetes.git
'''
#### Launch Machine
'''
vagrant up
'''
#### login to the master node
'''
vagrant ssh master
'''
#### copy kube config file 
'''
scp vagrant@kmaster.example.com:~/.kube/config ~/.kube/
#password for vagrant is vagrant
'''

## build docker images  and push it to your registry
'''
docker build -t <img-name> .
docker tag <img-name> gcr.io/<project-id>/<img-name>
docker push gcr.io/<project-id>/<img-name>
'''

## deploy app on k8s cluster
'''
kubectl apply -f ./k8s-specifications/*
'''

### or run this script
'''
./RUN.sh
'''
