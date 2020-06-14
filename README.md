Example of how to deploy a full application with multiple pods and services using deployments. More info on the application on : https://github.com/dockersamples/example-voting-app

This application has 5 different pods:
- postgres-pod
- redis-pod
- result-app-pod
- voting-app-pod
- worker-app-pod

two services with type ClusterIp allowing the internal communication between pods:
- redis-service
- postgres-service

and another two services with type LoadBalancer exposing our two websites external:
- voting-app-service
- result-app-service

To execute this we can use our own kubernetes environment or create a cluster in a cloud solution like Google Cloud. In both options the commands needed to create the pods are:
- kubectl create -f voting-app-pod.yaml
- kubectl create -f voting-app-service.yaml
- kubectl create -f redis-pod.yaml
- kubectl create -f redis-service.yaml
- kubectl create -f postgres-pod.yaml
- kubectl create -f postgres-service.yaml
- kubectl create -f worker-app-pod.yaml
- kubectl create -f result-app-pod.yaml
- kubectl create -f result-app-service.yaml