# Kubernetes / K3s / K3d

Kubernetes: also known as K8s, is an open-source system for automating deployment,
scaling, and management of containerized applications.
K3S: Lightweight Kubernetes
K3D: a lightweight wrapper to run k3s (Rancher Lab’s minimal Kubernetes distribution) in docker.



## Doc

 - Kubernetes (K8s): https://kubernetes.io
 - K3s: https://k3s.io (https://github.com/k3s-io/k3s)
 - K3d: https://k3d.io
 - Kubernetes dashboard: https://kubernetes.io/docs/tasks/access-application-cluster/web-ui-dashboard/
 - Kubectl: https://kubernetes.io/docs/tasks/tools/#kubectl



[![N|Solid](https://k3s.io/img/how-it-works-k3s-revised.svg)](https://k3s.io)



## Install

 - Docker:

   https://docs.docker.com/desktop/install/linux-install/

   Add user to group 'docker'
   > ~# sudo systemctl start docker



 - Kubectl:

   > https://kubernetes.io/docs/tasks/tools/#kubectl



 - K3d:

   > wget -q -O - https://raw.githubusercontent.com/k3d-io/k3d/main/install.sh | bash

   > ~# k3d cluster create mycluster
   > ~# kubectl get nodes



 - Dashboard:

   > https://kubernetes.io/docs/tasks/access-application-cluster/web-ui-dashboard/



   -- Create Admin User:

   > https://github.com/kubernetes/dashboard/blob/master/docs/user/access-control/creating-sample-user.md

   > ~# kubectl apply -f dashboard-adminuser.yaml
   > ~# kubectl apply -f clusterrolebinding.yaml



   -- Dashboard:

   > ~# kubectl apply -f https://raw.githubusercontent.com/kubernetes/dashboard/v2.7.0/aio/deploy/recommended.yaml
   > ~# kubectl proxy

   > In browser: http://localhost:8001/api/v1/namespaces/kubernetes-dashboard/services/https:kubernetes-dashboard:/proxy/




:)
