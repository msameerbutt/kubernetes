# Kubernetes MiniCube Cluster

This guide will explain how you setup and run kubernetes minikube cluster on a VM. This guide is for linux centos 7

## Dependencies
1. Docker
1. Docker Compose
1. MiniKube
1. Kubectl
1. Kubectx
1. Nginx

## Setup
1. Install Docker and Docker Compose
1. Install MiniKube and Kubectl
1. Install Kubectx

    location /some/path/ {
        proxy_set_header Host $host;
        proxy_set_header X-Real-IP $remote_addr;
        proxy_pass https://localhost:8000;
    }


## Running a Minikube Cluster
1. ssh into the server `ssh user@45.76.185.146`
1. Switch to `developer` user by `su developer`
1. Check status of minikube `minikube status`
1. Start minikube with `minikube start --vm-driver=docker`
1. Start External Service with `minikube service mongodb-express-service --namespace=demo-namespace`
1. Set this for nginx `setsebool -P httpd_can_network_connect on`


## Resources
1. [How To Install and Use Docker on CentOS 7](https://www.digitalocean.com/community/tutorials/how-to-install-and-use-docker-on-centos-7)
1. [RHEL 8 / CentOS 8 open HTTP port 80 and HTTPS port 443 with firewalld](https://linuxconfig.org/redhat-8-open-http-port-80-and-https-port-443-with-firewalld)
1. [How to Install Minikube on CentOS](https://phoenixnap.com/kb/install-minikube-on-centos)
1. [Installing Minikube on CentOS](https://vocon-it.com/2018/11/19/single-node-kubernetes-cluster-1-installing-minikube-on-centos/)
1. [https://centos.pkgs.org/7/harbottle-main-x86_64/kubectx-0.6.3-1.el7.harbottle.x86_64.rpm.html]
1. [Intalling kubectx]()
1. [Running Minikube with `vm-driver=none`](https://nieldw.medium.com/running-minikube-with-vm-driver-none-47de91eab84c)
1. [Kubernetes on CentOS 7 with Firewalld](https://medium.com/platformer-blog/kubernetes-on-centos-7-with-firewalld-e7b53c1316af)