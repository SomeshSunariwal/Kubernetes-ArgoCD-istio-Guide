# Commands

1. Start minikube

```bash
minikube start --driver=docker
```

2. Set Default docker runtime

```bash
minikube config set driver docker
```

3. Minikube status

```bash
minikube status
```

4. Get the nodes

```bash
kubectl get nodes
```

5. Check Pods

```bash
kubectl get pods
```

6. Check Services

```bash
kubectl get services
```

7. Create POD

```bash
kubectl create deployment image-name --image=nginx
```

8. Check Deployment

   deployment is a blueprint of deployment

```bash
kubectl get deployment
```

9. Check ReplicaSet

```bash
kubectl get replicaset
```

10. Edit Deployment file

    Auto generated file from point 7

```bash
kubectl edit deployment image-name
```

deployment file can be edited. if edited then old pod will be deleted and new one created.

11. Logs

```bash
kubectl logs image-name-nodeID-podID
```

12. Interactive mode in kubectl

```bash
kubectl exec -it image-name-nodeID-podID -- bin/bash
```

`example` : image-name-579895999f-66mhv

13. Delete deployment

Deleting deployment will automatic delete pods

```bash
kubectl delete deployment image-name
```

14. Apply kubernetes files

```
kubectl apply -f filename.yaml
```
