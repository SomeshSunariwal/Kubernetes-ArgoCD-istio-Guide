# Kubernetes-ArgoCD-Guide

Here I try to Create end to end flow with Kubernetes and ArgoCD.

## 1. what it is?

1. Open source container orchestration tool
2. Developed by Google.
3. Manage Containerize Applications

## 2. Advantage

1. High Availability
2. Scalability
3. Disaster Recovery

## 3. Kubernetes Components

### 3.1 Pods

1. Smallest Unit
2. Abstraction over Container
3. 1 Application per pod.
4. Each pod gets it own IP Address.

`Issue` : If service ran out of resources then pod will die and it will create a new pod with new IP address which is not great because pods will talk to each other with IPs. So we attach to service component.

### 3.2 Service

1. Permanent IP address to each pod
2. Attach to pod but life cycle of pod and service is not attached means if pod dies service component still intact.
3. 2 Type of service
   1. internal Service
   2. external Service
4. Work as a load Balancer between 2 or more pods.

### 3.3 Ingress

1. Request from outside first go to ingress and then forward to service.

![image](images/image1.jpg)

### 3.4 Config Map

1. URLs and Endpoints are stored in config so if URL gets changes than only need to change in config map

### 3.5 Secret

1. It is used to store credentials
2. Base64 encoded

### 3.6 Volume

1. A physical device is attach to pod.
2. Prevent data lose when pod restart or crashed.
3. Its not taken care by kubernetes.

### 3.7 Replication

1. Deployment file is a blueprint of pod
2. Deployment file handle pods replication.
3. Deployment file is for stateless component.
4. Now on if pod dies then request will be forwarded to another pod
5. Database read and write state be handled by statefulSet but
6. Deploying statefulSet is not easy process. Common practice is to host database outside the kubernetes cluster.

![image](images/image2.jpg)
