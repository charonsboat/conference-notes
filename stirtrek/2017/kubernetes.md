# kubernetes (k8s)

- Container orchaestration software
- Open Source

## k8s goals

- container vs vm focus
- portable (run everywhere)
- general purpose
    - any workload - stateless, stateful, batch, etc...
- flexible (consume wholesale or a la carte)
- extensible
- automatable
    - open rest api server
    - use anywhere in devops pipeline
- advance state-of-the-art
    - cloud-native and devops focused
    - mechanisms for slow monolith/legacy migrations

## k8s architecture

- kubectl
    - k8s master
        - kube-scheduler
        - kube-api-server
        - kube-controller-manager
        - etcd
    - k8s minons
        - kubelet
        - kube-proxy
            - maintains separate ips for each workload in kube minions (directs you to the correct minion)
        - cAdvisor
        - docker, rocket, etc...
            - pods (container)

For more architecture info, see slides...

## demo system

github.com/dalealleshouse/zero-to-devops

What it will include:

1. static files (nginx)
2. browsers
3. asp.net core rest api
4. rabbitmq server
    - producer (ruby)
        - puts items in the queue
    - consumer (java)
        - grabs items off the queue

Things set up before demo:

- cluster
    - minikube
- ingress
    - load balancers
    - hosts file
- docker registry

Info learned:

- can manage service exposure to ensure that containers are reachable regardless of their new ip addresses
- can expose specific services to public traffic

## default monitoring

k8s has a default dashboard out of the box (heapster)

## autoscaling

k8s can automatically scale pods up or down based on resource usage contraints

## self healing

if health checks fail, it will pull that pod out of the pool

## free course

https://www.udacity.com/course/scalable-microservices-with-kubernetes--ud615

