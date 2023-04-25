# ansible-kubernetes
To deploy a kubernetes cluster with one master node and multiple worker nodes.

## Install
Change the `hosts` file according to your environment, then runnig the following command:
```
ansible-playbook -i hosts install-k8s.yml
```

## Reset
To reset the kubernets cluster, do as below, it will reset both masters and workers:
```
ansible-playbook -i hosts reset-k8s.yml
```

## Flannel
You can get the latest flannel pod network plugin here
```
https://raw.githubusercontent.com/coreos/flannel/master/Documentation/kube-flannel.yml
```

## Files
This ansible playbook use some files to notify ansible host to execute shell command or not:
|file|description|
|----|----|
|.swapoff	| If the file exists, swap is disabled|
|master_init	|If the file exists, master is initialized|
|flanner_init	|If the file exists, flannel is initialized|
|node_init	|If the file exists, node is initialized|
