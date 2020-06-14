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

To execute this we can use our own kubernetes environment or create a cluster in a cloud solution like Google Cloud. In both options we can clone this github repo and execute the following command:
- kubectl create -f .