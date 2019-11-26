# How to run k8s cluster on you machine
The scripts based on the article: https://kubernetes.io/blog/2019/03/15/kubernetes-setup-using-ansible-and-vagrant/ with small changes. 

### Prerequisites
- Vagrant
- Ansible

My configuration MacBook, all of the prerequisites you can install use brew. 

### Define amount of worker nodes

in Vagrantfile:
```
N = 2
```


### Start  cluster
```bash
$ vagrant up
```

### Connect to the master node
```bash
$ vagrant ssh k8s-master
$ kubectl get nodes
NAME         STATUS   ROLES    AGE    VERSION
k8s-master   Ready    master   7m     v1.16.3
node-1       Ready    <none>   4m1s   v1.16.3
node-2       Ready    <none>   78s    v1.16.3
```

