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

15. Run ArgoCD Server

```bash
kubectl port-forward svc/argocd-server -n argocd 8080:443
```

16. Get all info with namespace

```
kubectl get all -n namespace-name
```

17. Describe Service Related all Info

```bash
kubectl describe service service-names
```

18. Get the wide info of all pods

```bash
kubectl get pods -o wide
```

19. See the deployment file in terminal

```bash
kubectl get deployment deployment-name -o yaml
```

20. Assign external IP address to externally expose service

```bash
minikube service service-name
```

21. Create namespace

```bash
kubectl create namespace new-namespace-name
```

22. Cluster info

```bash
kubectl cluster-info
```

23. Particular component info in namespace

```bash
kubectl get pod -n namespace-name

kubectl get service -n namespace-name

kubectl get deployment -n namespace-name
```

24. Show Namespace label

```bash
kubectl get ns default --show-labels
```

25. Istio Web Hook Injection

```bash
kubectl label namespace default istio-injection=enabled
```

26. Port Forwarding to access service locally

```bash
kubectl port-forward svc/service-name -n namespace port-number
```

ex: kubectl port-forward svc/kiali -n istio-system 20001

27. Get minikube addons

```bash
minikube addon list
```

28. Enable addons

```bash
minikube addon enable ingress
```

29. Get the nodes IP info

```bash
kubectl get node -o wide (Internal IP)
```

30. get IP range for this node

```
sipcalc [InternalIP].1/24
```

if your internal IP is 127.0.23.45

ex: sipcalc 127.0.23.1/24

31. Continues Request to server for testing only

```bash
watch curl -s -o /dev/null http://192.168.39.210:80/productpage
```

32. nginx-ingress controller IP

```
minikube ip
```
